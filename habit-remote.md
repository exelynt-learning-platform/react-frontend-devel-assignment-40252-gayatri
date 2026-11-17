# Publish a Daily Habit Tracker to GitHub

## 1. Create a Local Git Repository

Created a project folder named `habit-tracker` and initialized it using Git.

Commands:

```bash
mkdir habit-tracker
cd habit-tracker
git init
```

The `git init` command initializes a Git repository and creates a hidden `.git` folder that stores project history and configuration.

## 2. Create a GitHub Remote Repository

Created a GitHub repository with the following details:

- Repository name: habit-tracker
- Platform: GitHub
- Repository URL: [INSERT YOUR ACTUAL GITHUB REPOSITORY URL]

The repository is used to store the project online and maintain its version history.

## 3. Connect the Local Repository to GitHub

Connected the local repository to GitHub using:

```bash
git remote add origin YOUR_ACTUAL_REPOSITORY_URL
```

Here, `origin` is the name assigned to the remote repository.

## 4. Verify the Remote Connection

Executed:

```bash
git remote -v
```

### Actual Terminal Output

Paste the complete output from your terminal here:

```text
[PASTE ACTUAL GIT REMOTE -V OUTPUT]
```

This output confirms the configured remote repository for fetching and pushing changes.

## 5. Create an Assignment Branch

Created a separate branch for the assignment:

```bash
git switch -c assignment/habit-remote
```

This branch keeps assignment-related changes separate from the main branch.

## 6. Commit the Assignment

Staged and committed the assignment file:

```bash
git add habit-remote.md
git commit -m "docs: complete habit tracker remote assignment"
```

## 7. Push the Assignment to GitHub

Executed:

```bash
git push -u origin assignment/habit-remote
```

### Actual Git Push Output

Paste the complete successful terminal output here:

```text
[PASTE ACTUAL SUCCESSFUL GIT PUSH OUTPUT]
```

The successful push confirms that the assignment branch has been uploaded to GitHub.

## 8. Why Is a Remote Repository Useful Even for a Solo Project?

A remote repository is useful even when only one developer is working on a project. It provides an online backup, reducing the risk of losing important work if the local computer fails. It allows developers to access their projects from different computers and maintain their work history. It also makes it easier to share code, restore previous versions, and manage project updates. Additionally, it makes future collaboration easier if other developers join the project.

## 9. Conclusion

Git and GitHub help developers manage project versions and store code online. A remote repository provides backup, accessibility, and better project management. Connecting a local repository to GitHub makes it easy to push and pull project changes.
