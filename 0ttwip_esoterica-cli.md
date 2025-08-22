
These are general command-line interface shortcuts, useful for most things. ⊞ for Windows, □ for Linux/Mac (⌘ if Mac is different).

## Parameters/commands

Most of the commands have special elements that modify the command's scope:

- e.g., "ls -S -s" will list all the files in a directory, but also sort them by size and print their size as well.
  - ⊞: [COMMAND] /w /s /p
  - □: [COMMAND] -w -s -p
- e.g., "dir /p" will print all the files in a directory, one page at a time.

To find all the parameters/options, consult the [documentation](language-writing-documentation-cs.md):

- help [command]
- -h
- --help
- man

## General commands

Folder shortcuts:

- . is the current folder
- .. is the parent folder

Output something to a text file:

- [any command] > [filename]

Append something to the end of a text file:

- [any command] >> [filename]

Send a file's text in as a command:

- < [filename]

Make the output of something become the input of something else:

- [program 1] | [program 2]

Display the current directory:

- □: pwd
- ⊞: echo %cd%

List the files in the directory:

- □: ls
- ⊞: dir

Count all files by type in a directory and recursively to subdirectories (Linux):

```
find . -type f | sed -n 's/..*\.//p' | sort | uniq -c
```

Change the directory:

- cd [path]

Delete a file/folder:

- □: rm [file or folder]
- ⊞: del [file or folder]

Delete *everything* in a file/folder:

- □: rm -rf [file path]/* (doesn't get rid of hidden/system files)
- ⊞: del *.*

Delete all empty subfolders:

- ⊞: robocopy [parent directory you want to purge] [parent directory you want to purge] /s /move

Move a file/folder (which is the equivalent of renaming it):

- □: mv [file or folder]
- ⊞: move [file or folder]

## Networking commands

Display general network config:

- □: ip a
- ⌘: ifconfig
- ⊞: ipconfig

Show network statistics:

- netstat

Measure how long network connections take:

- ping [IP address]

Show where packets are dropping:

- tracert [IP address]

Display IP routing tables:

- show ip route

Check which IP protocols are enabled:

- show ip protocols
