# Command Line Cheatsheet

| Command          | Description                                                      | Examples / Use Cases                                                                                       |
|------------------|------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| **Shell**        |                                                                  |                                                                                                            |
| `bash`           | Launches the Bash shell.                                         | - Default shell on many Linux/macOS systems.                                                               |
| `zsh`            | Launches the Zsh shell.                                          | - Enhanced version of the Bourne shell. <br> - Advanced tab completion, theme support, plugin ecosystem.    |
| `fish`           | Launches the Fish shell.                                         | - Modern syntax, auto-suggestions, syntax highlighting. <br> - User-friendly and intuitive.                 |
| **pwd**          | Print Working Directory                                          | `pwd`: Print current working directory. <br> `pwd -P`: Outputs resolved symbolic links.                      |
| **cd**           | Change Directory                                                 | `cd /path/to/dir`: Change current directory. <br> `cd ..`: Change to parent directory.                       |
| **ls**           | List Directory Contents                                          | `ls`: List current directory contents. <br> `ls -l`: List detailed information.                             |
| **mkdir**        | Make Directory                                                   | `mkdir new_dir`: Create a new directory. <br> `mkdir -p dir1/dir2`: Create nested directories.              |
| **rm**           | Remove                                                           | `rm file.txt`: Remove a file. <br> `rm -r dir`: Remove a directory recursively.                            |
| **cp**           | Copy                                                             | `cp file1 file2`: Copy a file. <br> `cp -r dir1 dir2`: Copy directories recursively.                       |
| **mv**           | Move                                                             | `mv file dir`: Move a file to a directory. <br> `mv file new_file`: Rename a file.                          |
| **touch**        | Create/Update Timestamps                                         | `touch file`: Create a new file. <br> `touch -t timestamp file`: Update file timestamp.                      |
| **cat**          | Concatenate and Display Contents                                 | `cat file.txt`: Display file contents. <br> `cat file1 file2 > combined.txt`: Concatenate and combine files. |

**References and Explanations:**

- **Recursively (`-r` option):** This means performing an operation on a target and all of its contents, including subdirectories, sub-subdirectories, and so on. For example, `rm -r dir` will delete the directory "dir" and all its contents.
  
- **Symbolic Links:** These are special types of files that act as shortcuts or references to other files or directories in the file system. When using `pwd -P`, symbolic links are resolved to show the actual path.

- **Detailed Information (`-l` option):** When using `ls -l`, you get a detailed listing of files and directories, including permissions, owner, size, and modification date.

- **Forcefully (`-f` option):** This option, used with `rm -f`, forces the removal of a file without prompting for confirmation, which can be useful in scripting or automation tasks.

- **Prompt Before Overwriting (`-i` option):** When using `cp -i`, a prompt appears before overwriting an existing file, helping to prevent accidental data loss.

