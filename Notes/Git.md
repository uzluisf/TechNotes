# Git

Git is a [[Version Control System]] 

It was created as an [[Open Source]] alternative to [[BitKeeper]] by [[Linus Torvalds]] and the Linux development community. Some of the goals of this new system were:
- Speed
- Simple design 
- Support for [[Non-linear Development]]
- Fully distributed
- Efficient while handling large projects

## Git in a Nutshell

Git thinks about data differently to what other [[Version Control System]]s do. Instead of storing information as a list of file-based changes[^delta], Git thinks of its data as series of snapshots of a miniature filesystem. 

In other words, every time you commit, Git basically takes a picture of what all the files look at that moment and stores a reference to that snapshot. Thus, *each commit is a link to a snapshot of the files and their changes at a specific moment in time*.

In Git nearly every operation is local, i.e., you've the entire history of the project in your local disk and thus Git doesn't have any network latency overhead like other [[Version Control System]]s, especifically CVCSs. For example, to browse the history of a project Git simply reads it directly from the local database instead of requesting it from a server.

Furthermore, Git ensures [[Data Integrity]], i.e., everything in Git is checksummed before it's stored and then referred solely by that [[Checksum]], meaning that Git doesn't store files/directories in its database by the filename but the hash of its contents. A side effect of this is  you cannot change the contents of any file without Git knowing about it. 

In order to compute the [[Checksum]] of a file, Git uses a [[Cryptographic Function]] known as SHA-1 which produces a 40-character string of hexadecimal characters. This string is known as a SHA-1 hash, and computed based on the contents of a file or a directory structure. A SHA-1 hash[^sha1sum] looks as follows:

```
d680157068351851166eef414acc471bf2c36223
```

Another important aspect of Git is that it generally only adds data, which means it's difficult to do anything that cannot be reverted. Thus we can experiment without the danger of screwing things up. 

[^delta]: This is known as *delta-based* version control.
[^sha1sum]: In [[Linux]], you can use the `sha1sum` in the [[Command Line Interface]] to get a file's sha1 hash.

Tags: #permanent 