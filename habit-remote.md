# Introduction to GitHub
# Publish a Daily Habit Tracker to GitHub

## 1. GitHub account

I have a GitHub account.

- Username: gayatrikotwal-web
- Profile: https://github.com/gayatrikotwal-web

## 2. Create a local Git repository

I created a local project folder named habit-tracker and initialized it with Git.

Commands:

```bash
mkdir habit-tracker
cd habit-tracker
git init -b main
```

Output:

```
Initialized empty Git repository in /home/claude/work/habit-tracker/.git/
```

`git init` creates a hidden .git folder that stores the project history and configuration.

## 3. Create the remote repository on GitHub

I created a public repository named habit-tracker on my GitHub account:

https://github.com/gayatrikotwal-web/habit-tracker

## 4. Connect the local repository to GitHub

Command:

```bash
git remote add origin https://github.com/gayatrikotwal-web/habit-tracker.git
```

This registers the GitHub repository as a remote named `origin`. The command prints nothing when it succeeds.

## 5. Verify the remote

Command:

```bash
git remote -v
```

Output:

```
origin	https://github.com/gayatrikotwal-web/habit-tracker.git (fetch)
origin	https://github.com/gayatrikotwal-web/habit-tracker.git (push)
```

Both the fetch and push URLs point to my habit-tracker repository, so the local repo is connected to GitHub correctly.

## 6. Pushing

Command to publish the local main branch:

```bash
git push -u origin main
```

I did not paste push output here because I have not pushed any commits from the local habit-tracker repository yet; the `git init` and `git remote` outputs above are the real output of the commands I ran. This assignment file itself was committed to the assignment repository on the branch introduction-to-github-week1-4.

## 7. Why a remote repository is useful even for a solo project

A remote repository keeps an off-site backup of my code, so a lost or broken laptop does not mean lost work. It lets me open the project from any computer and continue where I left off. It stores the full commit history online, so I can review or roll back changes at any time. It also makes it easy to share my work with mentors, reviewers or employers through a single link. Finally, it prepares me to collaborate later, because the same push and pull workflow works for a team.
