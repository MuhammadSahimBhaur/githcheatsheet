# Setup

```bash
git config --global user.name "<NAME GOES HERE>"
git congif --global user.email "<EMAIL GOES HERE>"
```

```bash
git innit
```

Add all the files into the staging environment

```bash
git add <FILENAME GOES HERE>
# or
git .
# then
git commit -m "<MESSAGE GOES HERE>"
```
# Terminologies
## Git Environments

- Wokring
- Staging
- Commit

## Possible File States
- Tracked
  - Unmodified
  - Modified
  - Staging
- Untracked

## File states
We can check file states using

```git
 git status
```

`git status ` will give you an output like this
```bash
On branch main
Changes not staged for commit:
  (use "git add <file>..." to update what will be committed)
  (use "git restore <file>..." to discard changes in working directory)
        modified:   Question6.html

no changes added to commit (use "git add" and/or "git commit -a")
```

# Deleting, Restoring and Renaming

To delete
`git rm <FILENAME GOES HERE>`

To restore
`git restore .`

Renaming
`git mv <OLDFILENAME> <NEWFILENAME>`

# Changing History

Can change ONLY the last commit
`git commit --amend`

## Rebasing – Change the history with the git time machine

`git rebase -i --root`

OR

`git rebase -i HEAD~3`

> The `HEAD~3` means the 3 commits behind the current commit the head pointer is pointing to.


# Branches

Create a branch
`git switch -c <NAME OF BRANCH>`

## Branch merging
1. Go to root branch
`git switch main`
2. Show all branches
`git branch`
> add the flag `-a` to view all remote branches as well.
3. Merge the named branch with the current branch
`git merge <BRANCH NAME>`

# Git Stash

`git stash`

`git stash list`

`git stash apply <NUMBER OF STASH>`

`git stash pop`

# Git Clean

Used to remove all untracked files
`git clean`
Dry run
> `-n or --dry-run`

Remove directories
> `-d`


# Github

## Push

First we need to add remotes.

A common practice is to name the remote, "origin".

`git remote add <NAME> <URL>`

> `git remote remove NAME`
> 
> `git rename <OLDNAME> <NEWNAME>`
> 
> `git remote -v`

# Git Push

This will push all branches to remote.

`git push -all`

The following command will only push the specified branch to remote.

`git push -u <REMOTE; i.e. origin> <BRANCH; i.e. main>`

We can pull in changes using

`git pull origin`






