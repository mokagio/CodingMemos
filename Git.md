Git Memos
=========

####List tags with message

```bash
git tag -n
```

#### Delete a tag

```bash
git tag -d TAG
git push --delete origin TAG
```

#### Discard local history and merge remote branch

_**Note** this section needs a bit more reserach to really understand the problem we're trying to solve._

Example scenario: you pushed your feature branch last night from the office, and now you're working from home. You need some code that's been added to master, a new library that makes things easier for example, so you rebase the feature branch onto master. You keep developing. The day after you're back in the office and you need to pull the changes you made the day before on the feature branch. Trying to `pull` only results in merge conflicts that you don't want to solve, because you just want what's on the server!

There are two options:

* The lame way: delete the branch and check it out again
* The pro way: `git reset --hard origin/branch_name`

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
