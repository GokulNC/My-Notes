## Mini Git Cheatsheet
It's not that git is difficult, but I seem to forget the commands if lose touch say for a year.

### Branch out from another branch
```console
$ git checkout -b dev master
```

### Merge (no fast forward)
```console
$ git checkout master
$ git merge --no-ff dev
```

### Ignore file mode changes
```console
$ git config --global core.fileMode false
```

### Change git editor
```console
$ git config --global core.editor "nano"
```

### Change author name of last commit
```console
$ git commit --amend --author "Gokul NC <gokulnc@ymail.com>"
```
(For previous commits, [do this](https://stackoverflow.com/a/28845565/5002496))
