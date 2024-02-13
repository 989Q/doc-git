# Deleting Commits in Git

## Easy Way to Undo Commits

### Short Command

```bash
git reset --hard HEAD~1
git push -f 
```

### Example Usage

```bash
git reset --hard HEAD~1
git push -f <remote> <branch>
```
Replace `<remote>` and `<branch>` with your desired remote and branch names, respectively. For instance: `git push -f origin bugfix/bug123`.

This command sequence undoes the last commit and updates the remote history. The `-f` flag is necessary to overwrite the upstream history in the remote repository.

For more information, refer to [stackoverflow.com/questions/6459080](https://stackoverflow.com/questions/6459080/how-can-i-undo-a-git-commit-locally-and-on-a-remote-after-git-push).

## Deleting Commits: Two Methods

### Method 1: Removing the Last Commit

If you want to delete the last commit from the branch, follow these steps:

```bash
# Step 1: Roll back the last commit
git reset --hard HEAD~1

# Step 2: Force push the changes to the remote repository
git push origin HEAD --force
```

For more details, check [stackoverflow.com/questions/1338728](https://stackoverflow.com/questions/1338728/delete-commits-from-a-branch-in-git).

### Method 2: Deleting a Specific Commit

If you need to delete a specific commit identified by its commit ID (SHA-1 hash), use the following steps:

```bash
# Step 1: Roll back to the commit before the target commit
git reset --hard HEAD~1

# Step 2: Roll back to the specific commit ID
git reset --hard <sha1-commit-id>

# Step 3: Force push the changes to the remote repository
git push origin HEAD --force
```

For more details, check [stackoverflow.com/questions/1338728](https://stackoverflow.com/questions/1338728/how-do-i-delete-a-commit-from-a-branch).
