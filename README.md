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
## Create a feature Branch from develop branch

```s
$ git flow feature start <branch_name>
```

Or by

```s
$ git checkout -b feature/<branch_name> develop
```



## Push the commit
