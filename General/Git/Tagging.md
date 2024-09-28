
## Tagging

`git tag <tag>` -> tagging the last commit

Eg: `git tag v1.0`

`git tag <tag> <hash>` -> tagging specific commit

Eg: `git tag v1.0 5e7a828`

## Checking out to tag

`git checkout <tag>`

## View all tags

`git tag`

## Annotated tag

Creating annotated tag: `git tag -a <tag> -m "<Message>`. 

Eg: `git tag -a v1.1 "My version 1.1"`

### View message of tags

`git tag -n`

If tag is annotated above command shows tag messages or message of the commit

## Delete tag

`git tag -d <tag>` Eg: `git tag -d v1.1`

