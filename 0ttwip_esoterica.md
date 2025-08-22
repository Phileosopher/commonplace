This is a pile of quick-reference tech concepts. They're effectively trivia, but critical within the industry.

## Slow computer fixes

NOTE: Avoid the following:

- Registry cleaners
  - A registry is plaintext and takes up *very* little space.
  - Modifying the registry can permanently damage the [OS](computers-os.md), even with Windows Update.
- Most third-party system cleaners
  - Most of them do what Windows' Disk Cleanup already does, alongside the above-mentioned registry cleaning.
  - They're usually adware or tracking user data you probably don't want.

1. Run an [antivirus scan](computers-cysec-malware.md), just to confirm.
2. Check for any running tasks, and sort by [CPU](computers-cpu.md), [memory](computers-memory.md), and [network](networks-computer.md) use to find what's using them the most.
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
11. Swap out Chrome web browser for Brave or Firefox (which consume less memory/CPU).
12. After all this doesn't work, upgrade it:
    - A new SSD hard drive, if it's an HDD (the easiest upgrade, assuming it's not a laptop).
    - A better CPU (it *must* match the chipset of the current processor).
13. If you need a new motherboard for better parts, get a new computer for your purposes.
    - Use the old computer for a dedicated [side-project](computers-embedded.md) that won't see heavy use.

## Network debugging

1. Ping a known local IP address: ping 192.168.100.1
2. Test telnet access to that local IP (failure is secure): telnet 192.168.100.1
   - On Windows, enable "Telnet Client" under Programs and Features before using.
3. Nmap the LAN side of the modem: nmap -v -A -p 1-65535 192.168.100.1
4. Check DNS settings, manually override with a known DNS provider.
5. Repeat for a known internet IP (e.g., 1.1.1.1).

## Browser optimizations - Chrome

1. Go to chrome://settings, navigate to Advanced > System
2. Disable the following, then click the relaunch button:
   - Continue running background apps when Google Chrome is closed.
   - Use hardware acceleration when available.
3. Go to chrome://flags and relaunch every time you apply a setting:
   - Disable WebRTC remote-bound event logging
   - Disable WinRT Geolocation Implementation
   - Disable hardware-accelerated video decode
   - Disable hardware-accelerated video encode
   - Enable Override Software Rendering List
   - Enable GPU Rasterization
   - Enable Parallel Downloading
4. Close the browser, then (on Windows) navigate to C:/Program Files/Google/Application/[the first folder with only numbers]
5. Delete the following:
   - Installer (folder)
   - elevation_service.exe
   - Locales/[every .pak file besides your language]
6. (On Windows) navigate to C:/Program Files (x86)/Google and delete the Updates folder.
7. Empty the recycle bin.
