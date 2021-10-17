# gitflow-demo
gitflow demo

while developing at branch feature/xxxx, a bug needs to be fix.
```
git stash
git checkout -b hotfix/yyyy main
# fix bug
git commit -a 
git checkout develop
git merge --no-ff hotfix/yyyy
git checkout main
git merge --no-ff hotfix/yyyy
git tag -a v0.1.1 -m "fix balabala bug"
git branch -d hotfix/yyyy
git checkout feature/xxxx
git merge --no-ff develop
git stash pop
```

