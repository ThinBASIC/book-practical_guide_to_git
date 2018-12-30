## Remote

Pointer to the remote repository on the server.

### Why is it good?

Linking your local Git repository with remote allows you to:
- backup your source code on the server
- continue work on the same project from any PC with access to the server
- share your work with others

For the purpose of this book, the remote repository will be a repository on the GitHub.

This will allow you to work on the same project from any PC with an Internet connection.

### One or many?

Remote repository and remote are two different terms.

Typically, for your private projects, you will have one remote, called always `origin`, does not matter how the remote repository is really named.

Should you work on [fork](./fork.md) of an existing project, you will have two remotes:
- `origin`, which is your remote forked version
- `upstream`, which is the original repository from which you forked
