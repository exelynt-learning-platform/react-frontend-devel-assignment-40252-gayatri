# Publish a Daily Habit Tracker to GitHub

## 1. Create a Local Git Repository

First, create a project folder named `habit-tracker` and initialize Git.

Commands executed:

```bash
mkdir habit-tracker
cd habit-tracker
git init
```

Git initializes the repository and creates a hidden `.git` folder. This folder stores the project's version history and configuration.

## 2. Create a GitHub Repository

Created a new repository on GitHub with the following details:

- Repository name: habit-tracker
- Hosting platform: GitHub
- Visibility: Public or Private
- Repository URL: PASTE YOUR ACTUAL GITHUB REPOSITORY URL HERE

The GitHub repository provides online storage for the local project.

## 3. Connect the Local Repository to GitHub

Connected the local repository to GitHub using:

```bash
git remote add origin YOUR_ACTUAL_GITHUB_REPOSITORY_URL
```

The `origin` name identifies the remote repository.

## 4. Verify the Remote Connection

Executed:

```bash
git remote -v
```

### Actual terminal output

Paste the actual output from your terminal below:

```text
PASTE YOUR REAL GIT REMOTE -V OUTPUT HERE
```

The output should display the GitHub repository URL for both fetch and push.

## 5. Create an Assignment Branch

Created a separate branch for the assignment:

```bash
git switch -c assignment/habit-remote
```

This branch allows me to complete the assignment without directly changing the main branch.

## 6. Stage and Commit the Assignment

Added the Markdown file:

```bash
git add habit-remote.md
```

Committed the changes:

```bash
git commit -m "docs: complete habit tracker remote assignment"
```

## 7. Push the Assignment to GitHub

Executed:

```bash
git push -u origin assignment/habit-remote
```

### Actual push output

Paste the successful output from your terminal below:

```text
PASTE YOUR REAL GIT PUSH OUTPUT HERE
```

A successful push confirms that the local assignment branch has been uploaded to GitHub.

## 8. Why Is a Remote Repository Useful Even for a Solo Project?

A remote repository is useful even when only one developer is working on a project.

1. It provides an online backup of the project, reducing the risk of losing important work if the local computer fails.
2. It allows developers to access their project from different computers.
3. It makes it easy to track and share project changes.
4. It allows developers to restore previous versions of their work.
5. It provides a safe place to store project code and documentation.
6. It makes future collaboration easier if other developers join the project.

Therefore, a remote repository is useful for maintaining project security, backup, version history, and accessibility.

## 9. Conclusion

Git and GitHub make project management easier by maintaining version history and storing code online.

Even for a solo project, a remote repository provides backup, accessibility, and better project management.

Connecting a local repository to GitHub using `git remote add origin` makes it easy to push and pull changes.
