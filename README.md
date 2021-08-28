# GitFlow.Practice

---
## Init

```s
$ git flow init
```

The default branch stratrgy:

| Branch name/prefix | Description |
|:------------------:|:------------|
| `master` | Production releases. |
| `develop` | Next release development. |
| `feature/` | Feature branches |
| `bugfix/` | Bugfix branches |
| `release/` | Release branches |
| `hotfix/` | Hotfix branches |
| `support/` | Support branches |


Then sync with a remote repository (optionaly) by

```s
$ git remote add origin git@github.com:<id>/<repository>
```


---
## Feature Branch


### Create a feature Branch based on develop branch

```s
$ git flow feature start <branch_name>
```

Or by

```s
$ git checkout -b feature/<branch_name> develop
```



### Track and push to the remote branch

After saving changes to local repository, we can push the commit(s) to remote by,

```s
$ git flow feature publish <branch_name>
```

Or

```s
$ git push --set-upstream origin feature/<branch_name>
```

After that we can push commit(s) with `git push`.


### Checkout an exist branch and pull

```s
$ git flow feature pull origin <branch_name>
```

Or

```s
$ git checkout feature/<branch_name>
$ git pull --rebase
```


### Merge to develop branch

```s
$ git checkout develop
$ git pull --rebase
$ git flow feature finish <branch_name>
$ git push
```

Or

```s
$ git checkout develop
$ git pull --rebase

# Merge feature branch to develop branch without fast-forward
$ git merge --no-ff feature/<branch_name>
$ git push
$ git branch -d feature/<branch>
```


---
## References

- [git-flow cheetsheet](https://danielkummer.github.io/git-flow-cheatsheet/)

