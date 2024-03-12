# How to using branch

## Create new branch / checkout to another branch
### Checkout and create (if nothing)
```bash
git checkout -b "branch-name"
```
example
```bash
git checkout -b "develop"
```
### Checkout to exist branch
```bash
git checkout main
```

### Push new branch
```bash
git push -u origin {new-branch-name}
```

### Example
```bash
git push -u origin create-classroom-schema
```

## Delete branch
```bash
git branch -D "branch-for-delete"
```
### Example
```bash
git branch -D "encode-decode-data"
```

## Full
1. create new branch
2. push new branch
3. back checkout to develop
```bash
git branch
# develop
git checkout -b "new-branch"
git push -u origin new-branch
git checkout develop
```
