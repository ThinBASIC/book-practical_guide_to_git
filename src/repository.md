## Repository

Git repository is a directory, containing your project or its subpart.

### Scope

A repository should be used for a single project, or better, its smallest functional part.

To give a specific example - thinBasic consists of an interpreter, many modules, thinAir integrated development environment, and help file.

While one could be tempted to have it all in a single repository, it would have the following issues:
- the repository size would grow bigger at a faster pace compared to separate repositories
- when you would need to revert a change in the interpreter, you would go back in time also for other components

In this particular case, the project should be split into multiple repositories this way:
- interpreter
- one repository for each module
- thinAir
- help file

### System files
Compared to a standard system directory, a repository contains:
- hidden `.git` directory, which is created by Git and contains the history of changes of your project
- git configuration files, if needed

A repository should also contain readme, license and adhere to some normalized structure. This will be discussed in the practical part.

### Technical restrictions
The Git repositories are optimized to work with text data, which makes them **ideal for storing source code**. Git allows to display changes between any two revisions of text data and store the history of changes efficiently.

While it is technically possible to add **binary files** to the repository, such as EXE/DLL files, PDF documents, and other common file formats, please be aware of the fact that this **might significantly increase the size of your repository**. The history of text files is stored via difference between two versions, however, each change in the binary file is stored as a new copy.
