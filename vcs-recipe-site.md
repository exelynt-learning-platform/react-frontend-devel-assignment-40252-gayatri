# Version Control Primer for an Open-Source Recipe Site

## 1. What is version control?

Version control is a system that records every change made to a set of files over time, so you can see who changed what and when, compare versions, and go back to any earlier state. Instead of keeping copies named `recipes_final_v2_REAL.html`, the system stores the full history in one place.

### Why open-source volunteers editing a recipe website depend on it

A recipe website is edited by many volunteers who may never meet, work in different time zones, and edit the same pages (for example, one fixes a typo in the pasta recipe while another adds a vegan variation to it). Version control lets them:

- work at the same time without overwriting each other's changes;
- see exactly who changed which recipe and why, through commit messages;
- undo a bad edit, for example someone deleting the ingredient list, by restoring an earlier version;
- review changes before they reach the live site, so mistakes and spam are caught.

Without it, the project would depend on emailing files around and hoping nobody pastes over someone else's work.

## 2. Why developers use Git

Git is the most widely used version control tool. Developers use it because it is fast, free and open source, keeps a complete history on every contributor's computer, makes branching cheap, and works with almost every hosting service and team.

## 3. Three common problems Git solves when many contributors edit the same files

1. **Overwritten work.** Two volunteers edit `pancakes.md` at once and the last one to save wipes out the first one's changes. Git tracks changes as commits and merges them. If two people edit different parts of a file, Git combines them automatically.
2. **Edit conflicts that nobody notices.** When two people change the same lines, Git does not silently pick one. It marks a merge conflict so the contributors decide which version to keep.
3. **Lost history and no way to undo.** Without history, a broken or deleted recipe cannot be restored and nobody knows who changed it. Git keeps every commit, so a change can be inspected with `git log` and `git diff`, and undone with `git revert` or by checking out an older version.

(Branches also solve a fourth problem: contributors can try a new feature on their own branch without disturbing the stable site.)

## 4. Git vs GitHub

- **Git** is the version control software. It runs on your computer, tracks changes, and works offline. It manages commits, branches and merges.
- **GitHub** is a website and service that hosts Git repositories online and adds collaboration tools on top of Git. It is a company's product, and Git can be used without it (other hosts include GitLab and Bitbucket).

A feature that exists only on GitHub: **pull requests**. A contributor pushes a branch and opens a pull request so maintainers can review, comment on and approve the change before it is merged. Git itself has no pull request. Issues, GitHub Actions and the web interface for reviewing code are also GitHub features.

## 5. Centralized vs distributed version control

| | Centralized (e.g. SVN, CVS) | Distributed (e.g. Git) |
| --- | --- | --- |
| Where is the history? | One central server holds the full history | Every contributor has a full copy of the repository and its history |
| Working offline | Needs a connection to the server to commit or view history | Can commit, branch, view history and compare versions offline |
| Single point of failure | If the server fails, history can be lost | Any clone can restore the repository |
| Speed | Operations talk to the server | Most operations are local and fast |
| Branching | Often slow and heavy | Cheap and fast |

### Why distributed control suits contributors working offline

A volunteer on a train or with a poor connection can keep editing recipes, committing, and creating branches on their own computer because the whole repository is stored locally. When the connection comes back, they run `git push` to share their commits and `git pull` to receive others' work. With a centralized system they could not commit until they were online. Distributed control also means every volunteer's copy is a backup of the project.

## Summary

Version control records the history of a project. Git is the distributed tool that does it on each computer, and GitHub is the hosting service that adds pull requests and other collaboration features. Together they let many volunteers safely improve a recipe website.
