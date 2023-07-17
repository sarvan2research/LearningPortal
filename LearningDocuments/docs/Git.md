# Git Learnings
Learn git related things
## Git Init
Below command used to setup repo and add it to master
```
git init
git add .
git commit -m "First commit"
git remote add origin git@github.com:sarvan2research/LearningPortal.git
git push -u origin master
```

## Git Revert commit before and after push
(Reference Link)[https://stackoverflow.com/questions/1611215/remove-a-git-commit-which-has-not-been-pushed]
```

#IF you have NOT pushed your changes to remote

git reset HEAD~1

#Check if the working copy is clean by git status.

#ELSE you have pushed your changes to remote

git revert HEAD

```

### Git Remove local changes
    This will unstage all files you might have staged with git add:
```
    git reset
```
    This will revert all local uncommitted changes (should be executed in repo root):
```
    git checkout .
```
    You can also revert uncommitted changes only to particular file or directory:
```
    git checkout [some_dir|file.txt]
```
    Yet another way to revert all uncommitted changes (longer to type, but works from any subdirectory):
```
    git reset --hard HEAD
```
    This will remove all local untracked files, so only git tracked files remain:
```
    git clean -fdx
```
  
To sum it up: executing commands below is basically equivalent to fresh git clone from original source (but it does not re-download anything, so is much faster):
```
git reset
git checkout .
git clean -fdx
```