### Init a empty dir as local repo

```
mkdir git-demo
cd git-demo
git init
```


### Add untracked files (aka Stage)
```
touch f
mkdir d/
touch d/f2
# See the status of stash and untracked file
git status
git add -A .
git status
```

### Commit to local repo
```
git commit -m "local commit"
git status
# see all local commits
git log --oneline
```
