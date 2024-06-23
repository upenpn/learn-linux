# Command Line Cheatsheet

## Background Information

The command line, also known as the terminal or console, is a text-based interface for interacting with the operating system. It allows users to execute a wide range of commands, scripts, and programs to perform various tasks. Understanding and using command-line tools efficiently is essential for developers, system administrators, and anyone working in a Unix-like environment.

This cheatsheet provides a comprehensive overview of commonly used commands in the command line, along with their descriptions, examples, use cases, and explanations of key concepts.

---

## Command Overview

| Command                | Description                                       | Example Usage                                           | Background & Explanation                                  |
|------------------------|---------------------------------------------------|---------------------------------------------------------|---------------------------------------------------------|
| stdout (Standard Out)  | Display output to the terminal                    | `echo Hello World`                                      | Standard output (stdout) is the default stream where command-line programs display their output. The `echo` command is used to print text to stdout. Redirecting stdout with `>` or `>>` allows saving the output to a file. |
| stdin (Standard In)    | Receive input from a file or command              | `cat < input.txt`                                       | Standard input (stdin) is where command-line programs read input. Using `<` redirects stdin to read from a file instead of the keyboard. |
| stderr (Standard Error)| Display error messages                             | `ls /fake/directory 2> error.log`                       | Standard error (stderr) is a separate stream used for error messages. Redirecting stderr with `2>` allows capturing error output to a file. |
| pipe and tee           | Combine and redirect command output                | `ls -l | grep "file" | tee results.txt`                | Pipes (`|`) connect the stdout of one command to the stdin of another. The `tee` command allows displaying and saving command output simultaneously. |
| env (Environment)      | Display and manage environment variables          | `echo $PATH`                                            | Environment variables store information about the system environment. Using `echo $VAR` displays the value of a specific environment variable. |
| cut                    | Extract portions of text from files or input      | `cut -f 2 -d ":" file.txt`                              | The `cut` command extracts specific fields or characters from input based on delimiter or position. |
| paste                  | Merge lines from files or input                   | `paste -d ',' file1.txt file2.txt > merged.txt`          | The `paste` command combines lines from multiple files or inputs, with an optional delimiter. |
| head and tail          | Display the beginning or end of files             | `head -n 10 file.txt`                                   | `head` shows the start of a file, while `tail` shows the end. `-n` specifies the number of lines. |
| expand and unexpand    | Convert TABs to spaces or vice versa              | `expand file.txt > formatted.txt`                        | `expand` converts TABs to spaces, while `unexpand` does the reverse. |
| join and split         | Combine lines from files or split files           | `join -1 2 -2 1 file1.txt file2.txt > merged.txt`        | `join` merges lines based on common fields, while `split` divides files into smaller parts. |
| sort                   | Sort lines in files                                | `sort -r file.txt`                                      | `sort` arranges lines in alphabetical or numerical order. `-r` performs a reverse sort. |
| tr (Translate)         | Translate or delete characters in input           | `echo "hello" | tr '[:lower:]' '[:upper:]'`                  | `tr` translates or deletes characters based on specified rules. |
| uniq (Unique)          | Remove duplicate lines from sorted input          | `uniq -c sorted.txt > unique.txt`                        | `uniq` removes consecutive duplicate lines from sorted input. `-c` adds a count of occurrences. |
| wc and nl              | Count lines, words, and characters in files       | `wc -l file.txt`                                        | `wc` counts lines, words, and characters in a file. `-l` specifies counting lines only. |
| grep                   | Search files for patterns and text                | `grep -i "pattern" file.txt`                             | `grep` searches files for patterns using regular expressions. `-i` makes the search case-insensitive. |

---

## Command Details

Each command in the table above is explained briefly, along with background information and key concepts. For detailed usage and more examples, refer to the specific command's documentation or manual pages (`man` command in Unix-like systems).
