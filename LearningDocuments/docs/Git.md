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