
# Specific file information and configs

## Locked files/databases

Windows: locked Office file

- look for and delete a file at the location titled ~$[filename]

Windows: locked file

- select Run, enter "mmc"
- File -> Add/Remove Snap-in
- Add Shared Folders to applicable computer (likely the local computer)
- Navigate to Open Folders, right click and select Close Open File

Linux: pacman database not synchronizing/locking

- Open a console and run the following:
- sudo rm /var/lib/pacman/db.lck
