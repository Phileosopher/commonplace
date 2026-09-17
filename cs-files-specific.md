
# Specific file information and configs

## Common file extensions

Text-based

- txt: plaintext
- md: [markdown](markdown.md)
- doc/docx: proprietary MS Word document
- dot/dotx: proprietary MS Word template
- odt: open document text

Advanced office uses

- xls/xlsx: proprietary MS Excel spreadsheet
- xlt/xltx: proprietary MS Excel template
- ods: open document spreadsheet
- ppt/pptx: proprietary MS PowerPoint slideshow
- odp: open document slideshow

Applications

- exe: Windows program
- msi: Windows installer
- dmg/app: Mac program
- tar/tar.gz/tgz: general Linux package
- deb: debian package
- rpm: rpm package
- AppImage: portable application image

Specific languages

- js: JavaScript
- php: PHP
- py: Python

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
