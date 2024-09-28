
1. Check status
2. Prepare files for Staging Area
3. Commit

## Check status

```
git status
```

## Staging Area

Add a file

`git add <fileName>`

Add multiple files

`git add <fileName> <fileName2>`

Add files with pattern

`git add *.txt`

Add files in the current directory

`git add .`

## Commit

Short commit

`git commit -m "Commit message"`

Full Descriptive commit with defined default code editor

`git commit`

## Commit with skipping staging area

With separate flags 
`git commit -a -m "Commit message"`

With joined flages
`git commit -am "Commit message"`


