# Conflict Resolution

Conflict resolution can be a huge pain in the butt. It is extremely important to know how to do this manually, i.e.: Opening your favorite text editor, and manualling fixing the conflicts denoted by the conflict markers.

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
