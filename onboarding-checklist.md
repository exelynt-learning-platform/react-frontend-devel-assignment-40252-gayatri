# Git Environment Checklist for a New Intern

Welcome! Follow this checklist to get Git working on your computer before your first day. Pick the section for your operating system.

## 1. Install Git

### Windows
1. Download the installer from https://git-scm.com/download/win and run it.
2. Keep the default options and click Next until the install finishes. This also installs Git Bash.
3. Open **Git Bash** from the Start menu to use Git.

### macOS
1. Open Terminal and run `git --version`. If Git is missing, macOS offers to install the Command Line Tools; accept.
2. Or install with Homebrew: `brew install git`.
3. Close and reopen Terminal after installing.

### Linux
1. Debian/Ubuntu: `sudo apt update && sudo apt install git`.
2. Fedora: `sudo dnf install git`. Arch: `sudo pacman -S git`.
3. Open a new terminal when it finishes.

## 2. Proof that Git is installed

I installed and verified Git myself. Command and output:

```
$ git --version
git version 2.43.0
```

Note: I ran this on a Linux machine (kernel 6.18). On Windows or macOS the version number may differ, but the command is the same.

## 3. Configure your name and email

Git stamps every commit with this information. Use the same email as your GitHub account.

```
$ git config --global user.name "gayatrikotwal-web"
$ git config --global user.email "gayatrikotwal-web@users.noreply.github.com"
```

Check it (only the name and email lines are shown):

```
$ git config --global --list | grep -E '^user\.(name|email)='
user.name=gayatrikotwal-web
user.email=gayatrikotwal-web@users.noreply.github.com
```

On Windows Git Bash, `grep` also works; or simply run `git config --global --list`.

## 4. Terminal basics

These are commands I actually ran in one terminal session, with their output.

| Command | What it does |
| --- | --- |
| `pwd` | Prints the folder you are in |
| `ls` (`dir` on Windows cmd) | Lists files and folders |
| `mkdir name` | Creates a new folder |
| `cd name` | Moves into a folder (`cd ..` goes up one level) |
| `touch file` | Creates an empty file |

```
$ pwd
/tmp/demo
$ ls
$ mkdir intern-project
$ ls
intern-project
$ cd intern-project
$ pwd
/tmp/demo/intern-project
$ touch notes.txt
$ ls -l
total 0
-rw-r--r-- 1 root root 0 Nov 17 06:07 notes.txt
$ cd ..
$ pwd
/tmp/demo
```

The first `ls` printed nothing because the folder was empty. After `mkdir`, `ls` shows the new folder. `cd` changed the folder, which `pwd` confirmed.

## 5. Final checklist

- [ ] Git installed (`git --version` prints a version)
- [ ] `user.name` and `user.email` configured
- [ ] Can open the terminal / Git Bash
- [ ] Can use `pwd`, `ls`, `cd` and `mkdir`
