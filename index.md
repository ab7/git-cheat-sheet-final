# Git Cheatsheet

Documentation - [https://git-scm.com/](https://git-scm.com/)

## Configuration

```
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
git config --global core.editor vim
git config --list
```

[https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup)

## Creating a local repository

```
git init .           # initialize an empty repository
git clone <address>  # download a repo from a remote repository
git status           # check the current status of repo
```

[https://git-scm.com/docs/git-init](https://git-scm.com/docs/git-init)

## Commits

```
git diff                            # view changes against previous commit
git add .                           # stage files to be included in commit
git add <file>|<dir>                # stage specific file/dir
git commit                          # using editor saved from config
git commit -m “This is an message”  # skip the editor
git commit --amend                  # update most recent commit
```

[https://git-scm.com/docs/git-commit](https://git-scm.com/docs/git-commit)

## Commit management

```
git reset                         # unstage changes ready for commit
git reset head~N                  # undo N most recent commits
git reset --hard origin <branch>  # reset local branch to remote
git checkout <file>               # throw away changes
git stash                         # stash current changes
git stash apply                   # apply the most recent stash
git stash list                    # list currently stashed changes
git stash apply stash@{N}         # apply stash at index N
git log                           # list commits
```

[https://git-scm.com/docs/git-reset](https://git-scm.com/docs/git-reset) & [https://git-scm.com/docs/git-stash](https://git-scm.com/docs/git-stash)

## Branches

```
git checkout -b awesome-feature  # create new branch
git branch                       # lists all branches
git branch -d awesome-feature    # delete branch without changes
git branch -D awesome-feature    # force delete branch
```

[https://git-scm.com/docs/git-branch](https://git-scm.com/docs/git-branch)

## Merging

```
git merge <branch>  # merge another branch into your current branch
```

[https://git-scm.com/docs/git-merge](https://git-scm.com/docs/git-merge)

## Rebasing

```
git rebase -i <branch>  # move commits in branch to top of <branch>
git rebase -i head~N    # modify N previous commits
```

[https://git-scm.com/docs/git-rebase](https://git-scm.com/docs/git-rebase)

## Merge conflicts

```
git merge|rebase --continue  # run after resolving conflicts
git merge|rebase --abort     # cancel merge|rebase
```

[https://git-scm.com/docs/git-merge](https://git-scm.com/docs/git-merge)

## Remotes

```
git remote add origin <remote-address>      # add a remote called origin
git push -u origin master                   # push master to remote repo
git remote -v                               # list current remotes
git remote set-url origin <remote-address>  # change remote address
```

[https://git-scm.com/docs/git-remote](https://git-scm.com/docs/git-remote)

