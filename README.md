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

