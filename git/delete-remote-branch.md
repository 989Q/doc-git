# How to Delete a Remote Branch in Git

To delete the remote branch `remotes/origin/dev-ninja`, you can use the `git push` command followed by `--delete` and the name of the branch you want to delete, as shown below:

```bash
git push origin --delete dev-ninja
```

## Explanation:

- `git push origin --delete dev-ninja` will delete the `dev-ninja` branch from the remote repository (origin).

After executing this command, the branch `remotes/origin/dev-ninja` will be removed from the remote repository.

## Example Branch List

Here is an example of a branch list that includes `remotes/origin/dev-ninja` and other `dev-user` branches with new names:

```bash
❯ git branch -a
* dev
  main
  remotes/origin/HEAD -> origin/main
  remotes/origin/brachdebug
  remotes/origin/dev
  remotes/origin/dev-alex
  remotes/origin/dev-bob
  remotes/origin/dev-ninja
  remotes/origin/dev-charlie
  remotes/origin/dev-dana
  remotes/origin/dev-erin
  remotes/origin/dev-frank
  remotes/origin/dev-grace
  remotes/origin/main
  remotes/origin/past-project
  remotes/origin/structure
(END)
```

By using the above command, you will remove the `dev-ninja` branch from the remote repository, cleaning up your remote branches and ensuring only relevant branches are kept.
