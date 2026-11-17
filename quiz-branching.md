# Quiz Branching Assignment

## 1. Create a Branch from Main

First, switch to the main branch and create a new branch named `fix-score-bug`.

Commands:

```bash
git switch main
git pull origin main
git switch -c fix-score-bug
```

The `fix-score-bug` branch is created from the main branch. This allows us to work on the quiz score issue without directly modifying the main branch.

## 2. Make and Commit the Fix

Modified `quiz.txt` to correct the score calculation rules.

The corrected scoring logic is:

- Correct answer = 1 point.
- Incorrect answer = 0 points.
- Unanswered question = 0 points.

Stage and commit the changes:

```bash
git add quiz.txt
git commit -m "fix: correct quiz score calculation rules"
```

The changes are now saved in the `fix-score-bug` branch.

## 3. Switch Back to Main and Verify

Switch back to the main branch:

```bash
git switch main
```

Check the contents of `quiz.txt`:

```bash
cat quiz.txt
```

The score fix is not present in the main branch because the changes were committed only on `fix-score-bug`.

This confirms that feature branch changes remain separate until they are merged.

## 4. Merge the Branch into Main

Merge the completed feature branch into main:

```bash
git merge fix-score-bug
```

The changes from `fix-score-bug` are now included in the main branch.

## 5. Git Branch Output

Command:

```bash
git branch
```

Expected output:

```text
  fix-score-bug
* main
```

The asterisk indicates that the current branch is `main`.

## 6. Git Commit History Output

Command:

```bash
git log --oneline --graph
```

Example output:

```text
* 71cd356 fix: correct quiz score calculation rules
* 76e7dee chore: add starter quiz
```

The graph shows the commit history and confirms that the score fix is part of the main branch after merging.

Note: Commit hashes and graph formatting may differ in your actual repository.

## 7. What Is a Merge Conflict?

A merge conflict happens when Git cannot automatically combine changes from two branches.

This commonly happens when two developers modify the same lines in the same file differently.

### When Does a Merge Conflict Occur?

For example:

- Developer A changes the quiz score from 1 point to 2 points.
- Developer B changes the same score from 1 point to 3 points.
- Both developers commit their changes on different branches.
- When the branches are merged, Git cannot decide which change should be kept.

This creates a merge conflict.

### Steps to Resolve a Merge Conflict

**Step 1: Identify the conflict**

Run:

```bash
git status
```

Git shows the files that have conflicts.

**Step 2: Open the conflicted file**

Git displays conflict markers like:

```text
<<<<<<< HEAD
Score: 2 points
=======
Score: 3 points
>>>>>>> another-branch
```

**Step 3: Resolve the conflict**

Decide which change should be kept or combine both changes.

For example:

```text
Score: 2 points
```

Remove all conflict markers after resolving the issue.

**Step 4: Stage the resolved file**

```bash
git add quiz.txt
```

**Step 5: Complete the merge**

```bash
git commit -m "fix: resolve quiz score merge conflict"
```

**Step 6: Verify the result**

```bash
git status
git log --oneline --graph
```

The merge conflict is resolved, and the final changes are saved in the repository.

## 8. Conclusion

Git branches allow developers to work on different features independently without affecting the main branch.

After completing the changes, developers can merge their branches into main.

Merge conflicts can happen when multiple contributors modify the same parts of a file. Git helps identify these conflicts so developers can resolve them manually.

Branching and merging make collaborative software development safer and more organized.
