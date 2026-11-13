# Mission 0 — Create your GitHub workspace

## 1. Task / objective

The objective of this mission is to create an organised workspace for the Digital Detective assignment and prepare a public GitHub repository. The project must contain a root README, separate folders and READMEs for all nine missions, and an evidence folder.

## 2. Work completed

I created the local project folder named `digital-detective-8008` and organised it into the following folders:

- `mission-00-setup`
- `mission-01-computer-basics`
- `mission-02-terminal`
- `mission-03-operating-system`
- `mission-04-programs`
- `mission-05-numbers-data`
- `mission-06-git-github`
- `mission-07-networking`
- `mission-08-final-report`
- `evidence`

I created a separate `README.md` inside every mission folder and a root `README.md` for the overall assignment.

I prepared the root README with the project title, assignment purpose, a mission index linking to each mission README, and a note explaining that missions will be completed and committed separately.

I also created an empty `number_converter.py` file inside `mission-05-numbers-data` for Mission 5. I added an empty `.gitkeep` file inside `evidence` so that Git can track a file in that otherwise empty folder.

GitHub publication and verification are pending.

## 3. Commands / tools used

| Command / tool | Purpose |
|---|---|
| Terminal | Enter commands to create and inspect the project |
| `python3 --version` | Check the installed Python version |
| `git --version` | Check the installed Git version |
| `cd` | Move into another directory |
| `mkdir` | Create a directory |
| `touch` | Create an empty file if it does not already exist |
| `ls` | List files and folders in the current directory |
| `open .` | Open the current folder in Finder on macOS |
| Text editor | Write and save the README files |

Python version: **[Python 3.14.5]**

Git version: **[git version 2.54.0 (Apple Git-157)]**

Git publication commands will be added here after I use them.

## 4. My understanding

A repository is a project whose files and change history can be managed using Git. Git works locally on my computer, while GitHub hosts a copy online.

The root README introduces the complete assignment and helps visitors navigate to each mission. Each mission README explains the work for that particular mission.

A path such as `mission-00-setup/README.md` means that the file `README.md` is inside the folder `mission-00-setup`. Files in different folders can have the same name without being the same file.

Separating the assignment into mission folders makes the work easier to find, review and update. Recording each completed mission in a separate commit will make the progress visible in the repository history.

Git tracks files rather than empty directories. The `.gitkeep` file is an ordinary placeholder that allows the evidence folder to appear in the repository even before evidence is added.

## 5. Difficulties faced

I was initially confused about whether the first `README.md` in the assignment table was a file or a folder. I also did not understand why `.gitkeep` was added to the evidence folder.

## 6. How I resolved them

I asked for explanations and learned that the first `README.md` is the main file in the project root. The other README files are separate files located inside their respective mission folders.

I also learned that Git does not track empty folders. Adding `.gitkeep` gives Git a file to track inside the evidence folder.

## 7. Evidence / files

- Root `README.md`: assignment introduction and mission index.
- `mission-00-setup/README.md`: setup documentation.
- Mission folders from `mission-00-setup` to `mission-08-final-report`, each containing a README.
- `mission-05-numbers-data/number_converter.py`: empty file prepared for the later programming task.
- `evidence/.gitkeep`: placeholder for the evidence folder.

## 8. Commit details

Planned commit message: `Set up Digital Detective mission structure`

Commit status: Completed.

Push status: Completed.

GitHub verification: Setup commit confirmed visible on GitHub.