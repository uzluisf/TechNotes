# Version Control System

A **Version Control System** (VCS) is a system that records changes to a collection of files over time. Each set of changes is versioned, so you can return to specific versions later on.

 Among the things a VCS allows you are:
* Revert a specific file to a previous state.
* Revert a whole project to a previous state.
* Compare changes over time.
* See who introduced changes that caused problems, and when they did.

There are different types of VCSs depending on how the versioned data is kept: local, centralized, or distributed. 

## Local Version Control Systems (LVCSs)

A **Local Version Control System** is a VCS with a simple and local database that keeps all changes to files under revision control. *All the information is kept local*, and aside from the author nobody else has access to it unless it's shared.

An example of this type of VCS is **Revision Control System** ([RCS](https://en.wikipedia.org/wiki/Revision_Control_System)), where a set of patches[^patch] in a special format are kept in the disk; it can recreate what a file looked like at any point in time by adding up all the patches. 

## Centralized Version Control Systems (CVCSs)

A **Centralized Version Control System** is a VCS where all versioned files are kept in a single server, and a number of clients that check out files from that central place. This allows for collaboration among developers.

Advantages of these systems are:
* Everyone knows what everyone else on the project is doing,
* Administrators have fine-grained control over what everyone else does,
* It's easier to administer a CVS than dealing with local databases on every client.

Among its disadvantages are:
* There's a single server, which represents a *single point of failure* (e.g., 1) if server goes down, nobody can collaborate, 2) if disk the server is on gets corrupted, all data is lost unless it's been backup, etc).

Examples of these systems are [CVS](https://www.nongnu.org/cvs/), [Subversion](https://subversion.apache.org/), and [Perforce](https://www.perforce.com/products/helix-core). 

## Distributed Version Control Systems (DVCSs)

A **Distributed Version Control System** is VCS where all clients both check the latest snapshot of the files and fully mirror the server's repository's whole full history. The main advantage of this is that if the server dies, any of the client repositories can be copied back up to the server and restore it.

In a DVCS, every clone is a full backup of all the data. 

Examples of these systems are [[Git]], [Mercurial](https://www.mercurial-scm.org/), [Bazaar](http://bazaar.canonical.com/en/), or [Darcs](http://darcs.net/).


[^patch]: A patch is the difference between two files with the same name. 

Tags: #permanent
