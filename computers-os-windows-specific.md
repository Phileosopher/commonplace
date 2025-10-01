
# Specific Windows trivia and information

## Windows file paths

Start menu shortcuts

- C:\ProgramData\Microsoft\Windows\Start Menu\Programs

Windows Store apps (*not* the old-style Windows Desktop apps)

- %windir%\explorer.exe shell:::{4234d49b-0245-4df3-b780-3893943456e1}

Temporary folder

- %temp%

Print folder contents to file

- dir /a /s /b > filelist.txt

Access *all* controls

1. Create a new folder, then rename to:
2. [anything you want].{ED7BA470-8E54-465E-825C-99712043E01C}

## Windows registry keys

NOTE: create the registry values and keys if they're not made, or simply edit them.

Delete what you want, but save a backup just in case, since incorrect registry edits *will* brick the system, and Windows Update usually won't auto-fix them.

Optimization

- Enable L2 and L3 Cache
  - HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/Control/Session Manager/Memory Management/SecondLevelDataCache [DWORD] = (in KB, use [CPU-Z](https://www.cpuid.com/softwares/cpu-z.html), bottom right)
  - HKEY_LOCAL_MACHINE/SYSTEM/CurrentControlSet/Control/Session Manager/Memory Management/ThirdLevelDataCache [DWORD] = (in KB, use [CPU-Z](https://www.cpuid.com/softwares/cpu-z.html), bottom right)
- Disable lock screen
  - HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Personalization\NoLockScreen [DWORD] = 1
- Prevent auto-reboot from updates
  - HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\WindowsUpdate\AU\NoAutoRebootWithLoggedOnUsers [DWORD] = 1
- Delete ALL temp files during Disk Cleanup
  - HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\VolumeCaches\Temporary Files\LastAccess [DWORD] = 0 (number of days)
- Display a notice during boot with a click-through
  - HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Policies\System\legalnoticecaption = [enter your text heading]
  - HKEY_LOCAL_MACHINE\Software\Microsoft\Windows\CurrentVersion\Policies\System\legalnoticetext = [enter your text body]
  - NOTE: For carriage returns, edit binary data and add "0D 00" where you want it.
- Disable Cortana and Windows Search
  - HKEY_LOCAL_MACHINE\SOFTWARE\Policies\Microsoft\Windows\Windows Search\AllowCortana [DWORD] = 0
  - Computer\HKEY_CURRENT_USER\SOFTWARE\Policies\Microsoft\Windows\Explorer\DisableSearchBoxSuggestions [DWORD] = 1

Context Menu

- Add/remove context menu items (old shell)
  - HKEY_CLASSES_ROOT\*\shell
    1. Disable with HKEY_CLASSES_ROOT\*\shell[Menu Item]\LegacyDisable [String]
    2. Require Shift key to be pressed with HKEY_CLASSES_ROOT*\shell[Menu Item]\Extended [String]
- Add/remove context menu items (extended shell)
  - HKEY_CLASSES_ROOT\*\shellex\ContextMenuHandlers
  - HKEY_CLASSES_ROOT\AllFileSystemObjects\ShellEx
  - NOTE: Rename the (Default) key to something else (e.g., add a few dashes), or simply delete.
- Add "New [markdown](markdown.md) file" to context menu
  - HKEY_CLASSES_ROOT\.md\(Default) = markdown
  - HKEY_CLASSES_ROOT\.md\ShellNew\NullFile
  - HKEY_CLASSES_ROOT\markdown\(Default) = Markdown Document
- Add/remove file extension-specific context menu items
  - HKEY_CLASSES_ROOT[the file extension you want]\(Default) - remember the Default's value
  - HKEY_CLASSES_ROOT[Default's value]\shell
- Add/remove folder-specific context menu items
  - HKEY_CLASSES_ROOT\Directory\shell
  - HKEY_CLASSES_ROOT\Directory\shellex\ContextMenuHandlers
- Remove "Open with..." programs
  - HKEY_CURRENT_USER\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\FileExts[File Extension]\OpenWithList
  - NOTE: Delete whatever keys you want.
- Add encrypt/decrypt
  - HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced\EncryptionContextMenu [DWORD] = 1
- "Open with" in context menu
  - New Key: HKEY_CLASSES_ROOT\Directory\Background\shell[Program Name]
  - NOTE: to allow an ALT-click shortcut set the (Default) value in that key to &[name] (e.g., &Notepad).
  - HKEY_CLASSES_ROOT\Directory\Background\shell[Program Name]\command\(Default) = [the program's path]
- Open with command prompt
  - Rename the following:
    - HKEY_CLASSES_ROOT\Drive\shell\cmd\Extended -> HKEY_CLASSES_ROOT\Drive\shell\cmd\Extended-Orig
    - HKEY_CLASSES_ROOT\Directory\shell\cmd\Extended -> HKEY_CLASSES_ROOT\Directory\shell\cmd\Extended-Orig
- Open with Notepad
  - HKEY_CLASSES_ROOT\*\shell\Open with Notepad\command\(Default) = notepad.exe %1
- Run as administrator
  - HKEY_CLASSES_ROOT[File Type]\shell\open\command
  - Export the "open" key, edit the file with text editor. Replace "open" with "runas".
  - Run the exported, edited file.

Diagnostics

- Edit Windows Defender exclusions
  - HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows Defender\Exclusions[Paths/Processes/IpAddresses/Extensions]
- Show more details when crashing (Win10)
  - HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\CrashControl\DisplayParameters [DWORD] = 1
- BIG diagnostics
  - Re-enable Task Manager (e.g., a virus)
    - HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Policies\System\DisableTaskManager [DWORD] = 0
  - New install stuck in an error loop while booting - sysprep
    - HKEY_LOCAL_MACHINE\SYSTEM\Setup\Status\ChildCompletion\setup.exe = 3 (should be 1 when you get there)
  - New install stuck in an error loop while booting - Audit Mode
    - HKEY_LOCAL_MACHINE\SYSTEM\Setup\Status\ AuditBoot [DWORD] = 0
    - HKEY_LOCAL_MACHINE\SYSTEM\Setup\Status\ChildCompletion\audit.exe [DWORD] = 0
    - HKEY_LOCAL_MACHINE\SYSTEM\Setup\Status\SysprepStatus\CleanupState [DWORD] = 2
    - HKEY_LOCAL_MACHINE\SYSTEM\Setup\Status\SysprepStatus\GeneralizationState [DWORD] = 7
    - HKEY_LOCAL_MACHINE\SYSTEM\Setup\Status\UnattendPasses\auditSystem [DWORD] = 0

The code for making a .reg file (auto-executing registry script) is relatively easy to make

1. Make a text file, but change the extension to .reg.
2. Use the following syntax:

```registry
Windows Registry Editor Version 5.00

[PUT THE PATH YOU WANT HERE]
@="the value you want for (Default)"

[PUT THE NEXT PATH YOU WANT HERE]
"Value"="the value for the new key, which may be empty"
```

## Windows reserved storage

1. Access command prompt.
2. Get status:
   - DISM.exe /Online /Get-ReservedStorageState
3. Enable/disable:
   - DISM.exe /Online /Set-ReservedStorageState /State:Enabled
   - DISM.exe /Online /Set-ReservedStorageState /State:Disabled

Extremely useful to toggle if Windows complains about not having enough disk space.

Disable as much as possible, since Windows devs don't always use it and it takes up ~8GB of HD space.

## Windows Run commands

- Windows 10's drive:
  -

- Home folder of current user:
  - .
- Users folder:
  - ..
- Control panel:
  - control
- System config:
  - msconfig
- Programs/features:
  - appwiz.cpl
- Disk cleanup:
  - cleanmgr
- Resource monitor:
  - resmon
- Common apps:
  - calc
  - notepad
  - mspaint
- Mouse settings:
  - main.cpl
- Remote desktop:
  - mstsc
- System info:
  - msinfo32
