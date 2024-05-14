## Merging Changes from One Branch to Another

To seamlessly integrate changes from one branch into another in your Git repository, follow these steps:

### 1. Switch to the Target Branch

Before merging the changes, ensure you are on the target branch (`dev-2`). If you're not already on `dev-2`, switch to it using the following command:

```bash
git checkout dev-2
```

### 2. Merge Changes

Once you're on the target branch (`dev-2`), merge the changes from the source branch (`dev-1`) using the merge command:

```bash
git merge dev-1
```

## How to Unmerge a Git Merge?

In case you need to undo a merge, follow the steps outlined in [this Stack Overflow thread](https://stackoverflow.com/questions/28932515/how-to-unmerge-a-git-merge)

```bash
git reset --merge HEAD~1
```

### Note:

- If you're already on the target branch (`dev-2`), you can directly execute the merge command without switching branches.
- It's recommended to review any merge conflicts that may arise during the merge process and resolve them before finalizing the merge.
