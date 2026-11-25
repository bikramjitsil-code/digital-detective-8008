# Mission 2 — Become comfortable with the Terminal

## 1. Task / objective

Use Terminal to navigate directories, create and manage practice files, understand command flags and pipes, and explain the purpose of package managers.

## 2. Work completed

### Task 2.1 — Basic Terminal operations

The following table records the commands and their purposes. The observation column must reflect the actual command output.

| Command I used | What it does | What I observed |
|---|---|---|
| `pwd` | Shows my current location | The path ended in `Documents/digital-detective-8008`, so I could tell I was inside my project folder. |
| `ls` | Lists the files and folders | I could see `README.md`, the numbered mission folders and the `evidence` folder. |
| `ls -l` | Shows a detailed listing | I saw the same files and folders, but this time each entry also showed details like its permissions, size and modification date. |
| `cd ..` | Moves up one folder | When I ran `pwd` again, the path ended in `Documents`. I had moved out of the project folder. |
| `cd digital-detective-8008` | Enters the project folder | I was back inside my project and could see the mission folders again when I ran `ls`. |
| `mkdir terminal-practice` | Creates a folder | The command itself printed nothing. When I ran `ls` inside `mission-02-terminal`, I could see the new `terminal-practice` folder. |
| `touch sample.txt` | Creates an empty file | A file named `sample.txt` appeared in my practice folder. It had no text in it yet. |
| `cp sample.txt sample-copy.txt` | Copies a file | I could see two files: `sample.txt` and `sample-copy.txt`. The original was still there. |
| `mv sample-copy.txt renamed-copy.txt` | Renames the copy | The copy now appeared as `renamed-copy.txt`. The old name `sample-copy.txt` was gone, and the original `sample.txt` was still there. |
| `cat sample.txt` | Displays the file’s contents | No text appeared, and the Terminal prompt came back. That made sense because I hadn’t written anything in the file yet. |

### Task 2.2 — Practise file changes safely

The practice files belong inside `mission-02-terminal/terminal-practice`.

Commands used for writing:

```bash
echo "This is my first line." > notes.txt
echo "This is my second line." >> notes.txt
cat notes.txt
```

Expected contents:

```text
This is my first line.
This is my second line.
```

Actual contents and confirmation that both lines are present: [When I ran `cat notes.txt`, I saw both lines in the order I wrote them. Using `>>` added the second line below the first and kept the first line in the file.]

Backup commands:

```bash
cp notes.txt notes-backup.txt
mv notes-backup.txt notes-backup-renamed.txt
```

Backup verification:[After copying and renaming the backup, I could see both `notes.txt` and `notes-backup-renamed.txt`. Renaming the backup did not change the name of the original file.]

#### Replacing versus appending

`>` writes output to a file and replaces any existing contents. `>>` adds output to the end without removing existing contents.

#### Copying versus moving

Copying creates another file while keeping the original. Moving changes the file's location or name without retaining a separate original at its previous path.

#### Information provided by the current-directory display

`pwd` displays the full path of the directory where commands are currently being executed.

#### Why directory listings are useful

Directory listings help check available files, confirm names and verify that file operations produced the intended result.

### Task 2.3 — Flags and pipes

`ls` displays a normal listing.

`ls -lah` combines three flags:

- `-l`: detailed listing.
- `-a`: include hidden entries.
- `-h`: use human-readable file sizes.

Observed difference between the listings: [When I ran `ls`, I saw the names of my practice files. When I ran `ls -lah`, each entry appeared on its own line with details such as permissions, file size and modification time. I also saw `.` and `..`, which represent the current folder and its parent folder.]

Pipe command:

```bash
ls -l | head -n 5
```

The pipe passes the output of `ls -l` to `head`. The second command displays up to the first five lines of that output. These are lines, not necessarily five files.

Actual pipe result: [With `ls`, I saw a simple list of filenames. With `ls -lah`, I saw a longer listing that included hidden entries such as `.` and `..`, along with permissions and sizes.

When I ran `ls -l | head -n 5`, the output stopped after the first five lines. I noticed that a line such as `total` also counts, so five lines of output does not always mean five filenames.]

### Task 2.4 — Package managers

A package manager helps install, update, track and remove software packages. It can also handle dependencies needed by those packages.

Homebrew is a package manager commonly used on macOS. I checked its availability using `command -v brew`.

Homebrew availability: Homebrew was available on my Mac. `brew --version` displayed its version, and `brew list` showed the packages it manages. I only inspected the information and did not install or remove anything.

Version, if available: `Homebrew 7.0.10`

Package-list observation, if available: [When I ran brew list, I saw the names of the packages Homebrew manages on my Mac. I could check what was installed without changing anything.]

No software installation or removal is required for this activity.

## 3. Commands / tools used

`pwd`, `ls`, `cd`, `mkdir`, `touch`, `cp`, `mv`, `cat`, `echo`, `head` and `command -v` were used or provided for the practical activities.

`>` redirects output into a file, `>>` appends output, and `|` passes output between commands.

Homebrew commands apply only if Homebrew is available.

VS Code is used for documentation, and Git/GitHub are used to commit and publish the mission.

## 4. My understanding

Terminal commands operate relative to the current directory unless another path is supplied.

Flags modify command behaviour. Redirection sends output into files, while a pipe connects the output of one command to the input of another.

Checking the current directory and filenames helps avoid changing the wrong files.

## 5. Difficulties faced

No major difficulties.

## 6. How I resolved them

Not applicable.

## 7. Evidence / files

- `README.md`.
- `terminal-practice/sample.txt`.
- `terminal-practice/renamed-copy.txt`.
- `terminal-practice/notes.txt`.
- `terminal-practice/notes-backup-renamed.txt`.
- Privacy-safe observations recorded in this README.

## 8. Commit details

Planned commit message: `Complete Terminal and file management mission`

Commit, push and GitHub verification: Verified and committed the mission documentation and terminal-practice files, then pushed to GitHub.