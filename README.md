## Delete commits 

### Delete commits from a branch in Git
- https://stackoverflow.com/questions/1338728/delete-commits-from-a-branch-in-git

```git
git reset --hard HEAD~1
```

```git
git push origin HEAD --force 
```



## Github Token 

### Solve problem 
Support for password authentication was removed on August 13, 2021. Please use a personal access token instead

### Document
How to fix support for password authentication was removed on GitHub
- https://levelup.gitconnected.com/fix-password-authentication-github-3395e579ce74

```
git remote set-url origin https://<githubtoken>@github.com/<username>/<repositoryname>.git
```

### New acc token
- https://www.youtube.com/watch?v=ytSoabxSQ6E
Support for password authentication was removed Github Fixed using Token (August 13, 2021) - Linux



## Git submodule 

### Solve problem 
error: 'part-one/' does not have a commit checked out </br>
fatal: adding files failed

### git submodule add error: does not have a commit checked out
- https://stackoverflow.com/questions/12940626/github-error-message-permission-denied-publickey

In my case subfolder is containing .git folder. </br>
Check if any subfolder contains '.git' folder. Delete that ".git" folder and it will work. </br>
OR another way is </br>
In git-shell Run </br>
```
rm -rf .git
```



## Github connect vscode

### Solve problem 
git@github.com: Permission denied (publickey). fatal: Could not read from remote repository.
```
!!! use commit and push on vscode for authentication to github
```

### GitHub Error Message - Permission denied (publickey)
- https://stackoverflow.com/questions/12940626/github-error-message-permission-denied-publickey
```
GitHub isn't able to authenticate you. So, either you aren't setup with an SSH key, because you haven't set one up on your machine, or your key isn't associated with your GitHub account.

You can also use the HTTPS URL instead of the SSH/git URL to avoid having to deal with SSH keys. This is GitHub's recommended method.

Further, GitHub has a help page specifically for that error message, and explains in more detail everything you could check.
```