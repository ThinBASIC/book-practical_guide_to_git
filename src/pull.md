## Pull

The process of getting changes from your [remote](./remote.md) repository to the local one.

### Example

Imagine you have 1 local and 1 remote repository, both with `[master]` on initial commit.

Then, somebody updates the remote repository with `[feature1]` branch.

In order to retrieve the branch, you first need to make your local repository aware of the branch via fetch:
```

                                               o "New feature 1"  [feature1]
                                               |
o "Initial commit" [master][origin/master]     o "Initial commit" [master]
(local)                                        (origin)

```

Then you pull the `[feature1]` branch to your local repository:
```

o "New feature 1"  [feature1][origin/feature1] o "New feature 1"  [feature1]
                                               |
o "Initial commit" [master][origin/master]     o "Initial commit" [master]
(local)                                        (origin)

```

> Always fetch before you pull!
