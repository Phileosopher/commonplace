
# Specific Unix trivia and shortcuts

To edit any plaintext file from the command line:

- nano (the text file), you may need to use sudo

## Superuser

Many of the instructions online will have "$" or "#" at the beginning of the command.

- Don't enter it, since "#" means simply running the command and "$" means running it as "sudo"

You will frequently need to enter sudo at the beginning of any system process.

- This is "superuser do", and requires you enter your password to authenticate [the highest permission possible on the computer](computers-cysec-authentication.md).

## Keyboard tweaks

To add a compose key:

Open /etc/default/keyboard

- "XKBOPTIONS=compose:ralt" (or whatever compose keyboard mapping you want)
- Your compose key can be the following:
  - ralt (a good general option)
  - lwin/rwin (probably not a good idea since it opens the bottom left programs bar)
  - menu (probably not on most keyboards)
  - lctrl/rctrl (might be a good option)
  - caps (a bad idea unless you never use caps lock ever)
  - paus (a good option)
  - prsc (not recommended if you ever use screenshots)
  - sclk (not recommended if you ever use it)
