# Basic Commands and Directory Hierarchy

## The Bourne Shell: /bin/sh
- Shell
    - Shell scripts
- Bash aka "Bourne-again" shell
- Shell prompt
    - $
- To change shell
    - $ chsh

## Using the Shell
- Shell Window aka Terminal
    - $ echo Hello World
- cat aka Concatenation
    - outputs contents
        - $ cat /etc/passwd
        - $ cat \<file1> \<file2>
- Standard Input (Stdin) & Standard Output (Stdout)
    - Processes read data: input stream
        - file, device, terminal, output stream
        - $ cat
            - Ctrl-D to stop current Std Input
            - Ctrl-C to terminal regardless Std I/O
    - Write data: output stream
    - Bonus: Standard Error

## Basic Commands
- ls
    - list contents in a directory
    - $ ls -l
        - detailed long listing
            - owner
            - group
            - file size
            - modification date/time
    - $ ls -F
        - display file type
- cp
    - copy files
    - $ cp \<file1> \<file2>
    - copy files to a directory
        - $ cp \<file1> ... \<fileN> \<dir>
- touch
    - create a file
    - $ touch \<file>
    - Touching the file again will modify the data/time to current
        - to check last date/time
            - $ ls -l \<file> 
- rm
    - remove a file
    - $ rm \<file>
- echo
    - prints argument to stdout
    - $ echo Herro!

## Navigating Directories
- / root directory
    - absolute path
- . refers to current directory
    - relative path
- $ cd \<nameOfDirectory>
    - current working directory
    - $ cd
        - home directory
- $ mkdir \<nameOfDirectory>
    - to create a new directory
- $ rmdir \<nameOfDirectory>
    - to remove a directory
    - $ rm -rf \<nameOfDirectory>
        - to remove everything inside the directory and the directory itself
        - r stands for recursive delete
        - f stands for force
        - BE CAREFUL!
- Shell Globbing (Wildcards)
    - $ echo *
        - To print a list of files in a directory    
    - $ at*
        - any files that starts with at
    - $ *at
        - any files that ends with at
    - $ *at*
        - any files that has at
    - $ ?
        - to match one specific character
    - $ ''
        - enclosing with a single quote to cancel glob from expanding

## Intermediate Commands
- grep
    - $ grep root /etc/passwd
        - to print lines from a specific file that contain the word 'root'
    - $ grep root /etc/*
        - to print lines from multiple files that contain the word 'root'
    - -i
        - case-insensitive matches
    - -v
        - inverts the search
        - prints lines that DON'T match
    - egrep aka grep -E
    - grep can understand Regular Expressions
        .* matches any # of characters
        . matches one character
- less
    - used when a file is too long
    - spacebar to advance
    - b to go back
    - q to exit
    - to send output of a grep command to less
        - $ grep ie /usr/share/dict/words | less
- pwd
    - to output the name of the current directory you're in
    - use $ pwd -P to see TRUE path
- diff
    - to see the difference between two files
    - $ diff <file #1> <file #2>
- file
    - to see what type of file you're working with
    - file <file #1>
- file and locate
    - to find and locate a file 
    - $ find <name of directory> -name <name of file> -print
- head and tail
    - to view portions of a file or data streams
    - head shows the first 10 lines
         - $ head <name of file>
    - tail show the last 10 lines
        - $ tail <name of file>
- sort
    - to sort the line of a file by alphanumeric order
        - $ sort <name of file> -n 
    - to sort in reverse order
        - $ sort <name of file> -r

## Changing Your Password and Shell
- to change your password
    - $ passwd
- to change your shell
    - $ chsh

## Dot Files
- to view Dot File, which are configuration files/directories
    - $ ls -A

## Environment and Shell Variables
- to store a variable in the shell
    - $ STUFF=yas
- to access the shell variable
    - $ $STUFF
- to convert a shell variable to an envirnment variable
    - $ STUFF=yas
    - $ export STUFF

## The Command Path

## Special Characters

## Command-Line Editing

## Text Editors

## Gettting Online Help

## Shell Input and Output

## Understanding Error Messages

## Listings and Manipulating Processes

## File Modes and Permissions

## Archiving and Compressing Files

## Linux Directory Hierarchy Essentials

## Running Commands as the Superuser
