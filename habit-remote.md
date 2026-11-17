# Habit Tracker – Git Remote Assignment

## 1. Create a Local Git Repository

First, create a folder named `habit-tracker` and initialize it as a Git repository.

Commands:

```bash
mkdir habit-tracker
cd habit-tracker
git init
```

The `git init` command initializes a new Git repository and creates a hidden `.git` folder to store version history and repository information.

## 2. Create a GitHub Repository

A new GitHub repository named `habit-tracker` is created to store the project online.

Repository name: `habit-tracker`

GitHub repository URL:

```text
https://github.com/YOUR_GITHUB_USERNAME/habit-tracker.git
```

Replace `YOUR_GITHUB_USERNAME` with your actual GitHub username.

## 3. Connect the Local Repository to GitHub

Use the following command to connect the local repository to the GitHub repository:

```bash
git remote add origin https://github.com/YOUR_GITHUB_USERNAME/habit-tracker.git
```

Here:

- `git remote add` adds a remote repository.
- `origin` is the default name given to the remote repository.
- The URL points to the GitHub repository.

## 4. Verify the Remote Connection

Run the following command:

```bash
git remote -v
```

Expected output:

```text
origin  https://github.com/YOUR_GITHUB_USERNAME/habit-tracker.git (fetch)
origin  https://github.com/YOUR_GITHUB_USERNAME/habit-tracker.git (push)
```

The output confirms that the local repository is configured with a remote repository for fetching and pushing changes.

Note: The above output is an example. Replace the username with your actual GitHub username and paste your real terminal output after executing the command.

## 5. Why Is a Remote Repository Useful Even for a Solo Project?

A remote repository is useful even when only one developer is working on a project.

1. It provides an online backup of the project, reducing the risk of losing important work if the local computer fails.
2. It allows developers to access their project from different computers.
3. It makes it easy to track and share project changes.
4. It allows developers to restore previous versions of their work.
5. It provides a safe place to store project code and documentation.
6. It also makes future collaboration easier if other developers join the project.

Therefore, a remote repository is useful for maintaining project security, backup, version history, and accessibility.

## 6. Create an Assignment Branch

Create a separate branch for this assignment:

```bash
git switch -c assignment/habit-remote
```

This allows assignment-related work to be completed separately from the main branch.

## 7. Stage and Commit the Assignment

Add the assignment file:

```bash
git add habit-remote.md
```

Commit the changes with a clear commit message:

```bash
git commit -m "docs: explain Git remote setup"
```

## 8. Push the Branch to GitHub

Upload the assignment branch to GitHub:

```bash
git push -u origin assignment/habit-remote
```

This command pushes the local branch to GitHub and sets the upstream tracking branch.

## 9. Conclusion

Git remote repositories help developers keep their projects backed up, accessible, and organized.

Even for a solo project, GitHub provides a reliable way to store code online, maintain project history, and manage future development.

Connecting a local Git repository to GitHub using `git remote add origin` makes it easier to push and pull project changes.
