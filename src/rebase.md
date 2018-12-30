## Rebase

The act of changing the base commit.

### Example

Let's return to our example from [Merge](./merge.md) chapter.

There were `master`, `feature1` and `feature2` branches originally, then `feature1` got modified and then merged to `master`, making the whole situation look like this::
```

o "New feature 1"  [master] [feature1]
|
o "Initial commit" [feature2]

```

Imagine we now add some new functionality to `feature2`:
```

o "New feature 1"  [master] [feature1]
|
| o "New feature 2" [feature2]
|/
o "Initial commit"

```

You can see the `feature2` branch is no longer at the "Initial commit", but it created a true separate branch in the commit tree.

So far so good, but you might notice the `feature2` no longer contains the changes from the updated `master`, which is now on the _New feature 1_ commit.

How to make `feature2` contain the current `master` code + the changes in _New feature 2_ commit?

The answer is, to _rebase_ the `feature2` on the current `master`. That is the same as rebasing `feature2` on the _New feature1_ commit, by the way.

After the rebase on `master`, the commit tree looks like this:
```

o "New feature 2"  [feature2]
|
o "New feature 1"  [master] [feature1]
|
o "Initial commit"

```

Looking at the commit tree, we can see it is linear sequence again, with _"Initial commit"_ being first, _"New feature 1"_ second and _"New feature 2"_ the last commit.

The code at the _"New feature 2"_ contains the cumulative contents of the two previous commits, and it is ready to be merged to `master`.

> If we would try to merge `feature2` without rebase, we would revert changes in `master`!
