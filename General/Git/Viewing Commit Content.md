
To view the content of the commit after log command:

`git show <commitHash>`

or:
the last commit

`git show HEAD`

or the previous commits

`git show HEAD~<step>`

## To view the final version of the file in the history

`git show HEAD~1:<fileFullPath>`

## All files in the commit

`git ls-tree HEAD~<step>` and then `git show <fileID>`

## View commit specified by steps

`git show HEAD~<step>`

`<step>` -> is a number eg. 2

## View all changed files in the specified commit

`git show HEAD~<step> --name-only`

## View all changed files in the specified commit by their status: added, modified etc

`git show HEAD~<step> --name-status`

