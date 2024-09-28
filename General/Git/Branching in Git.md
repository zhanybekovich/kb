
## Creating branch

`git branch <branchName>` Eg: `git branch bugfix`

## View branches

`git branch`

## Switching branches

`git switch <branchName>` Eg: `git switch bugfix`

or

`git checkout <branchName>`

## Create and switch to new branch

`git switch -C <newBranch>`
## Renaming branch name

`git branch -m <oldName> <newName>`

Example of renaming bugfix branch to more specified branch name:

`git branch -m bugfix bugfix/signup-form`


## Deleting branch

If changes of the branch are merged into master you may delete branch by:

`git branch -d <branchName>`

Git prevents from deleting branches that are not merged with master to force delete use:

`git branch -D <branchName>`

## Compare changes in branches

Bellow command shows all commits in bugfix branch that are not in master

`git log master..bugfix`

### View changes in branches

`git diff master..bugfix`

or view diff between current branch and specified branch

`git diff <branch>`

### View files 

`git diff --name-status <branch>`

or

`git diff --name-only <branch>`


## Stashing

If the working area is dirty and there are changes that not committed it is not allowed to switch to other branches. In order to save changes and not to loose them use **stashing**.

### Creating

`git stash push -m "<message>"`

### View stashes

`git stash list`

### View changes in the stash

`git stash show <stash>` Eg: `git stash show stash@{1}` or short: `git stash show 1`

### Apply changes of the stash to working directory

`git stash apply <stashNumber>` Eg: `git stash apply 1`

### Delete stashes

Delete specified stash: `git stash drop <stashNumber>`

Delete all: `git stash clear`


## Merging

There are 2 ways of merging:
1. Fast-forward -> if branches have not diverged
2. 3-way -> if branches have diverged

## Fast-forward merge

Before merge switch to the needed branch and run:

`git merge <branch>`

It is possible to merge without fast-forward in this case for merge will be created new commit

`git merge --no-ff <branch>` and then create your merge commit message.

## Disable fast-forward merge in current repository

`git config ff no`

Disable globally: 

`git config --global ff no`

## View branches that were merged to current branch

`git branch --merged`

## View branches that were not merged to current brach

`git branch --no-merged`

## Merge Tools

- Kdiff
- P4Merge
- WinMerge (Windows)

### Example of setting P4Merge as mergetool

1. Install P4Merge
2. run `git config --global merge.tool p4merge`
3. run `git config --global mergetool.p4merge.path "C:\Program Files\Perforce\p4merge.exe"`

To run the merge tool during merging run `git mergetool`
``
