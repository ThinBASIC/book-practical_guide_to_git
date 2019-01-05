## Push

The process of moving changes from your local repository to [remote](./remote.md) repository.

### Example

Imagine you have 1 local repository with 1 [remote](/remote.md) repository, referenced as `origin`.

Both the local repository contains the "Initial commit" in the `[master]` branch.
```

o "Initial commit" [master][origin/master]    o "Initial commit" [master]
(local)                                       (origin)

```

On the left, you can see the local repository with local `[master]` branch, while the local repository is aware of the fact there is a master in origin as well.

Then, you create a new feature branch on the local repository, and commit some code into it:
```

o "New feature 1"  [feature1]
|
o "Initial commit" [master][origin/master]    o "Initial commit" [master]
(local)                                       (origin)

```

You can see the local repository changed, but the remote repository didn't.

How to sync them?

You need to *push* the `feature1` branch to the remote.
```

o "New feature 1"  [feature1][origin/feature1] o "New feature 1"  [feature1]
|                                              |
o "Initial commit" [master][origin/master]     o "Initial commit" [master]
(local)                                        (origin)

```

 After the push, both repositories are in sync for the given branch.
 