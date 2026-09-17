
# Specific Samba performance enhancement configurations

## Configuration settings

```samba

[global]

# FORCE THE DISK SYSTEM TO ALLOCATE REAL STORAGE BLOCKS WHEN A FILE IS CREATED OR EXTENDED TO BE A GIVEN SIZE.
# ONLY GOOD WITH FILE SYSTEMS THAT SUPPORT UNWRITTEN EXTENTS LIKE XFS, EXT4, BTRFS, OCS2.
# IF THE FILE SYSTEM DOES NOT SUPPORT UNWRITTEN EXTENTS, SET "strict allocate = no".
# NOTE: MAY WASTE DRIVE SPACE EVEN ON SUPPORTED FILE SYSTEMS
# SEE: https://bugs.debian.org/cgi-bin/bugreport.cgi?bug=798532

   strict allocate = Yes

# COUNTERACT SPACE WASTE FROM "strict allocate" FEATURE
# SEE: https://lists.samba.org/archive/samba-technical/2014-July/101304.html

   allocation roundup size = 4096

# ALLOW READS OF 65535 BYTES IN ONE PACKET, WHICH TYPICALLY PROVIDES A MAJOR PERFORMANCE BENEFIT.

   read raw = Yes

# SERVER SIGNING SLOWS THINGS DOWN WHEN ENABLED, WAS DISABLED BY DEFAULT PRIOR TO SAMBA 4.

   server signing = No

# SUPPORT RAW WRITE SMBs WHEN TRANSFERRING DATA FROM CLIENTS.

   write raw = Yes

# WHEN "strict locking = no", THE SERVER PERFORMS FILE LOCK CHECKS ONLY WHEN THE CLIENT EXPLICITLY ASKS FOR THEM.
# WELL-BEHAVED CLIENTS ALWAYS ASK FOR LOCK CHECKS WHEN IT IS IMPORTANT. THUS, "strict locking = auto" OR "strict locking = no" IS ACCEPTABLE IN THE VAST MAJORITY OF CASES.

   strict locking = No

# TCP_NODELAY: SEND AS MANY PACKETS AS NECESSARY TO KEEP DELAY LOW
# IPTOS_LOWDELAY: [Linux IPv4 Tweak] MINIMIZE DELAYS FOR INTERACTIVE TRAFFIC
# SO_RCVBUF: ENLARGE SYSTEM SOCKET RECEIVE BUFFER
# SO_SNDBUF: ENLARGE SYSTEM SOCKET SEND BUFFER

   socket options = TCP_NODELAY IPTOS_LOWDELAY SO_RCVBUF=131072 SO_SNDBUF=131072

# ALTERNATE WITH MORE FEATURES:
# SO_KEEPALIVE: INITIATES A PERIODIC CHECK EVERY 4 HOURS TO VERIFY THE CLIENT EXISTS.
# DEADTIME: CLOSES IDLE CONNECTIONS.

   socket options = TCP_NODELAY IPTOS_LOWDELAY SO_RCVBUF=65536 SO_SNDBUF=65536 SO_KEEPALIVE
   deadtime = 15

# SMBWriteX CALLS GREATER THAN "min receivefile size" WILL BE PASSED DIRECTLY TO KERNEL recvfile/splice SYSTEM CALL.
# TO ENABLE POSIX LARGE WRITE SUPPORT (SMB/CIFS WRITES UP TO 16MB), THIS OPTION MUST BE NONZERO (MAX VALUE = 128k)
# THIS OPTION WILL HAVE NO EFFECT IF SET ON A SMB SIGNED CONNECTION.

   min receivefile size = 16384

# USE THE MORE EFFICIENT sendfile() SYSTEM CALL FOR EXCLUSIVELY OPLOCKED FILES.
# NOTE: ONLY FOR CLIENTS HIGHER THAN WINDOWS 98/ME

   use sendfile = Yes

# READ FROM FILE ASYNCHRONOUSLY WHEN SIZE OF REQUEST IS BIGGER THAN THIS VALUE.
# NOTE: SAMBA MUST BE BUILT WITH ASYNCHRONOUS I/O SUPPORT.

   aio read size = 16384

# WRITE TO FILE ASYNCHRONOUSLY WHEN SIZE OF REQUEST IS BIGGER THAN THIS VALUE.
# NOTE: SAMBA MUST BE BUILT WITH ASYNCHRONOUS I/O SUPPORT

   aio write size = 16384
```

## Things to watch for

hide files identifies files hidden by the Windows client.

- hide files will result in any file matching the pattern being passed to the client with the DOS hidden attribute set.
- It requires a pattern match per file when listing directories, and slows the server noticeably.

lpq cache time is used if the lpq (printer queue contents) command takes a long time to complete.

- Increase lpq cache time to a value higher than the actual time required for lpq to execute to keep Samba from starting a new query when one's already running.
- The default is 10 seconds, which is reasonable.

strict locking causes Samba to check for locks on every access, not just when asked to by the client.

- The option is primarily to avoid bugs, and can prevent poorly-optimized DOS and Windows applications from corrupting shared files.
- However, it is slow, so typically it's worth avoiding.

strict sync causes Samba to write each packet to disk and wait for the write to complete whenever the client sets the sync bit in a packet.

- Windows 98 Explorer sets the bit in all packets transmitted, so anyone with Windows 98 will think Samba servers are horribly slow with this on.

sync used to "sync always" and causes Samba to flush every write to disk.

- This is good if your server constantly crashes, but it has immense performance costs.
- SMB servers normally use oplocks and automatic reconnection to avoid adverse consequences of crashes, so setting this option is not normally necessary.

wide links turns off wide links to prevent Samba from following symbolic links in one file share to files that are not in the share.

- It is turned on by default, since following links in Unix is not a security problem, but turning it off requires extra processing on every file open.
- If you turn off wide links, turn on getwd cache to cache some of the required data.
- There is also a follow symlinks option that can be turned off to prevent following any symbolic links at all, but the option does not pose a performance problem.

getwd cache option caches the path to the current directory, avoiding long tree-walks to discover it.

- It's a good performance improvement on a printer server or if wide links are turned off.
