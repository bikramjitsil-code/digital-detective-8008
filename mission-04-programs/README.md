# Mission 4 — How programs run

## 1. Task / objective

Create and run a simple Python program and compare how compilers and interpreters translate or execute programs.

## 2. Work completed

### Task 4.1 — Create and run a Python program

File: `hello.py`

```python
print("Hello from Python")
```

The `print()` function displays the string supplied inside its parentheses.

Command, run from this mission folder:

```bash
python3 hello.py
```

Expected output:

```text
Hello from Python
```

Actual output and execution result: [I ran `python3 hello.py` from the Mission 4 folder. Terminal displayed `Hello from Python` on one line and then returned to the prompt. The output matched the message inside `print()`.]

### Task 4.2 — Compare compiler and interpreter

| Point | Compiler | Interpreter |
|---|---|---|
| When translation / execution happens | Translates source code into another form before that translated output is executed | Executes program instructions at runtime |
| Typical output | Object code, machine code, bytecode or another target form | Program results; it does not necessarily create a standalone executable |
| One example | Clang compiling C source code | CPython executing Python code |
| One advantage | Native compilation can produce efficient executable programs | Convenient for interactive experiments and quick testing |

A compiler translates source code into another form that can be executed or processed later. An interpreter executes instructions at runtime. Compilation and interpretation can be combined in the same language implementation. For example, CPython compiles Python source into bytecode and executes that bytecode using its interpreter.

## 3. Commands / tools used

| Command / tool | Purpose |
|---|---|
| VS Code | Create and save `hello.py` |
| `python3 hello.py` | Run the Python program |
| `print()` | Display the message |
| Git and GitHub | Record and publish the mission |

## 4. My understanding

Source code is text containing instructions written in a programming language. It needs a language implementation to translate or execute those instructions.

Saving the program creates the source file. Running `python3 hello.py` asks Python to execute it.

Compiler and interpreter describe approaches to processing programs, and real implementations can use both.

## 5. Difficulties faced

[No major difficulties.]

## 6. How I resolved them

[Not applicable.]

## 7. Evidence / files

- `README.md`.
- `hello.py`.
- Actual execution observation recorded above.

## 8. Commit details

Planned commit message: `Compare compilers and interpreters`

Commit, push and GitHub verification: [RECORD ACTUAL RESULT]