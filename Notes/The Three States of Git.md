# The Three States of Git

[[Git]] has three states that any file can be in: modified, staged, and committed. 

- **Modified.** The file has changes but have not been committed to the database yet. 
- **Staged.** A modified file has been marked in its current version to be included in the next commit snapshot. This gives rise to the concept of staging area.
- **Commited.** A file's contents is safely stored in the local database.

```
    Working Directory      Staging Area     Git directory
           |                    |                |
           |                    |                |
           |         Checkout the project        |
           |<-------------------|----------------|
           |                    |                |
           |    Stage fixes     |                |
           |------------------->|                |
           |                    |                |
           |                    |      Commit    |
           |                    |--------------->|
           |                    |                |
```

- **Working Directory.** This is a single checkout[^single-checkout] of one version of the project, where files are pulled from the compressed database in the `.git` directory, and placed in the disk for in order to be used or modified.
- **Staging Area.** This is a file, usually in the `.git` directory, that stores information about what will go into the next commit. Technically, it's called the "index". 
- **Git Directory.** This is wher [[Git]] stores the metadata and object database for a particular project. It's the most important part of Git, and it's what it's copied when you clone a repository from another computer.

There are different [[Git Workflows]] but the basic one goes like this:

1. Modify files in the working tree.
2. Selectively stage only those changes you want as part of your next commit; only these changes are added to the staging area.
3. Do a commit, which takes the files as they're in the staging area and stores that snapshot permanently in the Git repository.

[^single-checkout]: A single checkout is one commit that's being checked out.

Tags: #literature