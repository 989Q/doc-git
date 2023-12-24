## Deleting Commits in Git

### Way 1: Removing the Last Commit

If you want to delete the last commit from the branch, follow these steps:

```bash
# Step 1: Roll back the last commit
git reset --hard HEAD~1

# Step 2: Force push the changes to the remote repository
git push origin HEAD --force
```

For more details, check [Stack Overflow](https://stackoverflow.com/questions/1338728/delete-commits-from-a-branch-in-git)

### Way 2: Deleting a Specific Commit

If you need to delete a specific commit identified by its commit ID (SHA-1 hash), use the following steps:

```bash
# Step 1: Roll back to the commit before the target commit
git reset --hard HEAD~1

# Step 2: Roll back to the specific commit ID
git reset --hard <sha1-commit-id>

# Step 3: Force push the changes to the remote repository
git push origin HEAD --force
```

For more details, check [Stack Overflow](https://stackoverflow.com/questions/1338728/how-do-i-delete-a-commit-from-a-branch)



## Github Token 

### Problem: Support for Password Authentication Removed

GitHub has deprecated password authentication, and it's necessary to use a personal access token for authentication instead. If you encounter the following error:

> Support for password authentication was removed on August 13, 2021. Please use a personal access token instead

### Solution 1: Updating Git Remote URL

Run the following command, replacing `<githubtoken>`, `<username>`, and `<repositoryname>` with your GitHub token, username, and repository name:

```bash
git remote set-url origin https://<githubtoken>@github.com/<username>/<repositoryname>.git
```

For more details, refer to the guide: [Fix Password Authentication on GitHub](https://levelup.gitconnected.com/fix-password-authentication-github-3395e579ce74)

### Solution 2: Using Personal Access Token (Linux)

Support for password authentication was removed Github Fixed using Token (August 13, 2021) - Linux

[Watch the video tutorial](https://www.youtube.com/watch?v=ytSoabxSQ6E)



## Git submodule 

### Problem: "does not have a commit checked out" Error

If you encounter the error message "error: 'part-one/' does not have a commit checked out" and "fatal: adding files failed" while working with Git submodules, you can resolve it using the following steps:

### Solution 1: Check for .git Folder in Submodule

In some cases, the presence of a `.git` folder within the submodule directory can cause issues. To resolve this:

1. Navigate to the submodule directory (`part-one`/ in this case).
2. Check if there is a `.git` folder.
3. If found, delete the `.git` folder.

This can be done using the following commands:

```bash
cd part-one/
rm -rf .git
```

### Solution 2: Use Git Shell to Remove .git Folder

Alternatively, you can use the Git Shell to remove the `.git` folder. Run the following command in Git Shell:

```bash
rm -rf .git
```

This command recursively removes the `.git` folder, which may be causing conflicts during submodule addition.

For more details, you can refer to the discussion on [Stack Overflow](https://stackoverflow.com/questions/12940626/github-error-message-permission-denied-publickey)



## Connecting github to vscode 

### Solution: Use HTTPS URL Instead of SSH

If you are facing the "Permission denied (publickey)" error while trying to connect GitHub to Visual Studio Code and are using SSH for authentication, here's how you can resolve it:

### Additional Information

GitHub has a help page specifically for the "Permission denied (publickey)" error. You can refer to it for more detailed information and troubleshooting steps. The page provides comprehensive guidance on resolving authentication issues.

[GitHub Help - Error: Permission denied (publickey)](https://stackoverflow.com/questions/12940626/github-error-message-permission-denied-publickey)

By following these steps and using the HTTPS URL, you should be able to connect Visual Studio Code to GitHub without encountering the "Permission denied (publickey)" error.
