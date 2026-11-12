# 🐧 OPERATING SYSTEM LAB
## EXPERIMENT – 01: Linux Basics, Redirection & Process Management

**Student Name:** Anshu  
**Roll Number:** 2025A1R141  
**Department:** Computer Science & Engineering (CSE)  
**Semester:** 3rd  

---

## 1. AIM

To study and perform basic Linux commands, file and directory operations, input/output redirection, pipes, pattern searching, terminal text editors, and process management.

## 2. OBJECTIVES

- To understand basic Linux terminal commands.
- To create, copy, move and delete files and directories.
- To understand input and output redirection.
- To perform operations using pipes and filters.
- To search files and text using `find` and `grep`.
- To learn text editing using Vim and Nano.
- To monitor and manage processes in Linux.

## 3. REQUIREMENTS

- Operating System: Linux / Ubuntu
- Terminal: Linux Terminal
- Text Editors: Vim and Nano
- Basic knowledge of Linux commands.

---

## 4. DIRECTORY AND FILE OPERATIONS

### A. Navigation Commands

| Command | Description |
|---|---|
| `pwd` | Displays current directory |
| `cd` | Changes directory |
| `cd ..` | Moves one directory back |
| `cd ~` | Opens home directory |

**Practical:**
```bash
pwd
cd ~
mkdir OS_Lab
cd OS_Lab
```

### B. Directory Management

| Command | Description |
|---|---|
| `mkdir test` | Creates a directory |
| `mkdir -p a/b/c` | Creates nested directories |
| `mkdir -v demo` | Displays creation message |
| `mkdir -m 755 demo` | Creates directory with permissions |
| `rmdir demo` | Removes an empty directory |
| `rmdir -p a/b/c` | Removes empty parent directories |
| `rmdir -v demo` | Displays removal message |

**Practical:**
```bash
mkdir Experiment1
mkdir -p Linux/Commands
mkdir -v TestFolder
```

### C. Listing Files

```bash
ls
ls -l
ls -a
ls -h
ls -lah
```

**Description:** The `ls -lah` command displays all files, including hidden files, with detailed information and human-readable file sizes.

### D. File Creation and Updating

```bash
touch file1.txt
touch -c file1.txt
touch -t 202611121200 file1.txt
touch -d "2026-11-12 12:00" file1.txt
```

### E. Copying Files

```bash
cp file1.txt file2.txt
cp -r folder1 folder2
cp -i file1.txt file2.txt
cp -p file1.txt backup.txt
```

### F. Moving and Renaming Files

```bash
mv file1.txt newfile.txt
mv -i file1.txt folder/
mv -n file1.txt folder/
mv -v newfile.txt folder/
```

### G. Removing Files

```bash
rm -i file1.txt
rm -r folder1
```

**Note:** `rm -rf` can permanently remove files and directories without prompting. Never run it on important or unknown paths. Practise deletion only inside your test folder.

### H. Viewing File Contents

```bash
cat file1.txt
cat -n file1.txt
cat -b file1.txt
head -n 5 file1.txt
tail -n 5 file1.txt
```

---

## 5. INPUT AND OUTPUT REDIRECTION

Linux uses three standard streams:

| Stream | Number | Meaning |
|---|---:|---|
| stdin | 0 | Standard Input |
| stdout | 1 | Standard Output |
| stderr | 2 | Standard Error |

### Redirection Operators

| Operator | Purpose |
|---|---|
| `>` | Overwrites output into a file |
| `>>` | Appends output to a file |
| `2>` | Redirects error messages |
| `&>` | Redirects output and errors |
| `<` | Takes input from a file |

**Practical:**

```bash
echo "Hello Linux" > output.txt
echo "Operating System Lab" >> output.txt
cat output.txt
```

Redirect errors:

```bash
ls unknownfolder 2> error.txt
```

Redirect both output and errors:

```bash
ls . unknownfolder &> result.txt
```

Take input from a file:

```bash
sort < output.txt
```

---

## 6. PIPES AND LINUX UTILITIES

A pipe (`|`) sends the output of one command as input to another command.

### Important Commands

| Command | Description |
|---|---|
| `sort` | Sorts lines alphabetically |
| `uniq` | Removes adjacent duplicate lines |
| `tee` | Displays and saves output |
| `xargs` | Converts input into command arguments |

**Practical:**

```bash
printf "banana\napple\nbanana\nmango\n" > fruits.txt

sort fruits.txt
sort fruits.txt | uniq
sort fruits.txt | tee sorted.txt
cat fruits.txt | xargs echo
```

---

## 7. PATTERN SEARCHING USING GREP

The `grep` command searches for specific text or patterns inside files.

| Option | Description |
|---|---|
| `-i` | Ignores uppercase/lowercase |
| `-v` | Displays non-matching lines |
| `-c` | Counts matching lines |
| `-w` | Matches complete words |
| `-n` | Displays line numbers |

**Practical:**

```bash
grep "Linux" file1.txt
grep -i "linux" file1.txt
grep -v "Linux" file1.txt
grep -c "Linux" file1.txt
grep -w "OS" file1.txt
grep -n "Linux" file1.txt
```

---

## 8. FINDING FILES USING FIND

The `find` command searches for files and directories.

| Option | Description |
|---|---|
| `-name` | Searches by filename |
| `-iname` | Case-insensitive filename search |
| `-size` | Searches by file size |
| `-user` | Searches by owner |
| `-empty` | Finds empty files/directories |

**Practical:**

```bash
find . -name "*.txt"
find . -iname "*.TXT"
find . -size +1M
find . -user "$USER"
find . -empty
```

---

## 9. TERMINAL TEXT EDITORS

### A. Nano Editor

Nano is a simple, modeless text editor.

**Open a file:**
```bash
nano file1.txt
```

Important shortcuts:

- `Ctrl + O` – Save file
- `Ctrl + X` – Exit editor
- `Ctrl + W` – Search text
- `Ctrl + K` – Cut line
- `Ctrl + U` – Paste line

### B. Vim Editor

Vim is a modal text editor.

**Open a file:**
```bash
vim file1.txt
```

Important commands:

| Command | Function |
|---|---|
| `i` | Insert mode |
| `Esc` | Normal mode |
| `:w` | Save file |
| `:q` | Exit |
| `:wq` | Save and exit |
| `:q!` | Exit without saving |
| `/word` | Search word |
| `dd` | Delete current line |

---

## 10. PROCESS MANAGEMENT

A process is a program currently running in the operating system.

### A. Job Control

```bash
jobs
bg
fg
```

### B. Process Inspection

```bash
ps
ps -e
ps -ef
ps -p $$
ps aux
```

### C. Signal Handling

| Command | Description |
|---|---|
| `kill -15 PID` | Requests process termination (SIGTERM) |
| `kill -9 PID` | Forces process termination (SIGKILL) |
| `kill -STOP PID` | Pauses a process |
| `kill -CONT PID` | Resumes a stopped process |

For practice, create a test process:

```bash
sleep 300 &
jobs
```

Use the PID of this test process to practise process signals, and then clean up the test process.

### D. CPU Priority Management

```bash
nice -n 10 sleep 100
renice 5 -p PID
```

### E. Live Process Monitoring

```bash
top
```

Press `q` to exit the top command.

---

## 11. PRACTICAL EXECUTION

All commands should be executed in the Ubuntu/Linux terminal.

Create a lab directory:

```bash
mkdir -p ~/OS_Lab/Experiment1
cd ~/OS_Lab/Experiment1
```

Create sample files:

```bash
touch file1.txt file2.txt
echo "Welcome to Linux Operating System Lab" > file1.txt
cat file1.txt
```

Perform directory operations, redirection, pipes, searching and process-management commands using the examples given above.

## 12. OBSERVATION

The following observations were made:

1. Linux commands are useful for file and directory management.
2. Redirection helps save command output into files.
3. Pipes allow multiple commands to work together.
4. Grep and find make searching easier.
5. Vim and Nano provide terminal-based text editing.
6. Process management commands help inspect and control running processes.

## 13. RESULT

Successfully studied and practised Linux basics, directory and file operations, I/O redirection, pipes, searching utilities, terminal editors and process management commands.

## 14. CONCLUSION

This experiment provided practical knowledge of Linux command-line operations. It helped in understanding how files, directories, input/output streams and running processes are managed in a Linux operating system.

---

**Experiment Status:** Completed / To be verified in Linux Terminal

**Submitted By:** Anshu  
**Department:** Computer Science & Engineering  
**Semester:** 3rd
