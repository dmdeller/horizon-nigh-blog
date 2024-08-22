---
layout: post
title: How to merge Subversion branches with Git
date: '2011-02-17T23:05:00-08:00'
tags: []
tumblr_url: https://blog.horizon-nigh.org/post/3356960878/how-to-merge-subversion-branches-with-git
---
Git-svn is good. It’s really good. As others have said, it’s actually _too_ good, in that it reinforces the status quo (of continuing to use a Subversion repository regardless of the inherent issues) and the process of merging exemplifies this in a particularly insidious way.

It happens to many Git users that they are eventually forced to work with a Subversion repository. Fine, they’ll say, no problem. Just use Git-svn and you can do just about anything like you normally would in Git. Pushing to the repository will take longer, but oh well.

Then someone has to merge something.

Subversion users _hate_ merging. It’s slow, it’s difficult, things go wrong and they have no idea why. They can read the docs cover to cover, they can Google it for hours, but they will never find out how to make it work right. They blame themselves, because it’s supposed to work, but they don’t know what to do. It’s just painful and they’ve resigned themselves to that fact.

But then you come along, and you have Git-svn. All other interoperation between Git and svn works so flawlessly, you just assume merging should work as well. So you do the merge in Git, it takes under a second and it looks like it worked fine. Problem solved?

Unfortunately, you probably never read the ‘caveats’ section in 'git help svn’. Go ahead and read that now.  
(Tip: git help -w svn)

But maybe you didn’t read it, or maybe you shrug and say, 'eh, it seemed to work fine’, and you go ahead and 'git svn dcommit’ the merge.

Basically: Git-svn supports **reading** Subversion merge metadata, but doesn’t support **writing** it. If you 'git svn dcommit’ that merge, the Subversion server will receive all of the file changes but nothing to indicate it’s a merge. It will look like you made those changes all by yourself, in one commit. And of course, Subversion doesn’t support Git’s merge metadata either, so this isn’t even preserved for future Git-svn clones of the repository.

The result of this:

### If you do a Git merge of Subversion repositories, you are the only one who can ever see that merge again.

(And even then, only if you keep that working copy of yours preserved forever). All other Subversion users _and_ all other Git-svn users will not see this as a merge. And because of this, you have made future merges, annotations, history tracking, and many other things _much more difficult_ for everyone else, whether they use Subversion or Git-svn. (In particular, it may make future merges with Subversion on that branch nearly impossible.)

This is why the safest thing to do, and what I always recommend to Git-svn users, is:

### Never merge Subversion branches with Git.

Switch back to Subversion when you need to merge Subversion branches. Yes, it’s slow, painful and error-prone. This is your motivation to convince the organisation to switch to a sane SCM (remember, as much as Git seems like the best one, there are several alternatives that, if not as good as Git, would at least be an improvement). You can only do so much to work around a system that is fundamentally broken. If your organisation seems incapable of understanding this, it may be an indication that that organisation is also fundamentally broken, and you may wish to consider how much you can do to work around _that_.

### However…

If you’re not going to heed my warning, and you’re determined to do it anyway, here’s how to do it while keeping the level of destruction you cause to a minimum.

Assume you’re merging a branch named 'source’ into a branch named 'target’. Open two Terminal windows (or tabs, whatever): one for Git, one for svn. The part before the $ indicates the line number and which Terminal you should type into.

It should go without saying that if you receive errors at any point (not counting conflicts, which you should resolve normally), and you don’t understand what’s going on, you should abort the process, undo whatever destruction you have caused and start over.

    [01:git]$ git checkout target
    [02:svn]$ svn checkout proto://url/to/target target
    [03:svn]$ cd target
    [04:git]$ git svn fetch
    [05:git]$ git svn rebase -l
    [06:git]$ git merge remotes/source # (resolve any conflicts)
    [07:git]$ git commit --amend -m "Merge source - PARTIAL"
    [08:git]$ git svn fetch # IF THE RESULT of this is that you received more commits, GOTO line 05
    [09:git]$ git svn dcommit
    [10:svn]$ svn up # IF THE RESULT of this is that you received more commits OTHER THAN YOUR MERGE(s), GOTO line 04
    [11:svn]$ svn merge proto://url/to/source --record-only
    [12:svn]$ svn commit -m "Merge source - COMPLETE"

The key here is the ’–record-only’ option to 'svn merge’, which only sets the metadata and does nothing else. This should effectively repair the missing metadata caused by your Git-svn merge.

As you can see, this is a rather ridiculous amount of effort to do a merge. What’s more ridiculous, though, is that it may end up being drastically less time and effort than doing the merge with Subversion, due to all of the nonsensical conflicts that Subversion introduces, and/or simply the amount of time Subversion takes to do anything (I have literally sat watching Subversion churn through a merge of a few large commits for 30+ minutes, when Git did the same thing in less than one second).

The risk here (besides the possibility of you doing a step wrong), and the reason for all of the GOTOs, is that your merge is split across several commits, and while you’re committing them, other users may still be using the repository (especially while line 09 is executing, which can take a while). If the merge **content** from Git and the merge **metadata** from svn don’t agree, you have a big problem that will cause a lot of trouble for you. If possible, it is advisable to ask other users to stop committing while you’re doing this. If it is not possible to ask this, or if doing so would draw you ire, and indeed if you’re working with a high-traffic repository, my solution may be essentially impossible for you to complete (infinite loop).

An odd side effect that you may notice: your Git working copy will show the merge as having occurred at your **first** commit, but other Git-svn clones or Subversion clients will show it as having occurred at your **last** commit. This is probably a minor issue.

One last word of advice: Avoid doing people too many favours by doing their merges for them. You could end up becoming a de-facto Release Engineer, and that’s not a fun job.

