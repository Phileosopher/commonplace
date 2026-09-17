
# Bash-specific details

Bash is the interpreter, so the terminal emulator is just for the GUI experience, since they all process the same.

## Oddities and quirks

Case-sensitivity, like everything else in [Unix-likes](cs-os-unix.md), is a big deal, as opposed to [Windows](cs-os-windows.md) conventions where case doesn't matter. While this allows for more organization (e.g., a variable can be all-caps for visual demarcation) it also opens up the risk of more developer error.

Quotes in bash are interpreted different. Using '' makes *everything* into a non-expanded string, but "" makes strings with shell expansion on some elements.

- To protect a string with "", add \ before the character (somewhat similar to [regular expressions](cs-langs-specific-regex.md)).

## Built-in commands

/bin

- bash
- cat
- chmod
- cp
- date
- echo
- grep
- gunzip
- gzip
- hostname
- kill
- less
- ln
- mkdir
- more
- mount
- mv
- nano
- open
- ping
- ps
- pwd
- rm
- sh
- su
- tar
- touch
- umount
- uname

/etc

- crontab
- cups
- fonts
- fstab
- host.conf
- hostname
- hosts
- hosts.allow
- hosts.deny
- init
- init.d
- issue
- machine-id
- mtab
- mtools.conf
- nanorc
- networks
- passwd
- profile
- protocols
- resolv.conf
- rpc
- securetty
- services
- shells
- timezone

/sbin

- fdisk
- fsck
- getty
- halt
- ifconfig
- init
- mkfs
- mkswap
- reboot
- route

## Input/output

Output something to a text file:

- (any command) > (filename)

Output something and its errors to a text file:

- (any command) &> (filename)

Append something to the end of a text file:

- (any command) >> (filename)

Append something and its errors to the end of a text file:

- (any command) &>> (filename)

Send a file's text in as a command:

- < (filename)
  - This is implicit most of the time for commands, and usually only used with commands that don't accept file arguments.

Make the output of something become the input of something else:

- (program1) | (program2)
  - Can be continuous: (program1) | (program2) | (program3)

Print errors to a file:

- (command with errors) 2> (file)
  - This refers to Channel 2 (stderr)

## Variables

Bash variables must always start with a letter and not use embedded spaces or punctuation marks.

Unless there's an explicit reason to *not* quote a variable, *always* quote a variable when calling it.

- This is because variables with spaces will be called as separate variables:
  - e.g., assume $VALUE is "test information".
    - rm $VALUE means "rm test" and "rm information".
    - rm "$VALUE" means "rm 'test information'".

Display all present environment variables:

- printenv

Make a local variable:

- variable=(text)

make a local variable global:

- export (variable)

Make and print a variable:

- export variable=(text)

Remove a variable:

- unset $(variable)

Temporarily change the case of a variable:

- Uppercase: ${variable^}
- CAPITALS: ${variable^^}
- lowercase first letter: ${variable,}
- lowercase: ${variable,,}
- Uppercase: ${variable^}
- swap case first letter: ${variable~}
- sWAP CASE: ${variable~~}

Permanently change the case of a variable:

- Uppercase: declare -u variable=value
- Lowercase: declare -l variable=value

Track exit codes with "$?":

- Zero means the last command was successful, and any other number indicates an error.
  - 1: Catchall for general errors
  - 2: Misuse of shell builtins (according to Bash documentation)
  - 126: Command invoked cannot execute
  - 127: "command not found"
  - 128: Invalid argument to exit
  - 128+n: Fatal error signal "n"
  - 255: Exit status out of range (exit only takes args numbered 0-255)
- When scripting, make sure to always have exit codes to leave a pass/fail conditional for future use (e.g., "exit 0" or "exit 1").

### Pass an argument into a script file

```bash
    variable=$1
    (output)
  ```

file.sh (variable$1)

## User management

Change and check passwords:

- passwd (user)

## Managing history

View command history:

- history
  - enter !(number) to run that numbered command again
  - enter !(string) to run the last command that began with that string

Search for text within history:

- CTRL+R

Disregard specific future commands:

- HISTIGNORE="(text1):(text2*):(t?xt3)"

## Search

Searching inside a bash terminal can uses [regular expressions](cs-langs-specific-regex.md) with grep.

- It's a good idea to almost *always* use the -E handle to enable advanced regular expressions characters.

### sed

On a more advanced level, sed (stream editing) can find and replace characters within a file.

Remove all blank and comment lines from a config file (useful for reading without more noise):

```sed
sed '/^\[/d' config.ini
```

### awk

On an even *more* advanced level, [Awk](cs-langs-specific-awk.md) has more idiosyncrasies.
