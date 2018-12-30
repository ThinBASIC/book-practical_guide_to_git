## Merge

The act of promotion of changes by merging them with the existing state.

### Example

Imagine you have `master` branch and two branches `feature1` and `feature2`.

Both branches were created from `master` at the same time and do not contain any changes yet.

Because branch is basically a pointer to commit, the initial state looks like this:
```

o "Initial commit" [master] [feature1] [feature2]

```

Then you commit some changes to `feature1`:
```

o "New feature 1"  [feature 1]
|                  
o "Initial commit" [master] [feature2]

```

Then you merge the changes from `feature1` to `master`, modifying the repository to this:
```

o "New feature 1"  [master] [feature1]
|
o "Initial commit" [feature2]

```
