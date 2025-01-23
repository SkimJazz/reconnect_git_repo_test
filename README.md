# reconnecting to GitHub

Developers commonly use the terminal command `rm -rf .git` to remove the git repository from a project on local. This is useful when you want to minimize the Git conflicts or when you want to start a new repository. However, if you want to reconnect to the same repository, after removing the `.git` folder, you can follow the steps below. This will help you to reconnect to the same repository that you clone the first time.


## Steps to reconnect to a GitHub repository

1. Clone the repository again using the `git clone` command. This will create a new `.git` folder in your project directory.

```bash
git clone <repository-url>
```

2. Change the directory to the project directory.

```bash
cd <project-directory>
```

3. Check the remote repository URL using the `git remote -v` command.

```bash
git remote -v
```

4. If the remote repository URL is different from the original repository, you can change it using the `git remote set-url` command.

```bash
git remote set-url origin <repository-url>
```

5. Verify the remote repository URL using the `git remote -v` command.

```bash
git remote -v
```

6. Now you can push your changes to the repository using the `git push` command.

```bash
git push origin master
```

## Alternative method

If you want to reconnect to the same repository without cloning it again, you can follow the steps below.

1. Remove the `.git` folder from your project directory.

```bash
rm -rf .git
```

2. Initialize a new git repository in your project directory.

```bash
git init
```

3. Add the remote repository URL using the `git remote add origin` command.

> Note that you can use the SSH or HTTPS URL of the repository. If using the SSH URL
> after entering the `git fetch origin` command, you may need to enter your GitHub 
> passphrase. for the Key.


```bash
git remote add origin <repository-url>
```

4. Fetch the changes from the remote repository using the `git fetch` command.

```bash
git fetch origin
```

5. Reset the local repository to match the remote repository using the `git reset --hard` command.

```bash
git reset --hard origin/main
```

6. Now you can push your changes to the repository using the `git push` command.

```bash
git push origin main
```

