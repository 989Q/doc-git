# Changing Git Username in Terminal

For more information, refer to [stackoverflow.com/questions/22844806](https://stackoverflow.com/questions/22844806/how-to-change-my-git-username-in-terminal).

## 1. Navigate to Your Repository

Open your terminal and navigate to the repository where you want to change the Git username.

## 2. Check Current Configuration

Execute the following command to check your current Git username and email configuration:

```bash
git config --list
```

This will display your current username and email associated with the local repository.

## 3. Change Username and Email

To change your Git username and email, use the following commands:

### Global Change (Applied to All Repositories)

```bash
git config --global user.name "Your Full Name"
git config --global user.email "your_email@example.com"
```

Replace `"Your Full Name"` with your desired full name and `"your_email@example.com"` with your desired email address.

### Local Repository Specific Change

For changing the username and email for a specific local repository, navigate to the repository and use the same commands without the `--global` flag. This will only affect the current repository:

```bash
git config user.name "Your Full Name"
git config user.email "your_email@example.com"
```

## 4. Manual Configuration (Per Repository Basis)

Alternatively, you can manually edit the `.git/config` file in the repository. Open the file using a text editor and update the `user.name` and `user.email` fields with your desired values.

```bash
nano .git/config
```

Make sure to save your changes after editing the file.
