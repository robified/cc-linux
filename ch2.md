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
        - 
    - $ grep root /etc/*
        - 
- less
- pwd
- diff
- file
- file and locate
- head and tail
- sort

## Changing Your Password and Shell

## Dot Files

## Environment and Shell Variables

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
