# The Digital Detective

The Digital Detective is my Diwali independent learning assignment. I used my MacBook to explore how a computer handles input, runs programs, stores files and communicates over a network. I documented each activity in its own mission folder and used Git and GitHub to track my work.

## Mission index

| Mission | Topic | Work included |
|---|---|---|
| [0 — Create your GitHub workspace](mission-00-setup/README.md) | Repository setup | Project folders, tool versions and the first Git commit |
| [1 — Know your computer](mission-01-computer-basics/README.md) | Computer fundamentals | Input, processing, output and storage (IPOS), hardware and software, and everyday computer systems |
| [2 — Become comfortable with the Terminal](mission-02-terminal/README.md) | Terminal and file management | Navigation, creating and editing files, backups, command flags, pipes and package managers |
| [3 — Understand the operating system](mission-03-operating-system/README.md) | Operating systems | macOS observations, running processes, storage, paths and file permissions |
| [4 — How programs run](mission-04-programs/README.md) | Program execution | A Python greeting program and a comparison of compilers and interpreters |
| [5 — Numbers and data](mission-05-numbers-data/README.md) | Data representation | Manual conversions, Python verification, a number converter, and ASCII and UTF-8 text encoding |
| [6 — Git and GitHub](mission-06-git-github/README.md) | Version control | Staging, committing, reviewing history, creating the `update-about` branch and opening a Pull Request |
| [7 — How computers communicate](mission-07-networking/README.md) | Computer networks | Network types, DNS, routers, protocols, packet switching, connectivity tests and how a website opens |
| [8 — Final report and submission](mission-08-final-report/README.md) | Final review | Mission status, corrections, evidence, final checklist and submission details |

## Tools used

| Tool | Version or purpose |
|---|---|
| macOS | 27.2 |
| Python | 3.14.5 |
| Git | 2.54.0 (Apple Git-157) |
| Terminal | Run commands and inspect their output |
| Visual Studio Code | Edit Python programs and Markdown files |
| GitHub | Publish commits and review changes through a Pull Request |

## How to run the number converter

The [number converter](mission-05-numbers-data/number_converter.py) takes a positive decimal integer and displays its binary and hexadecimal representations.

Open Terminal in the main `digital-detective-8008` folder and run:

```bash
cd mission-05-numbers-data
python3 number_converter.py
```

Example with the input `25`:

```text
Enter a positive decimal integer: 25
Binary: 0b11001
Hexadecimal: 0x19
```

Python uses `0b` for binary and `0x` for hexadecimal. Both results represent the same value, decimal 25. The [Mission 5 README](mission-05-numbers-data/README.md) contains the manual calculations and test table.

## How to run the greeting program

From the main `digital-detective-8008` folder, run:

```bash
python3 mission-04-programs/hello.py
```

Expected output:

```text
Hello from Python
```

## Workflow

I documented each mission in its own README and used separate commits to record the work for each mission. When I found a mistake, I could correct it in a later commit and review both changes in the [commit history](https://github.com/bikramjitsil-code/digital-detective-8008/commits/main).

For Mission 6, I used the `update-about` branch to propose adding my learning summary to this README. Pull Request #1 was created and merged into `main`. The [Mission 6 README](mission-06-git-github/README.md) records the Pull Request details.

## My Learning

- **Checking my work with Git:** When an edit was missing from GitHub, I opened the commit and saw that only the setup README had changed. I learned to check the full file path, save the edit and review `git status` before committing.
- **Reading a permission string:** My practice file showed `-rw-r--r--@`. The owner permissions were `rw-`, which told me I could read and edit `notes.txt`. Execute permission was absent.
- **Connecting a shell command to a process:** When I ran `top`, its parent process ID matched the process ID of `zsh`. I could see from those two numbers that my shell had started `top`.
- **Understanding number systems:** I converted 25 to binary by hand and got `11001`. Seeing Python display `0b11001` helped me understand how the prefix identifies the base.
- **Connecting DNS and ping:** My DNS lookup returned two IPv4 addresses for `example.com`, and `ping` used one of them. All four requests received replies, with 0% packet loss and an average round-trip time of 41.769 ms.

## Progress and submission

| Item | Status |
|---|---|
| Missions 0–7 | Completed |
| Mission 8 | Final report and repository verification completed. The final checklist is recorded in the [Mission 8 README](mission-08-final-report/README.md). |
| Google Form submission | Pending |

Repository URL: https://github.com/bikramjitsil-code/digital-detective-8008
