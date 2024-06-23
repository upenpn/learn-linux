Text-Fu


## Learn basic text manipulation and navigation.

| Command                | Description                                       | Example Usage                                           | Example(s)                                             | Explanation                                                                                                                                                                                                                                                                                                          |
|------------------------|---------------------------------------------------|---------------------------------------------------------|---------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| stdout (Standard Out)  | Displays output to the terminal.                  | `echo "Hello, World!"`                                  | `echo "Hello, World!" > hello.txt`<br>`echo "Goodbye, World!" > goodbye.txt`<br>`ls -l > directory_contents.txt` | The first example prints "Hello, World!" to the terminal. The second and third examples redirect the output of commands to files, creating or overwriting the specified files with the output.                                                                                                                   |
| stdin (Standard In)    | Receives input from a file or command.            | `cat < input.txt`                                       | `cat < file.txt`<br>`sort < unsorted.txt`<br>`head < data.log` | The first example uses input redirection to send the contents of `input.txt` as input to the `cat` command. The other examples demonstrate input redirection with different commands and files.                                                                                                                      |
| stderr (Standard Error)| Displays error messages.                           | `ls /fake/directory 2> error.log`                       | `ls /nonexistent_directory 2> error.log`<br>`grep pattern non_existent_file 2> error.log`<br>`./script_with_error.sh 2> error.log` | These examples redirect error messages (stderr) to an error log file (`error.log`). They handle errors gracefully by capturing error messages separately from regular output.                                                                                                                                    |
| pipe and tee           | Combines and redirects command output.             | `ls -l | grep "file"`                                   | `cat file1.txt | tee file2.txt`<br>`ps aux | grep "process"`<br>`command1 | command2 | tee output.txt` | These examples show how to use pipes (`|`) and the `tee` command to combine, redirect, and duplicate command output. Pipes pass the output of one command as input to another, while `tee` writes to a file and also sends the output to the terminal.                                                       |
| env (Environment)      | Displays and manages environment variables.        | `echo $PATH`                                            | `echo $HOME`<br>`echo $USER`<br>`env`                    | These examples demonstrate accessing and displaying environment variables such as PATH, HOME, and USER. The `env` command shows all environment variables set in the current shell session.                                                                                                                      |
| cut                    | Extracts portions of text from files or input.     | `cut -f 2 -d ":" file.txt`                              | `echo "John:Doe" | cut -d ":" -f 2`<br>`cut -c 1-5 file.txt`<br>`cut -f 1 -d "," data.csv` | These examples illustrate cutting and extracting specific fields or characters from input based on delimiter or position. The `cut` command is useful for processing structured data like CSV files or text with consistent delimiters.                                                    |
| paste                  | Merges lines from files or input.                  | `paste -d ',' file1.txt file2.txt > merged.txt`         | `paste -s file.txt`<br>`paste -d '\t' file1.txt file2.txt > merged.txt` | The examples show merging lines from files using default or custom delimiters (`-d`) and options (`-s`). The `paste` command is handy for combining text data horizontally from multiple sources.                                                        |
| head and tail          | Displays the beginning or end of files.            | `head -n 10 file.txt`                                   | `tail -n 20 file.txt`<br>`tail -f logfile.txt`<br>`head -c 1000 largefile.txt` | These examples demonstrate displaying the first or last lines, or continuously monitoring file changes with `tail -f`. The `head` and `tail` commands are useful for previewing or monitoring log files or large text files.                                     |
| expand and unexpand    | Converts TABs to spaces or vice versa.            | `expand file.txt > formatted.txt`                       | `expand -t 2 file.txt > formatted.txt`<br>`unexpand -t 4 file.txt > formatted.txt` | These examples show converting TAB characters to spaces (`expand`) or spaces to TABs (`unexpand`) in text files. Adjusting tab stops (`-t`) controls the spacing behavior, useful for formatting text data for display or processing.                           |
| join and split         | Combines lines from files or splits files.         | `join -1 2 -2 1 file1.txt file2.txt > merged.txt`       | `split -l 1000 bigfile.txt`<br>`split -b 1M bigfile.txt`<br>`join -t "," file1.csv file2.csv` | The examples demonstrate combining lines from files based on matching fields (`join`) or splitting large files into smaller parts (`split`). These commands are handy for data manipulation and management tasks.                                    |
| sort                   | Sorts lines in files.                             | `sort file.txt`                                         | `sort -r file.txt`<br>`sort -k 2 file.txt`<br>`sort -n data.txt` | The examples show sorting lines in files alphabetically or numerically (`-r` for reverse, `-k` for specific field). Sorting is useful for organizing data for analysis or presentation, or preparing data for further processing.                             |
| tr (Translate)         | Translates or deletes characters in input.         | `echo "hello" | tr '[:lower:]' '[:upper:]'`              | `echo "hello 123" | tr -d '[:digit:]'`<br>`echo "hello" | tr 'l' 'j'`<br>`echo "hello" | tr -s ' ' '*'` | These examples illustrate character translation or deletion (`tr -d`) based on character sets or specific characters. The `tr` command