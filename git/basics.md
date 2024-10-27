## Basic Concepts
- Git operates locally in three spaces : working directory, staging area and commited snapshots

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

<img src="https://github.com/user-attachments/assets/946cecc2-2c72-4aad-8640-e583f0691d6c" style="width:60%;"/>

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

### Revert a committed snapshot which will create another snapshot
```
git log
git revert <hash>
git log
```

## Branching
- Sub branches are called topic branches (for features, hot-fixes...)

### Merge 
```
git checkout -b branch2
echo blah >> branch2_file
git add -A .
git commit -m "branch 2 commit"
git log --oneline
# merge into master
git checkout master
git merge branch2
# HEAD/top moved to include the branch commits
git log --oneline
```

- The above merge is fast forward merge
- This is possible when a branch came out of master and just added the commits in linear way as shown below:
  
![image](https://github.com/user-attachments/assets/4db1d1be-274d-4ae1-9a95-1c6511b2d4d1)

![image](https://github.com/user-attachments/assets/3cb6877b-8ceb-41f7-8696-3132441c62dd)
