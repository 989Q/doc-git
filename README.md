<!-- MAIN CONTENTS -->
### Delete commits from a branch in Git
https://stackoverflow.com/questions/1338728/delete-commits-from-a-branch-in-git

```git
git reset --hard HEAD~1
```

```git
git push origin HEAD --force 
```

### How to fix support for password authentication was removed on GitHub
https://levelup.gitconnected.com/fix-password-authentication-github-3395e579ce74

Support for password authentication was removed on August 13, 2021. Please use a personal access token instead
```
git remote set-url origin https://<githubtoken>@github.com/<username>/<repositoryname>.git
```
