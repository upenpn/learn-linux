Text-Fu
Learn basic text manipulation and navigation.

## Background Information

The command line, also known as the terminal or console, is a text-based interface for interacting with the operating system. It allows users to execute a wide range of commands, scripts, and programs to perform various tasks. Understanding and using command-line tools efficiently is essential for developers, system administrators, and anyone working in a Unix-like environment.

This cheatsheet provides a comprehensive overview of commonly used commands in the command line, along with their descriptions, examples, use cases, and explanations of key concepts.

---

## Command Overview
| Command                | Description                                       | Example Usage                                           | Example(s) |
|------------------------|---------------------------------------------------|---------------------------------------------------------|------------|
| stdout (Standard Out)  | Displays output to the terminal.                  | `echo "Hello, World!"`                                  | `echo "Hello, World!" > hello.txt`<br>`echo "Goodbye, World!" > goodbye.txt`<br>`ls -l > directory_contents.txt` |
| stdin (Standard In)    | Receives input from a file or command.            | `cat < input.txt`                                       | `cat < file.txt`<br>`sort < unsorted.txt`<br>`head < data.log` |
| stderr (Standard Error)| Displays error messages.                           | `ls /fake/directory 2> error.log`                       | `ls /nonexistent_directory 2> error.log`<br>`grep pattern non_existent_file 2> error.log`<br>`./script_with_error.sh 2> error.log` |
| pipe and tee           | Combines and redirects command output.             | `ls -l | grep "file"`                                   | `cat file1.txt | tee file2.txt`<br>`ps aux | grep "process"`<br>`command1 | command2 | tee output.txt` |
| env (Environment)      | Displays and manages environment variables.        | `echo $PATH`                                            | `echo $HOME`<br>`echo $USER`<br>`env` |
| cut                    | Extracts portions of text from files or input.     | `cut -f 2 -d ":" file.txt`                              | `echo "John:Doe" | cut -d ":" -f 2`<br>`cut -c 1-5 file.txt`<br>`cut -f 1 -d "," data.csv` |
| paste                  | Merges lines from files or input.                  | `paste -d ',' file1.txt file2.txt > merged.txt`         | `paste -s file.txt`<br>`paste -d '\t' file1.txt file2.txt > merged.txt` |
| head and tail          | Displays the beginning or end of files.            | `head -n 10 file.txt`                                   | `tail -n 20 file.txt`<br>`tail -f logfile.txt`<br>`head -c 1000 largefile.txt` |
| expand and unexpand    | Converts TABs to spaces or vice versa.            | `expand file.txt > formatted.txt`                       | `expand -t 2 file.txt > formatted.txt`<br>`unexpand -t 4 file.txt > formatted.txt` |
| join and split         | Combines lines from files or splits files.         | `join -1 2 -2 1 file1.txt file2.txt > merged.txt`       | `split -l 1000 bigfile.txt`<br>`split -b 1M bigfile.txt`<br>`join -t "," file1.csv file2.csv` |
| sort                   | Sorts lines in files.                             | `sort file.txt`                                         | `sort -r file.txt`<br>`sort -k 2 file.txt`<br>`sort -n data.txt` |
| tr (Translate)         | Translates or deletes characters in input.         | `echo "hello" | tr '[:lower:]' '[:upper:]'`              | `echo "hello 123" | tr -d '[:digit:]'`<br>`echo "hello" | tr 'l' 'j'`<br>`echo "hello" | tr -s ' ' '*'` |
| uniq (Unique)          | Removes duplicate lines from sorted input.        | `sort file.txt | uniq`                                   | `uniq -c sorted.txt > unique.txt`<br>`sort file.txt | uniq -d`<br>`sort -n data.txt | uniq -c` |
| wc and nl              | Counts lines, words, and characters in files.     | `wc -l file.txt`                                        | `wc -w words.txt`<br>`nl file.txt`<br>`wc -c data.txt` |
| grep                   | Searches files for patterns and text.             | `grep "pattern" file.txt`                               | `grep -i "pattern" file.txt`<br>`grep -r "pattern" directory/`<br>`ls -l | grep "file" | tee results.txt` |
