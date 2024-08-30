# Git Operations: Merging and Unmerging

## Git Merge: Combining Changes from One Branch to Another

Merging in Git allows you to integrate changes from one branch into another. This is commonly used in collaborative projects to combine features or updates from different developers. 

### Steps to Merge Changes from One Branch to Another

1. **Switch to the Target Branch**

   Before merging changes, ensure that you are on the target branch where you want the changes to be applied. For example, if `dev-2` is the target branch, switch to it using:

   ```bash
   git checkout dev-2
   ```

2. **Merge Changes from the Source Branch**

   Once on the target branch (`dev-2`), merge changes from the source branch (`dev-1`) by running:

   ```bash
   git merge dev-1
   ```

   This command integrates all the commits from `dev-1` into `dev-2`.

3. **Resolve Merge Conflicts (if any)**

   If there are any conflicts between the branches, Git will prompt you to resolve them. Open the conflicting files, make the necessary changes, and then add the resolved files using:

   ```bash
   git add <file-name>
   ```

   After resolving all conflicts, complete the merge with:

   ```bash
   git commit
   ```

### Important Notes

- **Always review** the changes before merging to ensure you understand what modifications are being integrated.
- **Create a backup** of your branches before merging, especially if the branches contain critical or complex changes.

## Git Unmerge: Reverting a Merge Operation

Sometimes, a merge may introduce issues, or you might realize that the merge was done prematurely. Git provides ways to undo a merge depending on whether the merge has been committed.

### How to Undo a Git Merge

1. **If the Merge Has Not Been Committed**

   If you realize the merge was not what you wanted before making a commit, you can abort the merge with:

   ```bash
   git merge --abort
   ```

   This command will stop the merge process and return your branch to its pre-merge state.

2. **If the Merge Has Been Committed**

   If the merge has already been committed, and you want to undo it, use:

   ```bash
   git reset --hard HEAD~1
   ```

   This command will revert your branch to the state it was in before the merge commit. **Warning:** This will also discard all changes made after the merge. Ensure that this is what you want, as it will permanently delete any changes that are not committed.

### Considerations

- **Use `git reset --hard` with caution**: This operation will lose all uncommitted changes. It is advisable to use `git stash` to temporarily save changes that you don’t want to lose.
- **Verify your branch state**: After an unmerge, ensure that your branch is in the desired state by reviewing the commit history using:

   ```bash
   git log
   ```

## Additional Resources

- [Git Merge Documentation](https://git-scm.com/docs/git-merge)
- [Git Reset Documentation](https://git-scm.com/docs/git-reset)
- [Stack Overflow: How to Unmerge a Git Merge](https://stackoverflow.com/questions/28932515/how-to-unmerge-a-git-merge)
