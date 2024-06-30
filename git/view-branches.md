# How to View All Branches in Git

To view all branches in Git, you can use the `git branch` command, which displays a list of all branches in the current repository you are working on. There are three main forms of this command:

### View All Local Branches
```bash
git branch
```
This command will list all local branches and will have an asterisk (`*`) next to the branch you are currently on.

### View All Remote Branches
```bash
git branch -r
```
This command will list all remote branches.

### View All Branches (Local and Remote)
```bash
git branch -a
```
This command will list all branches, both local and remote.

### Usage Example:
```bash
$ git branch -a
* main
  feature-branch
  remotes/origin/main
  remotes/origin/feature-branch
```
In this example, you can see that there are `main` and `feature-branch` branches locally, and `remotes/origin/main` and `remotes/origin/feature-branch` branches remotely.

You can use these commands to easily view and manage different branches in Git.
