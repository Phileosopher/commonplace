
# CLI shortcuts

These are general command-line interface shortcuts, useful for most things. ⊞ for Windows, □ for Linux/Mac (⌘ if Mac is different).

## Parameters/commands

Most of the commands have special elements that modify the command's scope:

- (COMMAND) (OPTION) (ARGUMENT)
  - First the necessary command, then the optional handles, then the optional argument.
  - Many times, the argument has a implicit default (e.g., "ls" refers to the current folder)
- e.g., "ls -S -s" will list all the files in a directory, but also sort them by size and print their size as well.
  - ⊞: (COMMAND) /w /s /p
  - □: (COMMAND) -w -s -p
- e.g., "dir /p" will print all the files in a directory, one page at a time.

The options are often syntactic sugar, and there is a full-text version of it as well (e.g., "-a" vs. "--all").

To find all the parameters/options, consult the [documentation](language-writing-documentation-cs.md):

- man (command)
- info (command)
- help (command)
- fasthelp
- (command) -h
- (command) --help
- This is particularly helpful when you have limited internet access

## Interface conveniences

View system information:

- □: hostnamectl

Clear the screen:

- □: clear
- ⊞: cls

View all available commands:

- □: compgen -c

View all available aliases:

- □: "compgen -a" or "help alias" or "alias -p"

Indicate a command type and where it's located:

- □: type (command)
- □: which (command)

Pattern-matching:

- □
  - Match any range of characters: *
  - Match 1 of any character: ?
  - Match a class of characters: [] (e.g., [1-4], [3..25], [1b5])
    - character classes:
      - [:print:] printable characters (alnum + punct + space)
        - [:alnum:] letters and numbers
          - [:alpha:] a-z, A-Z
            - [:lower:] a-z
            - [:upper:] A-Z
          - [:digit:] (0-9)
          - [:xdigit:] hexadecimal (0-9, a-f, A-F)
        - [:punct:] punctuation characters (e.g., !, &, ")
        - [:space:] whitespace characters (e.g. tabs, spaces, newlines)
          - [:blank:] spaces and tabs
      - [:cntrl:] control characters (e.g., backspace, bell, NAK, escape)
      - [:graph:] all characters except ctrl and space

End the terminal session:

- quit or exit

Reboot the computer to BIOS:

- □: sudo systemctl reboot --firmware-setup
- ⊞: shutdown /r /fw /t 0

## Computer status

Indicate the computer's local date and time:

- date

View OS info:

- □: uname -r

View CPU info:  

- □: lscpu

View memory info:

- □: lsblk
- □: free
- □: mem (total RAM)
- □: swap

View disk usage of a folder:

- □: du

View active processes:  

- □: top (real-time)
- □: ps -ef --forest (snapshot)

View running services:

- □: service --status-all
  - A + means it's running, a - means it's stopped, and ? means it's not currently known.
  - service (servicename) status gives mroe information.

View system journal:

- □: journalctl

View active logs:  

- □: dmesg
  - This is an overwhelming amount of information, so it's best to scope it with grep

Count text in a file:  

- □: wc (-l for lines, -w for words, -c for characters)

## Navigation

Display a specified output:

- echo (something)

Display the current directory:

- □: pwd or "cd -"
- ⊞: echo %cd%

Change the directory:

- cd (path)

Folder shortcuts:

- . is the current folder
- .. is the parent folder

List the files in the directory:

- □: ls
- ⊞: dir
- The parameters can add *many* features to give more information.

Search for something in a directory:

- □: locate (file/directory name)

Indicate what a file is:

- □: file (file)

Count all files by type in a directory and recursively to subdirectories (Linux):

```bash
find . -type f | sed -n 's/..*\.//p' | sort | uniq -c
```

## File creation/destruction

Make a directory:

- mkdir (directory)
  - ⊞: md (directory) is a shortcut

Make a file or update its modified timestamp:

- □: touch (filename)

Delete a file/directory:

- □: rm (file) or rmdir (empty directory)
  - rmdir -ri will remove things inside it and ask for prompts (or rmdir-r without a prompt)
- ⊞: del (something) or erase (something)

Delete *everything* in a file/folder:

- □: rm -rf (file path)/* (doesn't get rid of hidden/system files)
- ⊞: deltree or "del *.*"

Copy everything:

- robocopy (directory 1) (directory 2) /s /move

Move a file/directory (which is the equivalent of renaming it):

- □: mv (file or folder)
- ⊞: move (file or folder)

Compare two files line-by-line:

- □: diff (file)
- ⊞: fc (file)

Quick-edit a text file:

- □: nano (file)
- ⊞: edit (file)

Set links:

- □: ln (existingtarget) (linkname)
  - Hard links are treated effectively like files for the sake of moving and renaming.
  - The option "-s" makes a symlink.

## User accounts

View current user ID and groups:

- □: id
- □: groups

View members of a group:

- □: groupmems (group)

View recent user logins:

- □: last
- □: lastb (for bad logins)

Escalate privileges:

- □: sudo (command) for a single command
- □: "su -" for root (use sparingly)

Add user/group:

- □: useradd (username)
- □: groupadd (group)
- □: passwd (username)

Remove user:

- □: userdel (username)
- □: groupdel (group)

Change ownership:

- □: chown (username):(groupname) (file)
- □: chgrp (group) (file)

## Networking

Display general network config:

- □: ip a
- ⌘: ifconfig
- ⊞: ipconfig

Manage wireless networks:

- □: iwlist
- □: iwconfig

Show network statistics:

- netstat

Measure how long network connections take:

- ping (IP address)
  - without specifying a limit, persists until you kill the terminal or press CTRL+C

Show where packets are dropping:

- tracert (IP address)

Display IP routing tables:

- show ip route

Check which IP protocols are enabled:

- show ip protocols

Securely copy (SSH+copy):

- □: scp (file1) (destinationdirectory)
  - It's very versatile and can route with hosts and specify ports.
  - [example syntax](https://hypexr.org/linux_scp_help.html)

## Inter-OS

Enable Windows Subsystem for Linux (WSL) and virtualization:

```powershell
dism /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism /online /enable-feature /featurename:VirtualMachinePlatform /all
```

## Scripting

Keep a process running even after reboot:

- □: nohup (command)
