# Renaming a Git Branch

This guide provides instructions for renaming a Git branch and updating the remote repository to reflect this change.

## Listing All Branches

To see a list of all branches in your repository, both local and remote, use the following command:

```bash
git branch -a
```

### Example Output

Running the `git branch -a` command might display something like the following:

```
* feature/google-tag-manager
  kurosos-devka
  main
  video-m3u8
  remotes/origin/feature/google-tag-manager
  remotes/origin/kurosos-devka
  remotes/origin/main
  remotes/origin/video-m3u8
```

> **Note:** The above branches are mock values for demonstration purposes.

## Steps to Rename a Branch

To rename the branch `video-m3u8` to `feature/video-m3u8`, follow these steps:

1. **Switch to the Branch to be Renamed**

   First, make sure you are on the branch you want to rename. Use the following command:

   ```bash
   git checkout video-m3u8
   ```

2. **Rename the Branch**

   Rename the current branch using:

   ```bash
   git branch -m feature/video-m3u8
   ```

3. **Update the Remote Repository**

   If you want to update the remote repository (such as GitHub or GitLab) with the new branch name, you will need to delete the old branch name and push the new branch name:

   ```bash
   git push origin --delete video-m3u8
   git push origin feature/video-m3u8
   ```

4. **Set the Upstream for the New Branch**

   Set the new branch to track the remote branch:

   ```bash
   git push --set-upstream origin feature/video-m3u8
   ```

By following these steps, you will successfully rename your branch and ensure the remote repository is up to date with this change.
