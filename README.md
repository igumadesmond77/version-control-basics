# version-control-basics
## This project contains only a ReadMe file with some information about version control using git and explanation of some of its associated terms
## The project only contains a ReadMe file detailing the explanations

# What is version control  
Version control (also known as source code management) is the software engineering practice of controlling, organizing, and tracking different versions in history of computer files; primarily source code text files, but generally any type of file.

# The difference between Git and Github
The main Git vs GitHub difference is in their functionality. While they both provide source code management (SCM) and make merging and sharing code easier, this is pretty much where their similarities end. Think of Git as a single computer and GitHub as a network of multiple interconnected computers, all with the same end goal but a wildly different role for how to get there.

# Alternatives to Github
*GitBucket
*Apache Allura
*Codegiant

# Difference between git fetch and git pull
In the simplest terms, git pull does a git fetch followed by a git merge(or git rebase).
git fetch gathers any commits from the target branch that do not exist in the current branch and stores them in your local repository. However, it does not merge them with your current branch. 
On the other hand, git pull tries to automatically merge after fetching commits. It is context sensitive, so all pulled commits will be merged into your currently active branch. git pull automatically merges the commits without letting you review them first

# Git Rebase
The git rebase command allows you to easily change a series of commits, modifying the history of your repository. You can reorder, edit, or squash commits together. Typically, you would use git rebase to: edit previous commit messages, combine multiple commits into one, and delete or revert commits that are no longer necessary.
The default command for git rebase follows this syntax: 
***git rebase [-i | --interactive] [ options ] [--exec cmd] [--onto newbase | --keep-base] [upstream [branch]]***
For example, To rebase all the commits between another branch and the current branch state, you can enter the following command in your shell:
***git rebase --interactive OTHER-BRANCH-NAME***

# Git Cherry pick
With the Cherry-pick command, Git allows you to integrate selected, individual commits from any branch into your current HEAD branch. Simplistically, it is the act of picking a commit from a branch and applying it to another.
The basic command for cherry pick involves providing the SHA identifier of the commit you want to integrate into your current HEAD branch. For example: 
***git cherry-pick commitSha*** where "commitSha" is the sha identifier of the commit you want to integrate
Git cherry pick can also be passed using other execution options like: ***-edit***, ***--nocommit***, ***--signoff***
