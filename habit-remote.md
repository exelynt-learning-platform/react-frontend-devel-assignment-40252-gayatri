# Publish a Daily Habit Tracker to GitHub

## 1. Create a Local Git Repository

Created a project folder named `habit-tracker` and initialized it using Git.

Commands executed:

```bash
mkdir habit-tracker
cd habit-tracker
git init
```

The `git init` command initializes a new Git repository and creates a hidden `.git` folder that stores project history and configuration.

## 2. Create a GitHub Repository

Created a GitHub repository with the following details:

- Repository Name: habit-tracker
- Platform: GitHub
- Visibility: Public
- GitHub Repository URL: [Replace with your actual GitHub repository URL]

The GitHub repository stores the project online and maintains its version history.

## 3. Connect the Local Repository to GitHub

Connected the local repository to GitHub using the following command:

```bash
git remote add origin YOUR_ACTUAL_GITHUB_REPOSITORY_URL
```

Here, `origin` is the default name assigned to the remote repository, and the URL points to the GitHub repository.

## 4. Verify the Remote Connection

Executed the following command:

```bash
git remote -v
```

### Actual Terminal Output

Paste the actual output from your terminal here:

```text
PASTE YOUR ACTUAL GIT REMOTE -V OUTPUT HERE
```

The output should display the remote GitHub URL for both fetch and push operations.

## 5. Create an Assignment Branch

Created a separate branch named `assignment/habit-remote` for this assignment.

Command:

```bash
git switch -c assignment/habit-remote
```

This branch allows me to complete the assignment independently without directly changing the main branch.

## 6. Stage and Commit the Assignment

Added the assignment file to the staging area:

```bash
git add habit-remote.md
```

Committed the changes using a clear commit message:

```bash
git commit -m "docs: complete habit tracker remote assignment"
```

## 7. Push the Assignment to GitHub

Pushed the assignment branch to the GitHub repository:

```bash
git push -u origin assignment/habit-remote
```

### Actual Git Push Output

Paste your actual successful push output here:

```text
PASTE YOUR ACTUAL SUCCESSFUL GIT PUSH OUTPUT HERE
```

A successful push confirms that the assignment branch has been uploaded to GitHub.

## 8. Why Is a Remote Repository Useful Even for a Solo Project?

A remote repository is useful even when only one developer is working on a project. It provides an online backup, reducing the risk of losing important work if the local computer fails. It allows developers to access their projects from different computers and maintain their work history. It also makes it easier to share code, restore previous versions, and manage project updates. Additionally, it makes future collaboration easier if other developers join the project.

## 9. Conclusion

Git and GitHub help developers manage project versions and store code online. A remote repository provides backup, accessibility, and better project management. Connecting a local repository to GitHub makes it easier to push and pull project changes.
