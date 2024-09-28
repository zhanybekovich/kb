
## Customize output

### Format commits by author and commit hashes

- `%an` -> author
- `%H` -> hash
- `%h` -> short hash
- more: https://git-scm.com/docs/git-log -> look for `placeholders`

`git log --pretty=format:"%an commited %H"`

or

`git log --pretty=format:"%an commited %H on %cd"`

