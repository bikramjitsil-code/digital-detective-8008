# Mission 6 — Git and GitHub

## 1. Task / objective

Understand version control, stage and commit changes, inspect history, create a branch, open a Pull Request and explain the collaboration workflow.

## 2. Work completed

### Task 6.1 — Basic Git workflow

| Git operation | Command | What it does |
|---|---|---|
| Check repository status | `git status` | Shows the branch and staged, unstaged or untracked changes |
| Stage selected changes | `git add mission-06-git-github/README.md` | Selects the saved version of this file for the next commit |
| Create a commit | `git commit -m "Document basic Git workflow"` | Records the staged snapshot in local history |
| View commit history | `git log --oneline -5` | Shows up to five recent commits in a compact format |

Staging selects the changes to include. Committing records the selected changes as a snapshot in repository history.

Actual status, commit and history observations: [After I saved the Mission 6 README, `git status` showed it as modified. After `git add`, it appeared under “Changes to be committed”. Once I committed it, `git log --oneline -5` showed my commit message in the recent history.]

### Task 6.2 — Create and use a branch

Required branch: `update-about`.

Command:

```bash
git switch -c update-about
```

The branch is used to add a section titled `My Learning` to the root README.

Commands for publishing the change:

```bash
git add README.md
git commit -m "Add my learning summary to README"
git push -u origin update-about
```

Actual branch creation and publication result: [I created the `update-about` branch and added a “My Learning” section to the root README on that branch. After pushing, I could select `update-about` on GitHub and see the new section.]

### Task 6.3 — Create a Pull Request

Pull Request direction:

- Source / compare branch: `update-about`.
- Destination / base branch: `main`.

Purpose: Propose adding the learning summary to the root README.
Pull Request URL: https://github.com/bikramjitsil-code/digital-detective-8008/pull/1
Pull Request status: Merged
Merge instruction from instructor: Completed merge of Pull Request #1 into `main`.

A branch provides a separate line of development. A Pull Request allows proposed changes to be reviewed before they are incorporated into another branch.

If the PR remains open, its changes remain available on `update-about` and in the Pull Request. They are not yet part of `main`.

If the PR is merged, the local main branch can be updated using:

```bash
git switch main
git pull origin main
```

### Task 6.4 — Git command glossary

| Command | Explanation |
|---|---|
| `git init` | Initialise a Git repository in the current directory |
| `git status` | Display the current branch and file-change status |
| `git add filename` | Stage a file's current saved changes |
| `git commit -m "message"` | Record staged changes with a descriptive message |
| `git log` | Display commit history |
| `git branch` | List local branches |
| `git branch branch-name` | Create a branch without switching to it |
| `git switch branch-name` | Switch to another branch |
| `git switch -c branch-name` | Create and switch to a branch |
| `git push` | Send local commits to a remote repository |
| `git pull` | Fetch remote changes and integrate them into the current branch |

## 3. Commands / tools used

Git commands for status, staging, commits, history, branches, pushing and pulling.

VS Code is used to edit the README. GitHub is used to host branches and create and review the Pull Request.

## 4. My understanding

Git is version-control software, while GitHub is a service for hosting Git repositories and collaborating online.

A commit is a local record of selected changes. A push transfers commits to a remote repository.

Branches allow changes to be developed separately. Pull Requests make it possible to review differences and discuss changes before merging.

## 5. Difficulties faced

[I saw “Open 0” on GitHub and thought my Pull Request was already open. I looked for its title and URL, but the list was empty. I also couldn’t select `update-about` because I hadn’t created the branch yet.]

## 6. How I resolved them

[I learned that “Open 0” meant there were zero open Pull Requests. I created the `update-about` branch, added the “My Learning” section to the root README, committed the change and pushed the branch. GitHub then showed `update-about` as a compare option, and I selected `main` as the base branch.]

## 7. Evidence / files

- `mission-06-git-github/README.md`.
- Root README change on `update-about`.
- Published branch.
- Pull Request and its actual status.
- GitHub commit history.

## 8. Commit details

Basic workflow commit: `Document basic Git workflow`

Branch commit: `Add my learning summary to README`

Final mission commit: `Complete Git and GitHub collaboration mission`

Commit, push and GitHub verification: Pushed the `update-about` branch to GitHub, opened Pull Request #1 to propose the 'My Learning' section in the root README, and completed the merge into `main`.