# Conflict Resolution

Conflict resolution can be a huge pain in the butt. It is extremely important to know how to do this manually, i.e.: Opening your favorite text editor, and manualling fixing the conflicts denoted by the conflict markers.

Note: Always make sure you have 0 uncommitted changes before attempting a merge, rebase, or pull. You can easily utilize `git stash` to temporarily store tracked changes.

## Automatically choosing which set of changes to keep:

`git checkout --ours file/path.ext`
`git checkout --theirs file/path.ext`

## Understanding Conflict Markers

### 2-way merge
```
<<<<<<< HEAD
This is the change from your local copy of the branch.
This is denoted by either "HEAD" or your specific commit message.
Another way to think of this is the branch you are merging *into*
=======
This is the change from the commit you tried to merge.
The number here is the commit hash.
>>>>>>> 461d08fd2677e893db8f7168763e364ac1971239
```

### 3-way merge

```
<<<<<<< HEAD
This is the change from your local copy of the branch.
This is denoted by either "HEAD" or your specific commit message.
Another way to think of this is the branch you are merging *into*
||||||| merged common ancestors
This text / code here is the state that was before either you or the commit/branch you tried to change it.
=======
This is the change from the commit you tried to merge.
The number here is the commit hash.
>>>>>>> 461d08fd2677e893db8f7168763e364ac1971239
```

## Changing the Merge Conflict Style

### Default

`git config --global merge.conflictstyle merge`

### 3-Way Merge

`git config --global merge.conflictstyle diff3`

This shows the original text before both your and their changes.


## Aborting

If you are simply merging
`git merge --abort`

`git reset --hard HEAD` This will reset your working directory to the commit `HEAD` is pointing to.

If you are rebasing
`git rebase --abort`
