# Event Booking Frontend

A React frontend where users can browse events, view details and book tickets.

## Project goals

- Let visitors browse and search upcoming events.
- Show event details (date, venue, price, seats left).
- Let users book and cancel tickets through a simple form with validation.
- Keep the code easy to read and contribute to, with a clean Git history.

## Setup steps

```bash
git clone https://github.com/exelynt-learning-platform/react-frontend-devel-assignment-40252-gayatri.git
cd react-frontend-devel-assignment-40252-gayatri/event-booking-frontend
npm install
cp .env.example .env     # add your own values; never commit .env
npm run dev              # start the dev server
npm run build            # create a production build
```

Requirements: Node.js 18 or newer and npm.

## Project structure

```
event-booking-frontend/
  README.md          project documentation (this file)
  CONTRIBUTING.md    how to contribute
  .gitignore         files Git must not track
```

## About .gitignore

The `.gitignore` file lists files and folders that Git should not track:

- `node_modules/`: installed packages. They are large and can be recreated with `npm install`.
- `build/` and `dist/`: generated build output. It can be rebuilt, and committing it creates noisy diffs.
- `.vscode/`, `.idea/`, `*.swp`, `.DS_Store`: editor and operating system files that differ between developers.
- `.env` (and `.env.local`): environment variables that may contain secrets such as API keys. Committing them would expose secrets publicly.

## Contribution guidelines

See [CONTRIBUTING.md](CONTRIBUTING.md). In short: create a branch for each change, make small commits with clear messages, open a pull request, and wait for a review before merging.

## GitHub issues and pull requests

- **Issues** are used to report bugs, request features and ask questions. Each issue has a title, a description, labels and an assignee, so the team can discuss and track work in one place. A commit or pull request can close an issue by writing `Closes #12` in its description.
- **Pull requests (PRs)** propose merging a branch into another branch (usually `main`). A PR shows the changes, lets teammates review and comment, runs automated checks, and records the decision. Nothing reaches `main` until the PR is approved and merged.

## Three Git best practices for React teams

1. **Use short-lived feature branches and pull requests.** Never commit directly to `main`. One branch per feature or fix (for example `feature/booking-form`) keeps `main` stable and makes reviews easy.
2. **Write small, focused commits with clear messages.** One purpose per commit, for example "Add validation to booking form". This makes history readable and any change easy to find or revert.
3. **Keep secrets and generated files out of the repository.** Use `.gitignore` for `node_modules/`, build output and `.env`, and keep `package-lock.json` committed so everyone installs the same dependency versions.
