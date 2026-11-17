# Study Log: Tracking Changes with Git

This log records the commits I made while keeping HTML and CSS study notes under version control on the branch `tracking-changes-with-git-week1-4`.

## Workflow I followed for each change

```
git status            # see which files are new or modified
git add <file>        # stage only the file for this change
git commit -m "..."   # save a snapshot with a clear message
git log --oneline     # check the history
```

## Commit history

The four commits below are the real history of this branch (newest first), taken from the commit list on GitHub, which shows the same information as `git log --oneline`:

```
$ git log --oneline -4
03418f2 Add Flexbox explanation to CSS notes
1d96451 Add semantic tags information to HTML notes
26e2940 Add initial CSS notes to documentation
faa1376 Add initial HTML notes to html-notes.md
```

Older commits from earlier assignments (for example `4d8aa74`) appear below these four and are not part of this assignment.

## What each commit contains

- **faa1376 - Add initial HTML notes to html-notes.md**: creates `html-notes.md` with a heading and three bullet points about what HTML is, what elements are, and how a page starts.
- **26e2940 - Add initial CSS notes to documentation**: creates `css-notes.md` with a heading and three bullet points about what CSS is, how a rule is written, and how a stylesheet is linked.
- **1d96451 - Add semantic tags information to HTML notes**: edits `html-notes.md` and adds one bullet about semantic tags (`<header>`, `<nav>`, `<main>`, `<footer>`). Only this file changed.
- **03418f2 - Add Flexbox explanation to CSS notes**: edits `css-notes.md` and adds one bullet about Flexbox. Only this file changed.

Each commit does one small thing, so the history reads like a story and any single change can be reviewed or undone on its own.

## Two common beginner mistakes and how to avoid them

### 1. Committing secrets (passwords, API keys, `.env` files)
Once a secret is committed and pushed, it stays in the history even if the file is deleted later, and anyone who can see the repository can find it.

**How to avoid it:**
- Put secrets in a `.env` file and list it in `.gitignore` before the first commit.
- Run `git status` and `git diff --staged` before every commit to check what is going in.
- If a secret is ever committed, revoke it immediately and create a new one; do not rely on deleting the file.

### 2. Huge mixed commits with vague messages
Putting many unrelated changes into one commit with a message like "update" or "stuff" makes the history hard to read, hard to review, and hard to undo.

**How to avoid it:**
- Commit small, focused changes, one purpose per commit.
- Stage files deliberately with `git add <file>` instead of `git add .` when changes are unrelated.
- Write the message so it says what changed and why, for example "Add Flexbox explanation to CSS notes".
