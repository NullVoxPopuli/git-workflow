# Undoing

Note that where `master` is used, any branch name could be used.

## Revert a file that was accidentally changed in a branch

`git checkout master -- path/to/file.ext`

## Revert to the remote copy

`git reset origin/master --hard`
