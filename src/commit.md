## Commit

A single set of changes.

### What can it contain?

A single commit might contain addition and/or modification and/or removal of files.

### How does it work?

Imagine a repository with two commits:
- the first commit adds files `a.txt` and `b.txt`.
- the second commit removes file `a.txt`, modifies `b.txt` and adds `c.txt`.

The repository now contains modified `b.txt` and `c.txt`. If you want, you can go back in time to the first commit - anytime. And without losing the ability to travel back to the last commit again.

Time travel is made possible thanks to the `.git` directory, which contains the history of changes in an efficient format.

### How can I reference specific commit?

Each commit has so-called commit hash. It is unique across the repository.

Each commit has also a commit message, which is a brief summary of changes specified by you.

Commit messages are referenced in this book like: _"Commit message"_
