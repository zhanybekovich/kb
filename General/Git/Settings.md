
## Basic Git Configurations

- Name
- Email
- Default Editor
- Line Ending

## Settings Leve

- System -> all users
- Global -> all repos of the current user
- Local -> the current repository

## Name 

```
git config --global user.name "John Doe"
```

## Email

```
git config --global user.email john@johnny.com
```

## Default Editor

Before adding editor be sure it is available via CLI

Example of setting VS Code as default editor:

```
git config --global core.editor "code --wait"
```

## Config End of Lines

For windows

```
git config --global core.autocrlf true
```

For Mac

```
git config --global core.autocrlf input
```
## Editing Global Config File via Default Editor

```
git config --global -e
```

## Setting default tool for Diff

```
git config --global diff.tool vscode
```

Set how start vscode

```
git config --global difftool.vscode.cmd "code --wait --diff $LOCAL $REMOTE"
```

Final config should look like:

```
[user]
    name = Mirlan Urzhanov
    email = urzhanovmirlan@gmail.com
[core]
    editor = code --wait
    autocrlf = true
[diff]
    tool = vscode
[difftool "vscode"]
    cmd = "code --wait --diff $LOCAL $REMOTE"
```

## View diff via difftool

To view changes via difftool run:

`git difftool`

or

`git difftool --staged`