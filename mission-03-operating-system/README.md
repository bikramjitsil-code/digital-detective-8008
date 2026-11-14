# Mission 3 — Understand the operating system

## 1. Task / objective

Explore operating-system information, storage and running processes. Understand absolute and relative paths, file permissions and the main responsibilities of an operating system.

## 2. Work completed

### Task 3.1 — Explore my operating system

| Information explored | What it tells me | What I observed |
|---|---|---|
| Operating system details | Shows the installed macOS version. | I ran `sw_vers -productVersion` and found that my Mac was running macOS 27.2. |
| Current account identity | Shows which account is running my Terminal commands. | When I ran `whoami`, Terminal displayed my account’s short username. I recorded it as `[redacted]` for privacy. |
| Available and used storage | Shows storage usage on the volume containing my project folder. | I ran `df -h .` from my project folder. The `Used` column showed 272 GiB and the `Avail` column showed 630 GiB. |
| System activity snapshot | Shows process states, CPU usage and memory usage at the time of the check. | I ran `top -l 1 -n 5` and saw 861 processes in total. At that moment, 2 were running, 859 were sleeping and the CPU was 84.71% idle. |
Commands:

- `sw_vers`: macOS version information.
- `whoami`: current account name.
- `df -h .`: storage information for the filesystem containing the current directory.
- `top -l 1 -n 5`: one macOS activity sample with a limited process listing.

### Task 3.2 — Understand processes

A process is a running instance of a program. The operating system manages its execution and resources.

PID means process identifier. It is a number used to identify a process.

I used `ps -ax` to inspect the running process list after opening an application.

Two processes actually observed:

### Task 3.2 — Understand processes

A process is a running instance of a program. When I entered `top -l 1 -n 5` in Terminal, I could see both `top` and `zsh` in the process list.

The `PID` column shows the process identifier. macOS uses this number to identify each process.

| Process | PID | State | What I observed |
|---|---:|---|---|
| `top` | 11139 | running | This was the program displaying system activity. I could see it in its own process list. |
| `zsh` | 10030 | sleeping | This was the shell where I entered the command. It was waiting while `top` ran. |

I also noticed that the `PPID` (parent process ID) of `top` was 10030. This matched the PID of `zsh`, showing that my shell had started `top`.
### Task 3.3 — Paths and permissions

An absolute path identifies a location starting from the filesystem root.

Privacy-safe example:

`/Users/[redacted]/Documents/digital-detective-8008/README.md`

A relative path identifies a location starting from the current directory.

Example from the project root:

`mission-03-operating-system/README.md`

When I enter a subfolder using `cd`, the current working directory changes. `pwd` displays the updated location.

Navigation observation: [I started in `digital-detective-8008`. After I ran `cd mission-03-operating-system`, `pwd` showed that my path now ended in `digital-detective-8008/mission-03-operating-system`. When I ran `cd ..` and checked with `pwd` again, I was back in `digital-detective-8008`.]

I inspected a practice file using:

```bash
ls -l mission-02-terminal/terminal-practice/notes.txt
```

Actual permission string: [ `-rw-r--r--@`]

[I checked the owner’s permissions by reading the `rw-` immediately after the first `-`. This showed that I could read and edit `notes.txt`. The execute permission was absent.]

| Permission | Meaning for a regular file | Example |
|---|---|---|
| `r` — Read | Allows its contents to be read | Opening a text file |
| `w` — Write | Allows its contents to be modified | Editing text |
| `x` — Execute | Allows execution when the file is a valid executable or script | Running an executable script |

For a directory, execute permission allows traversal/access to entries.

The first character of the permission string identifies the file type. The next three characters represent the owner's permissions.

Owner can read: [Yes]

Owner can write: [Yes]

Owner can execute: [No]

No system permission changes are required.

### Task 3.4 — Operating-system responsibilities

| OS responsibility | Explanation | Example |
|---|---|---|
| Process management | Creates, schedules and manages running processes | Shares processor time between a browser and an editor |
| Memory management | Allocates and manages memory used by programs | Provides RAM for an application's working data |
| Device management | Coordinates access to hardware through system components and drivers | Receives keyboard input and sends audio to speakers |
| File management | Organises and manages access to stored files and directories | Creates, reads and saves documents |
| User interface / shell | Provides ways for users to interact with the computer | Desktop windows and command-line shells |
| Security and permissions | Controls access to files and other resources | Prevents unauthorised modification of protected files |

## 3. Commands / tools used

`sw_vers`, `whoami`, `df -h .`, `top -l 1 -n 5`, `ps -ax`, `pwd`, `cd` and `ls -l`.

VS Code is used for documentation. Git and GitHub record and publish the work.

## 4. My understanding

The operating system provides services that allow applications to use hardware and stored information.

A program stored on disk is different from a process that is currently running.

Absolute paths identify locations from the root, while relative paths depend on the current directory.

File permissions determine which operations an account is allowed to perform.

## 5. Difficulties faced

[When I tried to check the permissions of `notes.txt`, Terminal showed “No such file or directory”. At first, I thought the permission string I saw in the project folder belonged to `notes.txt`, but it belonged to the root `README.md`.]

## 6. How I resolved them

[I used `find ./mission-02-terminal -type f` and saw that the only file there was `README.md`. I created the `terminal-practice` folder and added `notes.txt` inside it. Then I used `ls -l` to check the correct file. Its permission string was `-rw-r--r--@`, which showed that the owner could read and edit the file but could not execute it directly.]

## 7. Evidence / files

- `mission-03-operating-system/README.md`.
- Privacy-safe system and process observations.
- Path examples and permission interpretation.
- Operating-system responsibilities table.

## 8. Commit details

Planned commit message: `Document operating system and file management`

Commit, push and GitHub verification: [I pushed Mission 3 to `main` and verified that my operating-system observations and file-permission results were visible on GitHub.]