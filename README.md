# Some basic git setup commands

git --version

git config --global user.name "Brian Gramling"

git config --global user.email "bcgramling@gmail.com"

git config --list

# Setting up git repo

git init (from folder)

git remote add origin https://github.com/bgramling/gitlearn

git remote set-url origin https://github.com/bgramling/gitlearn (changed)

# Pushing to repo

git status

git add .

git commit -m 'Test Commit'

git push origin master

# Changes

git diff

git log

# Permanently authenticating with Git Repos

git config credential.helper store

git push https://github.com/bgramling/gitlearn.git

cache expire (seconds)
git config --global credential.helper "cache --timeout 7200"

# Reverting changes

git checkout -- .  (uncommitted)

git revert commit-num (committed)
-- can get from git log

git reset --hard (resetting changes)


# Branching

git branch

git branch test-branch

git checkout -b test-branch (create and make active)

git merge test-branch (merge branch in current active branch)

git push origin test-branch


# Deleting Branch

git branch -d test-branch (delete branch)

git branch -D test-branch (delete from local, useful if have unmerged)

git push origin :test-branch (delete from remote)


# Checkout remote branch

git fetch & git checkout xyz


# Ignoring files

.gitignore

# Stashing

git stash save "stash name"

git stash list

git stash apply {unique_id}
-- example git stash apply stash@{0}

git stash drop {unique_id}

git stash pop

git stash clear
