# Personal Travel Log

A small static website and set of notes that record places I have visited. The project is tracked with Git to practise commits, branches, merging and conflict resolution.

## Project structure

```
travel-log/
  .gitignore        files Git must not track (node_modules/, dist/, build/, editor files, .env)
  README.md         this file
  index.html        home page that links to every trip
  css/style.css     basic styles
  trips/
    manali.md       trip entry
    jaipur.md       trip entry
    goa.md          trip entry
```

## Setup and run

1. Clone the repository and open the project folder:
   ```bash
   git clone https://github.com/exelynt-learning-platform/react-frontend-devel-assignment-40252-gayatri.git
   cd react-frontend-devel-assignment-40252-gayatri/travel-log
   ```
2. No dependencies are needed. Open `index.html` in a web browser (double-click it), or serve the folder:
   ```bash
   python3 -m http.server 8000
   ```
   then visit http://localhost:8000.
3. To add a trip: create a file in `trips/`, link it in `index.html`, and commit.

## Git workflow used

- Work started on `main` with five commits (`.gitignore`, README, home page, stylesheet, Manali entry).
- A feature branch `add-goa-trip` added the Goa entry and its link on the home page (2 commits).
- At the same time `main` got a Jaipur entry (1 commit) that edited the same part of `index.html`.
- `git merge add-goa-trip` was run on `main`, and Git reported a merge conflict.

### Merge conflict explained

Both branches added a new `<li>` line directly under the Manali link in `index.html`. Git cannot know which line should come first, so it stopped and marked the file:

```
<<<<<<< HEAD
    <li><a href="trips/jaipur.md">Jaipur</a></li>
=======
    <li><a href="trips/goa.md">Goa</a></li>
>>>>>>> add-goa-trip
```

Resolution: both links are wanted, so I deleted the three marker lines and kept both `<li>` lines, then ran `git add index.html` and `git commit` to complete the merge.

### Commit history

Output of `git log --oneline --graph` on my local repository after the merge:

```
*   e007c82 Merge add-goa-trip into main and keep both Jaipur and Goa links
|\  
| * d25d6c2 Link Goa trip on home page
| * 9250c97 Add Goa trip entry
* | b5d87f8 Add Jaipur trip entry and home page link
|/  
* 8cd2d6f Add Manali trip entry
* 8d1d19c Add basic stylesheet
* 6a9ca8f Add travel log home page
* 52e88b9 Add initial README
* d64616c Add .gitignore for dependencies, build output, editors and .env
```

Note: this log comes from the local repository where the branch, merge and conflict were done. The files were then published to this GitHub branch with GitHub's web editor, so the commits here have different hashes and the merge itself is not visible in this repository's history.

## Security

No sensitive files are committed. `.env` and similar files are listed in `.gitignore`, and the project has no secrets or API keys.
