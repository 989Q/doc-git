# Deleted but Can't Create New Branch

## Issue Description

After deleting a branch named `deploy` from the remote repository using:

```bash
git push origin --delete deploy
```

You attempted to create a new branch with the same name:

```bash
git checkout -b 'deploy'
```

However, you encountered the following error:

```
fatal: a branch named 'deploy' already exists
```

## Cause

The error occurs because the `deploy` branch still exists in your local repository. While the branch was successfully deleted from the remote repository, it remains in your local environment.

## Solution

To resolve this issue, you need to delete the `deploy` branch locally before creating a new one with the same name:

1. Delete the local `deploy` branch:

   ```bash
   git branch -d deploy
   ```

   If the branch has changes that haven't been merged, use the `-D` flag to force deletion:

   ```bash
   git branch -D deploy
   ```

2. After deleting the local branch, create a new branch named `deploy`:

   ```bash
   git checkout -b deploy
   ```

By following these steps, you can successfully create a new branch named `deploy`.
