
# How to fix things that have computers in them

All [the rules of generally fixing things](https://adequate.life/fix/) apply, but there are technology-specific considerations to also consider.

Before you *ever* panic or give up, make a simple web search for what you want, since others have probably found the answer.

- To be more thorough, use search handles to narrow what you're looking for.
- Look for similar model numbers (hardware) or alternate-language implementations (software) of the same thing.
- What works for others may not work for you, but *how* you can use what worked is more important than what has been done.

Most of the industry is either "break-fix" (paid per fix) or "managed services" (paid to keep everything running).

## Preventative maintenance

Avoid the following:

- Registry cleaners
  - A registry is plaintext and takes up *very* little space.
  - Modifying the registry can permanently damage the [OS](computers-os.md), even with Windows Update.
- Most third-party system cleaners
  - Most of them do what Windows' Disk Cleanup already does, alongside the above-mentioned registry cleaning.
  - They're usually adware or tracking user data you probably don't want.

On a regular basis, do the following to a slow computer:

1. Run an [antivirus scan](computers-cysec-malware.md), just to confirm.
2. Check for any running tasks, and sort by [CPU](computers-cpu.md), [memory](computers-memory.md), and [network](networks-cs.md) use to find what's using them the most.
3. Turn the power settings to the max (on Windows, "Always On" or "High Performance" setting for plugged-in).
4. Check the interior for dust and blow it out with an air compressor.
   - Canned air has chemicals that can corrode motherboard circuits.
   - If possible, apply more thermal paste between the CPU and its fan.
5. Check that there's enough hard drive space (especially in C: drive in Windows).
   - Empty the Recycle Bin.
   - (in Windows) Run Disk Cleanup with Administrative permissions.
   - Use a file size checker for large, useless files.
   - Uninstall programs you haven't used in more than a year.
   - Run a general cleaner (e.g., BleachBit), but avoid any Windows "registry cleaner" features.
6. (in Windows) Run Disk Defragmenter and schedule it to run daily or weekly.
7. (in Windows) Disable Startup items (in msconfig or Task Manager) and tasks in Task Scheduler.
8. (in Windows' services.msc) Web search and disable unnecessary Windows services.
9. (in Windows command prompt) Scan the system:
   1. sfc /scannow (scans system files, re-run until no issues)
   2. chkdsk /r (checks the entire disk)
10. (in Windows' PowerShell terminal) Check the system image:
    - DISM /Online /Cleanup-Image /RestoreHealth
11. Swap out your [web browser](computers-browser.md) for a lower-profile one that consumes less memory/CPU.
12. After all this doesn't work, upgrade it:
    - A new SSD hard drive, if it's an HDD (the easiest upgrade, assuming it's not a laptop).
    - A better CPU (it *must* match the chipset of the current processor).
13. If you need a new motherboard for better parts, get a new computer for your purposes.
    - Use the old computer for a dedicated [side-project](computers-embedded.md) that won't see heavy use.

## Networked

Typically, it helps to triple-check that *every* [networked](networks-cs.md) component is offline, and preferably unplugged.

- For a long while afterward, a powered-off device can still register as connected (especially network switches).

## Network chains

As counter-intuitive as it sounds, move things around frequently to see if anything changes.

- Change out port locations, plug things into various locations, swap out hardware.
- Often, the [programmer](computers-software.md) will make code that worked for the situation (e.g., check ports 1 and 2 on a two-port switch), and it wasn't updated for a later hardware release (e.g., check all available ports).
- Sometimes, the code may need something to change to escape an endlessly looping subroutine.

Your most difficult challenge will first be in making the problem reproducible, then in localizing it.

- If the issue keeps arising up in the same area, split that area in half as many times as possible.
- [Brainstorm](mind-creativity-how.md) different perspectives on how it could arise or how you could fix it (e.g., mind maps).

### Perception

The ability to know *exactly* which details are significant can only come from experience.

- A network technician with 2 years of hands-on experience with that particular software or hardware is worth one with 6 or 10 years on anything else.

### Repetition

One of the fortunate aspects about most computer troubleshooting (with the important exception of anything involving [AI](computers-ai.md)) is that the system is *highly* fine-tuned, meaning that it's not likely that more than one thing broke at once.

## Complications

Since computers are inherently complicated, do *not* do anything to make things more complicated. This is not easy for the types of people who [specialize in](jobs-specialization.md) computers.

First, ask what the simplest likely thing would be that could have failed. It's usually not very interesting and easy to overlook.

- Check that everything has been [rebooted](computers-boot.md).
- Log out and login again with everything.
- For hardware, closely examine the model numbers for any discrepancies or known defects.
- For software, check the [version numbers](computers-software-versionctrl.md) to be sure everything is up-to-date.
  - For [enterprise](computers-distsys.md) software, examine if there *were* any updates corresponding to the outage.
- Make sure the configurations are set correctly.
- Check the [network](networks-cs.md) to be sure it's working correctly.

To avoid reference issues, don't let a CPU run updates or install *anything* while it's multitasking something else:

1. The code on the computer is instructed to write information to Point A.
2. While it's been designated, but before it was written, a tech-savvy user made Point A become Point B because they were trying to be [efficient](https://trendless.tech/fast/) with something else.
3. Computer writes to Point A.
4. Computer later glitches out because everything that *was* relative to Point A is now only accurate relative to Point B.
5. Worst-case scenario is that the tech-savvy user must do something far more dramatic, like reinstall the OS or extract data from a hard drive.

If you must roll back updates, turn off the auto-update features first, and make sure to roll back *all* the connected dependencies. Rolling back is like heart surgery, so only do it if you have no choice.

Try to avoid updating multiple systems at once, and reboot each time if possible.

## Repairing

The best way to repair depends heavily on the domain.

It's always important to have done *some* preventative work before you needed to repair it:

- Have the same or similar extra hardware available for replacement.
- Keep offline media of the current software versions available, or at least have another means to connect to another installation of that software (e.g., mobile hotspot cellphone subscription).
- Keep ready access to the precise technical documentation that indicates how to reset or reinstall something.

The easiest preventative measure is to always keep multiple backups.

- If you're pressed for memory space, space out the backup cycle as you go farther back (e.g., keep a copy for each week for the past month, a copy from every month for the past year, etc.).
- If you must manually run the backup, you should be spending more time saving backups than loading them.

For the most part, software fixes simply require having the software pre-downloaded for quick transfer, but it's worth keeping some hardware available, just in case:

- USB drive loaded with a plethora of diagnostic apps, preferably *two* of them (one for [Windows](https://trendless.tech/windows/), and the other with a lightweight [Linux distro](https://trendless.tech/unix/) on the drive)
- A wired USB keyboard, which is less trouble to set up
- A Bluetooth keyboard for mobile devices
- Non-magnetized screwdriver set with Torx, flat, and cross-point drivers
- Antistatic mat or antistatic wrist strap
- Head-mounted magnifier or magnifying glass
- POST card for [boot](computers-boot.md) issues
- Loopback plug for [network](networks-cs.md) diagnosis
- Multimeter for testing circuitry
- Power supply tester
- Soldering iron with solder wire

*Any* laziness whatsoever in fixing bugs or [documenting it](language-writing-documentation-cs.md), no matter how minor, will magnify the problem if it resurfaces:

- If it re-emerges in 3 months, you'll likely have forgotten about it in the interim.
- When someone else encounters it, they'll go through approximately the same journey of frustration you did.
- That bug may be unimportant right now, but will become *much* worse if the system ever scales.

At the same time, enough false-positives will make the system insensitive to actual issues, so the logs and staff should aim for *only* communicating legitimate issues.

### Hardware

If the problem is urgent, find a sufficient replacement that does the job.

- It *can* be an upgrade if the situation permits (e.g., [keyboard](computers-keyboard.md), [mouse](computers-mouse.md)), but make sure it's compatible before getting it.
- Don't worry too much about overkill (e.g., a newer model with more features) or reliability, since your fix is buying time to resolve it when it's *not* urgent.

### Software

Try to reinstall or reload the code.

- If you have access *to* the code, you may be able to change a reference, but don't try rebuilding the code until *after* it's back online and no longer urgent.

If anything depends on it, don't upgrade it.

- Unless a dependency elsewhere had upgraded and deprecated support for the current version, try to reinstall what existed.
- Updates are generally not good to roll out, but software updates will frequently overwrite hundreds, maybe *thousands* of references, and you may need to [debug](computers-software-redesign.md) new updates and features *on top of* addressing your current problem.

### Data

Unfortunately, recovering data can be *tremendously* difficult.

- Look for proprietary software to recover the data, which may require [decrypting](encryption.md) the device's memory.
  - If the data is particularly secure or proprietary, you may need another piece of hardware that's precisely the same type (e.g., a specific brand of disk drive).
- Sometimes, you'll simply have to hack the solution by ripping out the data yourself, then find the [protocol](standards-computers.md) that translates the raw data into a usable format.

### Distributed Systems

In the chain of various systems, all you need is one failure to make the entire thing fall apart:

- If there are any integers, avoid floats. In the case of currency, that's the only way for money to not randomly disappear or appear.
- Make sure the UUIDs are all interpreted as case-insensitive or with a shared convention.
- Watch for time-based discrepancies, such as asynchronous data flow or updating information that retroactively makes other information obsolete. This can be particularly nasty if a time server (e.g., NTP) shifts a few seconds or an hour for some reason. The solution is to have a centralized time, but also distinguish which system time you're also using.

Pay attention to the slowest part of the system. Any new subsystem that resolves slowdown will likely become the *new* "slowest part of the system".

### AI

If a [training model](ai-ml.md) has been poisoned, you have several options:

1. Start all over and retrain. This is technically the most obvious, but also the most time-consuming and potentially the most expensive.
2. Train the entire model on fixed, predictable, safe data, which dilutes the poison. It's not foolproof, but it's technically the lowest-effort, and further exposure to good data will make the model fix itself over time.
3. Delete and retrain the specific faulty nodes. If you can pull it off, this is ideal.

## Postmortem

After [fixing anything](https://trendless.tech/fix/), *always* [document](language-writing-documentation.md) the new rules and what happened. Otherwise, you've made life worse for someone else (including Future You).

The industry tends to not respect the people who repair the computers, so keep an eye on who you help, how much, and how much they pay you for the service relative to your investment.

## Case Studies

Weird failures:

- [Print this file, your printer will jam](https://nedbatchelder.com/blog/200811/print_this_file_your_printer_will_jam.html)
- [We can't send email more than 500 miles](https://web.mit.edu/jemorris/humor/500-miles)
- [Car allergic to vanilla ice cream](https://www.cs.cmu.edu/~wkw/humour/carproblems.txt)

Impressive fixes:

- [The long road to recover Frogger 2 from tape drives](https://github.com/Kneesnap/onstream-data-recovery/blob/main/info/INTRO.MD)
