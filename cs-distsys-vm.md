
# Virtualization, virtual machines, and emulation

"Virtualization" is splitting physical resources to make logical divides. It never changes the physical realities of the thing, but simply does one of several things:

1. Slices up the physical components into entirely separate logical divisions.
2. Combines the physical components into one single logical whole.
3. Does some funky combination of both, where it first combines and then separates the whole (e.g., 2 1TB hard drives made into one single 2TB virtual hard drive, then segmented into 1.5TB and 0.5TB hard drives).

This is a layer of abstraction that adds complexity (and therefore headache and [cybersecurity risks](cs-infosec.md)), but there are many times it can be useful.

- Sometimes a device only outputs information according to a specific [protocol](cs-standards.md) that isn't the receiving device's, or the other way around, and a virtual connection makes the device oblivious to that discrepancy.
- If you need to [encrypt](encryption.md) data across a network, you can use a tunnel, which is a specific type of network virtualization. You can also do this in layers to make onion routing for added [security](cs-infosec.md).
- You can save money on computers by using a few big computers and routing everything to workstations.
- A virtual bandwidth configuration allows for multiple connections to be redundant, but not require the rest of the systems to have to figure out which connection to use.
- Multiple small computers can work together as if they were one big computer.

One of the biggest risks from virtualization abstraction is the fact that every abstraction creates a black box underneath it.

- When something breaks, the technicians managing the abstractions won't know why.
- If a service is designed as a backup for another service, but they both share the same component, that component breaking will make them *both* fail and the entire purpose of redundancy was useless.

Virtual networking has been around for a very long time, but virtual machines are relatively newer. In practice, a virtual machine is slicing up computer to make it behave like it's several computers at once, or for a user experience of a computer-in-a-computer.

## Extra Processing

As computers have gotten faster, they end up having enough processing power to do *much* more work than the typical load that they're given, along with *much* more memory than necessary and lots of extra long-term storage space to burn. Some engineers were smart enough to take advantage of this.

Virtualization makes "virtual machines" inside the main computer, with each one pulling some resources from the actual computer. For example, a very fast computer could have multiple screens, multiple keyboards, and multiple mice, and everyone would treat it as if it were several computers. At scale, this can save a lot of money.

There are also "containers", with the key difference being that containers all share the same kernel while virtual machines have separate kernel instances. To the end user it makes no difference, but VMs are more [secure](cs-infosec.md) and containers are easier to spin up.

This can also work the other way, with multiple processors that feed into a shared resource pool. The system is how [enterprise](cs-distsys-enterprise.md)-grade software is relatively easy to set up without too much configuration.

## Extra Networking

Along with combining processors, some virtualization settings can combine multiple network cards together. Windows calls it NIC teaming and Linux calls it NIC bonding, but it's basically combining multiple network adapters together to act as if they were one network adapter bandwidth unit.

## Hypervisors

Virtual machines are run by a "hypervisor", which can either be Level 1 or Level 2. Level 1 hypervisors are run directly by the [BIOS](cs-boot.md), while Level 2 hypervisors work inside the [OS](cs-os.md). Level 1 is ideal if you want speed, but Level 2 is easier to set up.

A hypervisor can allow you to manage many computers at once if you need. For example, VMware has vSphere and vSAN. This may include [group policies](cs-infosec-compliance.md), managing [memory](cs-memory.md) or [processor](cs-cpu.md) use, or running [updates](cs-software-maintenance.md).

## Emulators

Underneath virtualization, emulation has a different sort of purpose.

Emulators have been around for decades. An emulator is software designed to reproduce conditions of different hardware to make *other* software work. This can be a far simpler and localized issue than trying to reproduce an entire computer.

For example, you may want to run Windows on your computer, but you only have Linux. By running a program (in this case, the software called Wine), you can make the Linux operating system act like it has Windows on it, at least enough to fool the program you're trying to run inside it.

This isn't always foolproof (there are usually glitches), but emulation gets the job done. In fact, it's often the only way to successfully (though not always [legally](legal-ip.md)) play many older [games](cs-software-gamedev.md) that haven't been published in decades (e.g., Atari, Game Boy, Super Nintendo).

Emulation is also far more common than most people may realize. To accommodate the 32-bit processing on a 64-bit processor, Windows uses the WOW (Windows on Windows) protocol to emulate an old system.

## Complicated

Setting up VMs has become trivially easy: a few clicks and you're done.

However, there are multiple issues that come with their simplicity:

1. You can assign virtual resources ([CPU](cs-cpu.md), [RAM](cs-memory.md), memory, [bandwidth](cs-networks.md)) that aren't actually corresponding to reality. For example, you may set a VM to have 150 GB of hard drive when there's only 40 GB of free space. You won't know that these resources are getting overloaded until you do, and something will crash. In a [business environment](cs-distsys-enterprise.md), this can cost money from being an unreliable service provider.
2. Since it's so easy to spin up a VM, it's also easy to lose track of all the VMs and what VM does what. At that point, it creates a "VM sprawl", where it's difficult to remember which VM tracks what. The only solution to this is to plan ahead and keep good [documentation](language-writing-documentation.md) on the matter.
3. There's an inherent [cybersecurity issue](cs-infosec-pentest.md) that comes through a "VM escape". A hacker can use exploits to break out of the VM box and gain access to the primary system.
