# Learn command line

Please follow and complete the free online [Bash Scripting Tutorial](https://ryanstutorials.net/bash-scripting-tutorial/) or [Codecademy's Learn the Command Line](https://www.codecademy.com/learn/learn-the-command-line). These are helpful tutorials. You should be able to go through these in a couple of hours.

**Note:** Bash is not installed on a PC. Rather, PC users must install Cygwin. Once Cygwin has been installed, the command line interface witll _emulate_ bash. You can find all information regarding Cygwin [here](https://www.cygwin.com/).

---

### Q1.  Cheat Sheet of Commands  

Here's a list of items with which you should be familiar:  
* show current working directory path
* creating a directory
* deleting a directory
* creating a file using `touch` command
* deleting a file
* renaming a file
* listing hidden files
* copying a file from one directory to another

Make a cheat sheet for yourself: a list of at least **ten** commands and what they do.  (Use the 8 items above and add a couple of your own.)  

Command | Behaviour
--------|----------
`pwd`| print current working directory
`mkdir` 'dirname' | create a new directory 'dirname' in the current directory
`rmdir` 'dirname' | remove directory 'dirname' if present
`touch` 'filename' | create a new file 'filename' in the current directory
`rm` 'filename' | remove a file 'filename' in the current directory if present
`mv` 'oldfilename''newfilename' | change the name of the file '-oldfilename' into '-newfilename'
`ls -a` ' | list all files in a directory including hidden files
`cp` 'filename''newdirectory' | copy '-filename' into '-newdirectory'
`vi` 'filename' | open 'filename' in vi editor
`wget` 'urlname' | copy url 'urlename' in the current directory


---

### Q2.  List Files in Unix   

What do the following commands do:  
`ls`  
`ls -a`  
`ls -l`  
`ls -lh`  
`ls -lah`  
`ls -t`  
`ls -Glp`  

Command | Behaviour
--------|----------
`ls`| list all files in current directory
`ls -a`| list all files in current directory, including hidden files
`ls -l`| list all files in current directory, using a long listing format
`ls -lh`| list all files in current directory, using a long listing format, in a human readable format
`ls -lah`| list all files in current directory, including hidden files, using a long listing format, in a human readable format
`ls -t`| list all files in current directory, sorted by modification time
`ls -Glp`| list all files in current directory, inhibiting display of group information, using a long listing format,appending indicator(one of /@=&#124;)

---

### Q3.  More List Files in Unix  

Explore these other [ls options](http://www.techonthenet.com/unix/basic/ls.php) and pick 5 of your favorites:

Command | Behaviour
--------|----------
`ls -x`| Displays files as rows across the screen.
`ls -R`| Displays subdirectories as well
`ls -c`| Displays files by file timestamp
`ls -u`| Displays files by the file access time
`ls -m`| Displays the names as a comma-separated list

---

### Q4.  Xargs   

What does `xargs` do? Give an example of how to use it.


`xargs` command is designed to construct argument lists and invoke other utility. `xargs` reads items from the standard input or pipes, delimited by blanks or newlines, and executes the command one or more times with any initial-arguments followed by items read from standard input. Blank lines on the standard input are ignored.

Example:

` $ find . -name "*.bak" -type f -print | xargs /bin/rm -f`

find all files with `.bak` extension in or below the current directory and delete them from the filesystem.
 

