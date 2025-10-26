
[macOS Sonoma Boot Failures | Hacker News](https://news.ycombinator.com/item?id=38089342)
[macOS Sonoma Boot Failures · AsahiLinux/docs Wiki](https://github.com/AsahiLinux/docs/wiki/macOS-Sonoma-Boot-Failures)

[Making EC2 boot time faster | Hacker News](https://news.ycombinator.com/item?id=40455208)
[Making EC2 boot time 8x faster](https://depot.dev/blog/faster-ec2-boot-time)

[Booting Linux off of Google Drive | Hacker News](https://news.ycombinator.com/item?id=40853770)
[Booting Linux off of Google Drive | Ersei 'n Stuff](https://ersei.net/en/blog/fuse-root)

## guides

[Ask HN: Where can I find a primer on how computers boot? | Hacker News](https://news.ycombinator.com/item?id=35229045)

[What happens when a CPU starts | Hacker News](https://news.ycombinator.com/item?id=34333638)
[lateblt.tripod.com/bit68.txt](https://lateblt.tripod.com/bit68.txt)

## bootloader

[No more boot loader: Please use the kernel instead | Hacker News](https://news.ycombinator.com/item?id=40907933)
[No more boot loader: Please use the kernel instead :: DevConf.CZ :: pretalx](https://pretalx.com/devconf-cz-2024/talk/W3AVCT/)

[Writing a BIOS bootloader for 64-bit mode from scratch | Hacker News](https://news.ycombinator.com/item?id=40959742)
[Setting up an x86 CPU in 64-bit mode](https://thasso.xyz/2024/07/13/setting-up-an-x86-cpu.html)

[Managing EFI Boot Loaders for Linux: Controlling Secure Boot](https://rodsbooks.com/efi-bootloaders/controlling-sb.html)

## BIOS

[I have come to bury the BIOS, not to open it [video] | Hacker News](https://news.ycombinator.com/item?id=33145411)
[I have come to bury the BIOS, not to open it: The need for holistic systems - OSFC](https://www.osfc.io/2022/talks/i-have-come-to-bury-the-bios-not-to-open-it-the-need-for-holistic-systems/)

[Investigating a vanishing BIOS on the Fujitsu Lifebook AH532 | Hacker News](https://news.ycombinator.com/item?id=39070871)
[Investigating a vanishing BIOS on the Fujitsu LIFEBOOK AH532 | timschumi's low-traffic blog](https://blog.timschumi.net/2024/01/20/ah532-bios-investigation.html)

### UEFI

[Responsible stewardship of the UEFI Secure Boot ecosystem | Hacker News](https://news.ycombinator.com/item?id=32066919)
[mjg59 | Responsible stewardship of the UEFI secure boot ecosystem](https://mjg59.dreamwidth.org/60248.html)

[Intel OEM Private Key Leak: A Blow to UEFI Secure Boot Security | Hacker News](https://news.ycombinator.com/item?id=35843566)
[Intel OEM Private Key Leak: A Blow to UEFI Secure Boot Security](https://securityonline.info/intel-oem-private-key-leak-a-blow-to-uefi-secure-boot-security/)

### GRUB

[A Grub theme in the style of Minecraft | Hacker News](https://news.ycombinator.com/item?id=36771980)
[Lxtharia/minegrub-theme: A Grub Theme in the style of Minecraft!](https://github.com/Lxtharia/minegrub-theme)

[Is there any work going on in Fedora to depend less on grub? : Fedora](https://old.reddit.com/r/Fedora/comments/xhl5q0/is_there_any_work_going_on_in_fedora_to_depend)

## SBAT

[What is an SBAT and why does everyone suddenly care | Hacker News](https://news.ycombinator.com/item?id=41318222)
[mjg59 | What the fuck is an SBAT and why does everyone suddenly care](https://mjg59.dreamwidth.org/70348.html)

## beginner guides - dual boot

[How to Dual Boot Windows 10 and Ubuntu - Linux Dual Booting Tutorial](https://www.freecodecamp.org/news/how-to-dual-boot-windows-10-and-ubuntu-linux-dual-booting-tutorial)

[Wrong Time Displayed in Windows-Linux Dual Boot Setup? Here's How to Fix it](https://itsfoss.com/wrong-time-dual-boot)

## specific guides - macos

[Vinod Yalburgi](http://www.ibtimes.co.uk/how-install-os-x-yosemite-new-partition-dual-boot-mavericks-1451812)
How to Install OS X Yosemite on New Partition and Dual-Boot with Mavericks

[GitHub - thyrlian/MacManual: Installation and Setup Guide](https://github.com/thyrlian/MacManual)

# specific - Throttlestop guide

Use at your own risk

Throttlestop is generally used to undervolt the cpu on locked desktops or laptops. It is a very powerful tool capable of increasing cpu performance when used correctly. If your cpu temperatures typically exceed 60c while playing, I would recommend only undervolting.

My current recommendation is to use Throttlestop v9.0.

## Main Screen

Set Clock Mod to 100% and Set Multiplier to max value. The Multiplier is what multiplies the base clock of the cpu, typically 100. Untick Power Saver, BD Prochot, Speedstep, and C1E.

Click Stop Data on the Main Screen! You'll need to do this every time you open Throttlestop. There's no need for it to track temperatures unless you're using it for monitoring purposes.

## FIVR

Lock Non-Turbo Ratio to the highest possible value. Simply typing 99 in the box will set it to max. Set Turbo Limits to max. Hold the right arrow on the BOTTOM cpu core and the rest should automatically follow. Check Disable and Lock Turbo Power Limits. Set the Cache Min/Max to the highest available value. Skip undervolting for now.

## TPL

Set Short/Long Power to max value (just type 9999). Drag Turbo Time Limit slider to max value. Tick Speed Shift and set Min/Max to 255. Tick start SpeedShift when Throttlestop starts. This will lock the CPU to max speed. Untick PP0 Power Limit (this setting will cause temperature increases. Highly recommended to avoid if you have high temps already). Tick Intel Power Balance and set CPU to 31 and GPU to 0 (unless you use the iGPU). This gives priority to the CPU over the GPU when the TDP limit is met.

## C1

Click the arrow on the right to bring up the C-States control pane. Set Request to C1 and untick all the boxes below. Click Apply and then Ok.

## Options

You can force Timer Resolution via Throttlestop. Set AC Timer Res to 0 and the Timer Res value will go to 0.5

## Undervolting

THERE IS NO "BEST"! Every CPU is different, and depending on your chip, you may get a better or worse undervolt than someone with the same CPU as you. This requires TESTING! Go back to the FIVR window, and adjust CPU Core and Cache. To unlock the screen, tick Unlock Adjustable Voltage. My advice is to start with an Adjustable voltage and adjust the Offset, going as low as possible before you experience freezing or loss of performance. After reaching your limit, monitor your Voltage under load. Use a stress test for this. You'll need to press Start Data on the main screen if you previously stopped it. Find the max value your CPU hits, and then change the voltage type to Static for both core and cache. Set the Voltage slider equivalent to the max voltage your cpu hits, and set to Offset to 0. In my experience, this provides a slight performance increase over Adaptive voltage when properly used, and can even shave off a few degrees under load.
