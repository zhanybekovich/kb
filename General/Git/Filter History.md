
## Last 3 commits

`git log --oneline -3`

## Filter commits by author

`git log --oneline --author="<author name>"`

## Filter by date

`git log --oneline --before="2020-08-07"`

`git log --oneline --after="2020-08-07"`

## Filter by relative days

`git log --oneline --after="yesterday"`

`git log --oneline --after="one week ago"`

## Filter by commit message

`git log --oneline --grep="GUI"` --> case sensitive

## Filter by changes in the files

### Filter commits that adds or deletes hello function declaration

`git log --oneline -S"hello()"` --> all commits that add or delete 'hello()'

`git log --oneline -S"foo"` --> all commits that add or delete word 'foo'

## Filter commits by range

`git log --oneline <startHash>..<endHash>`

## Filter commits that touch particular file or files

`git log --oneline <fileName>`

or 

`git log --oneline -- <fileName>`



