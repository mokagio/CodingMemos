Git Memos
=========

####List tags with message

```bash
git tag -n
```

####Pull a new branch

```bash
git checkout --track origin/my_new_branch
```

####Push a new branch

```bash
git push -u origin my_new_branch
```

####Delete a branch locally and on the server

_Warning: always think about it twice before deleting a branch_

```bash
git branch -d obsolete_branch               # locally
git push origin --delete obsolete_branch    # from the server (origin)
```

####Rename a branch

To rename the current branch
```bash
git branch -m <new_name>
```

To rename any branch
```bash
git branch -m <branch_name> <new_name>
```
