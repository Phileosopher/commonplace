
# Virtualization and emulation

"Virtualization" is splitting a computer to make it behave like it's several computers at once, or for using a computer-in-a-computer.

## Extra Processing

As computers have gotten faster, they end up having enough processing power to do *much* more work than the typical load that they're given, along with *much* more memory than necessary and lots of extra long-term storage space to burn. Some engineers were smart enough to take advantage of this.

Virtualization makes "containers" inside the main computer, with each one pulling some of the resources from the actual computer. For example, a very fast computer could have multiple screens, multiple keyboards, and multiple mice, and everyone would treat it as if it were several computers. At scale, this can save a lot of money.

This can also work the other way, with multiple processors that feed into a shared resource pool. The system is how [enterprise](computers-distsys-enterprise.md)-grade software is relatively easy to set up without too much configuration.

## Extra Networking

Along with combining processors, some virtualization settings can combine multiple network cards together. Windows calls it NIC teaming and Linux calls it NIC bonding, but it's basically combining multiple network adapters together to act as if they were one network adapter bandwidth unit.

## Hypervisors

Virtual machines are run by a "hypervisor", which can either be Level 1 or Level 2. Level 1 hypervisors are run directly by the [BIOS](computers-boot.md), while Level 2 hypervisors work inside the [OS](computers-os.md). Level 1 is ideal if you want speed, but Level 2 is easier to set up.

A hypervisor can allow you to manage many computers at once if you need. For example, VMware has vSphere and vSAN. This may include [group policies](computers-cysec-compliance.md), managing [memory](computers-memory.md) or [processor](computers-cpu.md) use, or running [updates](computers-software-maintenance.md).

## Emulators

Underneath virtualization, emulation has a different sort of purpose.

Emulators have been around for decades. An emulator is software designed to reproduce conditions of different hardware to make *other* software work. This can be a far simpler and localized issue than trying to reproduce an entire computer.

For example, you may want to run Windows on your computer, but you only have Linux. By running a program (in this case, the software called Wine), you can make the Linux operating system act like it has Windows on it, at least enough to fool the program you're trying to run inside it.

This isn't always foolproof (there are usually glitches), but emulation gets the job done. In fact, it's often the only way to successfully (though not always [legally](legal-ip.md)) play many older [games](computers-software-gamedev.md) that haven't been published in decades (e.g., Atari, Gameboy, Super Nintendo).

Emulation is also far more common than most people may realize. To accommodate the 32-bit processing on a 64-bit processor, Windows uses the WOW (Windows on Windows) protocol to emulate an old system.

## Complicated

Setting up VMs has become trivially easy: a few clicks and you're done.

However, there are multiple issues that come with their simplicity:

1. You can assign virtual resources ([CPU](computers-cpu.md), [RAM](computers-memory.md), memory, [bandwidth](networks-computer.md)) that aren't actually corresponding to reality. For example, you may set a VM to have 150 GB of hard drive when there's only 40 GB of free space. You won't know that these resources are getting overloaded until you do, and something will crash. In a [business environment](computers-distsys-enterprise.md), this can cost money from being an unreliable service provider.
2. Since it's so easy to spin up a VM, it's also easy to lose track of all the VMs and what VM does what. At that point, it creates a "VM sprawl", where it's difficult to remember which VM tracks what. The only solution to this is to plan ahead and keep good [documentation](documentation-technical.md) on the matter.
3. There's an inherent [cybersecurity issue](computers-cysec-pentest.md) that comes through a "VM escape". A hacker can use exploits to break out of the VM box and gain access to the primary system.
