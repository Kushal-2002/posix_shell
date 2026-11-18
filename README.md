# Advanced Operating Systems – Assignment 2

A modular UNIX-like shell written in **C++** for the AOS course.  
It supports command parsing, pipelines, I/O redirection, background execution (`&`), Ctrl+C/Ctrl+Z forwarding to the foreground process, history, and tab-autocomplete.

---

## 📂 Project Structure

| File              | Description |
|-------------------|-------------|
| `main.cpp`        | Entry point, initializes shell, REPL loop |
| `shell_core.cpp`  | Core execution logic: parsing & dispatch |
| `pipeline.cpp`    | Pipeline execution (`cmd1 | cmd2 | ...`) |
| `io.cpp`          | I/O redirection (`<`, `>`, `>>`) |
| `builtins.cpp`    | Built-in commands (`cd`, `pwd`, `exit`, `history`, …) |
| `signals.cpp`     | Signal handlers (`SIGINT`, `SIGTSTP`) |
| `history.cpp`     | Persistent history (`.shell_command_history`) |
| `autocomplete.cpp`| Tab-completion logic |
| `utils.cpp`       | Utility functions (raw mode, tokenizer, command splitting, helpers) |
| `shell.h`         | Shared declarations |
| `makefile`        | Build instructions |
| `README.md`       | Documentation |

---

## ⚙️ Build & Run

### Prerequisites
- Linux/Unix system  
- `g++` (C++17 or later)  

### Build
make

### execute
./shell

## 📑 Functions by File

### `main.cpp`
- main()

### `shell_core.cpp`
- input_with_history()
- execute_command()

### `pipeline.cpp`
- execute_pipeline()

### `io.cpp`
- system_command_handler()
- parse_redirection()
- apply_redirection()

### `builtins.cpp`
- pwd_handler()
- cd_handler()
- echo_handler()
- permission_checker()
- case_insensitive_cmp()
- ls_helper()
- ls_handler()
- pinfo_handler()
- search_handler()

### `signals.cpp`
- handle_sigtstp()
- handle_sigint()

### `history.cpp`
- load_history()
- save_history()
- add_history()

### `autocomplete.cpp`
- list_files()
- get_path_commands()
- common_prefix()
- autocomplete()

### `utils.cpp`
- enable_raw_mode()
- disable_raw_mode()
- tokenizer()
- preprocess()
- display()
- split_into_commands()
- is_internal()




