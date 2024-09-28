
If file was accidentally deleted it's possible to  restore it.

To restore:

- find all commits that touch the file: `git log --oneline -- <deletedFile>`
- in the logged list possibly file was deleted in the last commit so you should checkout to the 1 commit before: `git checkout <hash> <file>`
- and commit your restore


