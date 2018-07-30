Pull Requests
=============

> *This guide assumes a knowledge of branching. If you are new
to that topic, please see the guide on branching.*

What
----
A pull requests (PR) is a *request* to merge code from a feature
or bug fix branch into the master (or another restricted) branch.
PRs can also be used for peer code reviews allowing a fellow
developer to look over your changes and approve them before they
can be merged.

Why
---
Using pull requests (PRs) allows the project history to not
only remain clean (no random commits whose purpose is unclear),
but also to remain stable (complete features and fixes are merged
into master instead of parts). This method goes hand with the
methodology of committing "early and often"; it allows for a
detailed history of each feature without the fear of cluttering
the master branch.

When
----
Any time you have completed a feature or bug fix, and you would
like it to be merged into `master` or another restricted branch. 

How
---
In Team Foundation Server, click `Code`, and then `Pull Requests`.
Select the repository your changes are in using the selector on
the top of the page. If you have recently pushed changes to that
repository, a banner will appear at the top of the page asking if
you want to create a pull request from your branch into master.
You may use that option as a starting point, or you may start
from scratch.

When you first start creating a PR, you must specify the *source 
branch*, where your changes are, and the *target branch*, the 
branch you want your changes merged into. You can then give the 
PR a name describing the changes you want merged and description 
detailing what exactly was changed. You might find the messages 
of the commits that comprise the PR are a suitable description,
in which case you won't need to do much more than include them in
your description to complete it. You may also link TFS work items
(bugs, stories, features, etc.) in both the description and in
the PR itself. Keep in mind that any items linked in the PR 
directly will be *automatically* closed upon the merging of your 
PR, so if that is not a desired behavior, you should only mention 
that item in the description by using the pound symbol (#) 
followed by the work item number. The last step when creating a PR
is to add reviewers, someone who is invited to review the changes 
proposed by the PR. Once you've added reviewers, you can now 
finish the creation of your PR and move on to the next task while 
you wait for your awesome code to be reviewed.

When reviewing a PR, you may choose to accept or reject it, and 
to optionally provide a comment on your decision. Please be clear 
when commenting on PRs, if the issue is related to an existing 
work item make sure to link that work item for easy reference.

If you end up needing to make changes due to feedback on your
PR, all you need to do is push your new commits to the source
branch of your PR; it will automatically be updated in TFS.

Once all your changes have been approved, you or your manager may
merge the PR into the target branch. This is done by clicking the
`Merge` button on the PR's page in TFS. This will give you a 
prompt and ask you whether or not the source branch should be 
deleted, and the linked work items closed. The answer to both of 
those questions should be yes, and if you're hesitant, you should 
stop and review your PR, and possibly ask someone else for a 
second opinion.

**That's it**, your code now happily lives in the master branch! 