# Mission 8 — Final report and submission

## 1. Task / objective

The goal of this mission is to review my Digital Detective repository, check that a visitor can find each mission from the root README, verify the work published on GitHub and record the submission status.

Repository: [digital-detective-8008](https://github.com/bikramjitsil-code/digital-detective-8008)

## 2. Work completed

### Mission review

| Mission | Work and evidence | Status |
|---|---|---|
| [0 — Setup](../mission-00-setup/README.md) | I created the project structure and separate mission READMEs. I checked Python 3.14.5 and Git 2.54.0 (Apple Git-157). I saw the setup commit on GitHub. | Complete |
| [1 — Computer basics](../mission-01-computer-basics/README.md) | I traced typing and saving a document through input, processing, output and storage. I classified hardware and software and gave examples of everyday computer systems. | Complete |
| [2 — Terminal](../mission-02-terminal/README.md) | I practised file operations, compared directory listings and explained flags, pipes and package managers. I also checked that appending a second line preserved the first line in `notes.txt`. | Complete |
| [3 — Operating system](../mission-03-operating-system/README.md) | I checked my macOS version, storage, processes and file permissions. My process snapshot showed that `zsh` started `top`, and the owner permissions on `notes.txt` were `rw-`. | Complete |
| [4 — Programs](../mission-04-programs/README.md) | I used `hello.py` to display `Hello from Python` and compared how compilers and interpreters process instructions. | Complete |
| [5 — Numbers and data](../mission-05-numbers-data/README.md) | I worked through decimal, binary and hexadecimal conversions, checked them in Python and built a number converter. I also compared the character codes for `A` and `a`. | Complete |
| [6 — Git and GitHub](../mission-06-git-github/README.md) | I used the `update-about` branch to add a `My Learning` section to the root README. The Pull Request was reviewed and merged into `main`. | Complete — Pull Request #1 merged |
| [7 — Networking](../mission-07-networking/README.md) | I tested `example.com`. All four ping requests received replies, packet loss was 0%, and the average round-trip time was 41.769 ms. The DNS lookup returned two IPv4 addresses. | Complete |
| [8 — Final report](README.md) | I brought together the mission results, documented corrections and recorded the remaining publication and submission checks. | Complete |

### Corrections made

- In Mission 2, created and committed the practice files in `terminal-practice/` (`notes.txt`, `notes-backup-renamed.txt`, `sample.txt`, `renamed-copy.txt`) so they are visible on GitHub.
- In Mission 4, created and verified `hello.py` in `mission-04-programs/` to complete the required Python greeting program.
- In Mission 5, implemented and tested the working number converter in `mission-05-numbers-data/number_converter.py` for decimal-to-binary and decimal-to-hexadecimal conversions.
- Cleaned up remaining draft template placeholders across mission READMEs.
- In Mission 0, I expected both READMEs to change, but the GitHub commit showed only `mission-00-setup/README.md`. This helped me identify the root README edit I had missed.
- In Mission 3, my first permission check returned `No such file or directory`. I used `find` to inspect the Mission 2 folder, created the practice file and checked it again. The actual permission string was `-rw-r--r--@`.
- In Mission 6, I initially read `Open 0` as the status of a Pull Request. It was the number of open requests. I created the `update-about` branch, committed the README change and pushed the branch so I could select it on GitHub.

### Final checklist

A checked box records a completed activity. An empty box records a check or action still pending.

- [x] The local project contains mission folders numbered 0 through 8.
- [x] The root README contains an introduction and a mission index.
- [x] Mission 1 covers IPOS, hardware, software and everyday computer systems.
- [x] Mission 2 covers Terminal operations, file management, flags, pipes and package managers.
- [x] Mission 3 covers the operating system, processes, paths, storage and file permissions.
- [x] Mission 4 includes the Python greeting program and the compiler/interpreter comparison.
- [x] Mission 5 covers manual conversions, Python verification, the number converter and text encoding.
- [x] Mission 6 covers staging, committing, branches and the Pull Request workflow.
- [x] Mission 7 includes actual connectivity and DNS observations.
- [x] Every mission folder and its required files are visible on GitHub, including the Mission 2 practice files.
- [x] Every mission README on GitHub contains all required sections and has no unfinished placeholders.
- [x] Each mission has a dedicated, meaningful commit visible in the GitHub history.
- [x] The published Mission 5 README shows three positive test inputs and their actual converter outputs.
- [x] The branch, Pull Request link and its recorded status (merged) have been checked on GitHub.
- [x] The published Mission 7 README includes the network concepts, observations and website-opening explanation.
- [x] All nine links in the root README work, and the root README includes the topics, learning summary, converter instructions and note about separate mission commits.
- [x] Published screenshots and command outputs have been reviewed for private information.
- [x] The repository opens publicly and the final report commit is visible on `main`.
- [ ] The repository URL has been submitted through the instructor’s Google Form.

### Submission details

- Repository URL: https://github.com/bikramjitsil-code/digital-detective-8008
- Submission deadline: No deadline was stated in the assignment instructions available to me.
- Form submission status: Pending.
- Submission date: Not yet submitted.

## 3. Commands / tools used

| Command or tool | Purpose |
|---|---|
| `git status` | Check the current branch and see which files are modified or staged |
| `git diff` | Read saved edits before staging them |
| `git log --oneline` | Review the commit messages for each mission |
| `git add` | Select the README changes for a commit |
| `git commit` | Record the staged changes with a meaningful message |
| `git push` | Publish local commits to GitHub |
| VS Code | Edit and save the Markdown files |
| GitHub | Inspect published files, commits, branches and Pull Requests |

## 4. My understanding

I learned to follow a result back to the command or file that produced it. For example, the PID of `zsh` matched the parent PID of `top`, showing that my shell had started the command. In the networking task, one of the addresses returned by DNS matched the address used by `ping`.

I also learned to check what a Git commit actually contains. Saving a file writes the edit to my Mac, staging selects it for a commit, and pushing makes the commit available on GitHub. Opening the changed file on GitHub helped me catch an edit that I thought I had already published.

## 5. Difficulties faced

The root README and each mission README have the same filename. During setup, this made it easy to overlook which file I had saved and which file appeared in the commit. During the final review, I also needed to distinguish preparing the repository from submitting its URL through the form.

## 6. How I resolved them

I checked the full file path in VS Code and in the GitHub commit view. For example, `README.md` refers to the project overview, while `mission-08-final-report/README.md` refers to this report. I recorded form submission separately so the report shows its actual status.

## 7. Evidence / files

- [Root README and mission index](../README.md)
- [Mission 2 Terminal notes](../mission-02-terminal/README.md)
- [Mission 3 system and permission observations](../mission-03-operating-system/README.md)
- [Python greeting program](../mission-04-programs/hello.py)
- [Python number converter](../mission-05-numbers-data/number_converter.py)
- [Mission 6 Git workflow and Pull Request details](../mission-06-git-github/README.md)
- [Mission 7 network observations](../mission-07-networking/README.md)
- [Commit history on main](https://github.com/bikramjitsil-code/digital-detective-8008/commits/main)

## 8. Commit details

Planned commit message: `Complete Digital Detective final report`

Final report push verification: I pushed the final report and the updated root README to `main`. I opened both files on GitHub and confirmed that my final edits were visible.

Google Form submission confirmation: Pending.