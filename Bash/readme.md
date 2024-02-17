# Bash

## The general syntax of a shell command
```bash
$ ls -fa /
```

where `$` is **prompt** sign `ls` is the **command** `-fa` is **option/flag** and `/` is **arguments**.


 
## Working with the files and directories

| Command | Description|
|:--:|:-----------|
| / | the root directory of the file system |
| .. | parent directory of the current directory |
| whoami | shows the current user of the system |
| pwd | shows the present working directory |
| cd x | change the directory to “x” |
| cd .. | goes up a directory which is the parent directory of the current directory (..) is the parent directory |
| ls | shows all the files of the current directory |
| ls -a -h -t -l -r -F | -a is used to output hidden files, -h adds up the human readability to the output, -t shows the files in the order of most recently modified, -l is used to get more details about the files such as when it was created or modified, -r shows the files in reverse order, -F formats the files and shows the filetype such as /directory .file, etc |
| mkdir dir1 dir2 . . . | used to create directories  |
| mkdir -p parentdir/childdir/ | “-p” to create parent and child directories. |
| rmdir -p parentdir/childdir/ | to delete these parent-child directories |
| file filename | returns the information about the file |
| wc -l -m -w | wc is the ‘word count’ command: it counts the number of lines, words, and characters in files (returning the values in that order from left to right), -l for the number of lines per file, -m for the number of characters, -w for number of words per file |
| wc -l *.pdb > file | This command prints nothing on screen because all the count that comes from wc is redirected to the file using > symbol |
| touch | used to create files |
| touch file1 file2 file3 | to create multiple files |
| rm filename | delete files or multiple files |
| rm -i filename | -i prompts for deletion |
| rm -rf dirname | removes recursively all the files of a directory, -rf means recursively force |
| cp file1 file2 | to copy file1 and create file2 |
| cp filename /path | to copy a file into a specific directory |
| cp -r dirname dirnewname | to copy files of a directory into a new directory, this creates a new directory with a new name with all the files inside it. |
| mv file1 file2 | used to rename file1 into file2 |
| mv file /destination/newname | to move a file to the destination given with the name |
| head file | prints the first ten lines of a file (head -5 file) where -5 is the number of lines  |
| tail filename | prints the last 10 lines of a file |
| cat filename | concatenates and prints on the terminal. this prints the full file on the terminal |
| echo “text” | displays a text on the terminal  |
| echo “text” > file | puts the data into the file |
| cat file1 file2 > file3 | extracts data from file1 and file and adds into file3 |
| cat > file  | creates a file and writes in the file. This command helps by writing directly into the file using the terminal. Use ctrl + D to stop writing. |
| cat file1 > file2 | copies file1 and create file2 with same data from file1 |
| more file | shows data per page |
| less file | opposite of more |

## Working with the system

| Command | Description |
|:--:|:-----------|
| uptime | shows the up time of the system and users |
| free | shows the information about the memory usage of the system |
| ps -a | shows the processes currently running on the system |
| df -h  | shows disk usage of files |
| sudo fdisk -l | used to manipulate system partition tables |
| lsblk | shows the list of all the blocks of partitions |
| top, htop | displays linux processes, better version of top |
| ifconfig | configuring network interface, shows network information |
| ip | shows/manipulates network devices etc. |

## Sudo related

| Command | Description |
|:--:|:-----------|
| sudo | “super user do” gives the admin user power |
| apt | advanced package manager tool is a package manager tool for Debian-based distros |
| sudo apt update | updates cache of available packages of your OS, shows the packages that can be upgraded |
| sudo apt upgrade | upgrades the packages |
| sudo apt —upgradable | shows the list of packages that can be upgraded |
| sudo apt search packagename | searches the package  |
| sudo apt remove  | to remove the package from the system |

## Filtering Output (Advanced)


| Command | Description |
|:--:|:-----------|
| sort -n | sorts the data of the file in order, -n sorts the file in an increasing order |
| command > [file] | redirects a command’s output to a file (overwriting any existing content) |
| [firstcommand] | [secondcommand] | it is a pipeline: the output of the first command is used as the input to the second. |
| command >> [file]  | appends a command’s output to a file. |