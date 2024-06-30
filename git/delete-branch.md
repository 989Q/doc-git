# How to Delete a Recently Created Branch in Git

If you have just created a new branch using the command `git checkout -b <branch_name>` and want to delete that branch, you can use the `git branch -d <branch_name>` or `git branch -D <branch_name>` command, depending on the status of the branch. Here are the details:

## Delete a Recently Created Branch (Local Branch)

### Check the Current Branch:
Before deleting a branch, ensure that you are not currently on the branch you want to delete. You can check the current branch with the command:

```bash
git branch
```

### Switch to Another Branch:
If you are on the branch you want to delete, switch to another branch, such as `main`:

```bash
git checkout main
```

### Delete the Branch:
Use the command `git branch -d <branch_name>` to delete the recently created branch:

```bash
git branch -d <branch_name>
```

If the branch has not been merged into another branch, you can use the `git branch -D <branch_name>` command to force delete the branch:

```bash
git branch -D <branch_name>
```

## Example of Deleting a Recently Created Branch:
Suppose you have just created a branch named `feature-xyz`:

```bash
git checkout -b feature-xyz
```

If you want to delete this branch, follow these steps:

### Check the Current Branch:
```bash
git branch
```

### Switch to Another Branch if You Are on `feature-xyz`:
```bash
git checkout main
```

### Delete the `feature-xyz` Branch:
```bash
git branch -d feature-xyz
```

If the `feature-xyz` branch has not been merged and you want to force delete it:

```bash
git branch -D feature-xyz
```
