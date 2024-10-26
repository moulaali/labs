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

### Time travel in local checkouts
```
git log --online
# pick one of the snapshots
git checkout <hash>
ls
# go back to head
ls
git checkout master
```

### Revert/undo staged but not commited files
```
echo blah >> f
git add -A .
git status
git reset --hard
# change should be gone
cat f
git status
```

<img src="[https://github.com/user-attachments/assets/946cecc2-2c72-4aad-8640-e583f0691d6c" style="width:50%;"/>

![image](https://github.com/user-attachments/assets/946cecc2-2c72-4aad-8640-e583f0691d6c)

