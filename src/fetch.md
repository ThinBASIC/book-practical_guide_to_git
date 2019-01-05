## Fetch

The operation to make your Git aware of the changes in the *remote* repository.

### Example

Imagine you have 1 local repository with 1 [remote](/remote.md) repository, referenced as `origin`.

Both the local repository contains the _"Initial commit"_ in the `[master]` branch.
```

o "Initial commit" [master][origin/master]    o "Initial commit" [master]
(local)                                       (origin)

```

Then, some other collaborator updates the remote repository:
```

o "Initial commit" [master]                    o "Initial commit" [master]
(local)                                        (origin)

```

What? What change?

If you would like to *see* the change, you first need to make your Git aware of changes in the remote repository.

How to do it?

Fetch!

```

                                               o "New feature 1"  [feature1]
                                               |
o "Initial commit" [master][origin/master]     o "Initial commit" [master]
(local)                                        (origin)

```
Once you do this, you have an idea about what was the state of the remote repository at the time of fetch:

> Please note fetching does not update your local repository with the remote changes. You have to [pull](./pull.md) to sync!
