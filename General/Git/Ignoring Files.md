
## Create .gitignore file

Define ignored files and directories in `.gitignore` file

```
logs/
main.log
*.log
```

If file was accidentally committed and  then added in `.gitignore`:
remove file from staging are via: 
- for a file `git rm --cached <file>`
- for a directory `git rm --cached -r <directory>/`

## Example of gitignore files

https://github.com/github/gitignore

