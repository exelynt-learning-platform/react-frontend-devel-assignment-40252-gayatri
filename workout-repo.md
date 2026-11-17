# Workout Planner – Git Repository Assignment

## 1. Repository Initialization

Created a folder named `workout-planner` and initialized it as a Git repository using:

```bash
mkdir workout-planner
cd workout-planner
git init
```

The `git init` command creates a hidden `.git` folder that stores all the information Git needs to manage the repository.

## 2. What is the .git Folder?

The `.git` folder is the internal database of a Git repository. It stores:

- **HEAD:** Points to the currently checked-out branch or commit.
- **config:** Stores repository-specific configuration.
- **objects:** Stores Git objects such as commits, trees, and file contents.
- **refs:** Stores references to branches and tags.
- **index:** Stores the staging area information.
- **logs:** Records changes to references, such as branch movements.

The `.git` folder is important because it maintains the project's version history and tracking information.

## 3. Creating plan.txt

Created a file named `plan.txt` with the following content:

```text
Workout Planner

Monday: Cardio for 30 minutes
Tuesday: Upper body workout
Wednesday: Rest day
Thursday: Lower body workout
Friday: Full body workout
Saturday: Walking for 30 minutes
Sunday: Rest day
```

After creating the file, executed:

```bash
git status
```

The file appeared as an untracked file because Git had not started tracking it.

## 4. Staging and Modifying the File

First, added the file to the staging area:

```bash
git add plan.txt
```

Then modified `plan.txt` by adding another workout activity:

```text
Monday: Cardio for 30 minutes
Tuesday: Upper body workout
Wednesday: Rest day
Thursday: Lower body workout
Friday: Full body workout
Saturday: Walking for 30 minutes
Sunday: Rest day

Additional Activity: Stretching for 10 minutes
```

After modifying the file, executed:

```bash
git status
```

The file appeared in two sections:

- Changes to be committed: The previously staged version.
- Changes not staged for commit: The new modifications made after staging.

### Why does this happen?

When `git add` is executed, Git saves the current version of the file in the staging area.

If the file is modified again after staging, Git detects the new changes separately. Therefore, the file appears as both staged and modified.

To stage the latest changes, execute:

```bash
git add plan.txt
```

## 5. Three File States in Git

Git has three main file states:

### 1. Modified

A file is modified when changes are made to it but those changes have not yet been staged.

Example: Editing `plan.txt` to add a new workout activity.

### 2. Staged

A file is staged when changes are added to the staging area using:

```bash
git add plan.txt
```

The changes are now ready to be included in the next commit.

### 3. Committed

A file is committed when staged changes are permanently recorded in the repository history.

Example:

```bash
git commit -m "Add weekly workout plan"
```

## 6. How Changes Move Between the Three States

Using `plan.txt` as an example:

1. Create `plan.txt`. It is initially untracked.
2. Edit the file to add workout activities. It becomes modified.
3. Run `git add plan.txt`. The changes become staged.
4. Run `git commit -m "Add weekly workout plan"`. The changes become committed.
5. Edit the file again. It becomes modified.
6. Run `git add plan.txt` again to stage the latest changes.
7. Commit the latest changes to save them in the repository history.

## 7. Conclusion

Git helps developers track file changes, maintain project history, and manage different versions of their work.

The three important file states are Modified, Staged, and Committed. Understanding these states helps developers manage their work correctly and collaborate effectively.
