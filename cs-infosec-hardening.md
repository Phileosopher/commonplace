
# Network and OS hardening

Making a [computer network](cs-networks.md) involves adding communication features between computers. By contrast, [network hardening](cs-infosec-cysec-network.md) involves *removing or disabling* all unnecessary features authorized users won't use.

The actual methods for hardening are often very, very common-sense:

- Turn off things you don't use, especially if they're internet-facing.
- Enable a firewall.
- Use [good passwords](cs-infosec-authentication.md).
- Keep all software [up to date](cs-software-versionctrl.md).
- Be suspicious of *everything* that's even remotely unusual.

## Specific network hardening tricks

As a general rule, do *not* download proprietary apps when you can use a web browser.

- Many people have become accustomed to downloading proprietary apps due to convenience, but most of the time the apps expand the attack surface and add tracking software.

If you're particularly paranoid, make sure to change your devices' MAC address, since that MAC has the origination and likely information about the firmware on it.

Have a burner browser to work with any suspicious situations.

- Even if you use privacy-minded things browser features (e.g. private windows, no cookies), some services will still detect other content in that browser.
- For this reason, have a "burner" browser that has absolutely nothing in it.
- Preferably, it should use a different framework (e.g., Firefox uses Gecko, Brave uses Chromium)

While wired networks are safer than wireless, some natural threats exist on all networks.

- To avoid an ICMP flood, block ICMP packets in a firewall.
- To avoid DoS or DDoS, use an anti-DoS/DDoS device to filter traffic.
- To avoid a fraggle attack, disable IP broadcasting and use the firewall to block ICMP packets.

Wireless networks are particularly risky, since they're effectively a hub to all devices within physical range.

- To avoid wardriving, hide the SSID.
- To avoid WEP and WPA cracking, set up a stronger encryption protocol (at least WPA2).
- To prevent war driving, decrease the wireless access point's range and hide the SSID.
- To prevent war chalking use WPA2, enable MAC filtering and hide the SSID.
- To avoid evil twin attacks, deploy a Wireless Intrusion Prevention System (WIPS).
- To prevent a rogue access point on your network, enable switch port tracing, use monitor mode scanning, or use a rogue detector.

If the network is connected to the internet and [has a website](cs-software-webdev.md), it has other issues.

- To prevent injections, use server-side validation and sanitize *all* input data.
- To mitigate broken authentication, use multi-factor authentication and complex passwords.
- To avoid sensitive data exposure to man-in-the-middle attacks, encrypt all data in transit and disable caching.
- To avoid the risks of a misconfigured security policy, disable all unnecessary features and services and focus on hardening the OS itself.

Sadly, overflow attacks require some level of [software debugging](cs-software-redesign.md) to detect vulnerabilities in the code.

[Virtual machines](cs-distsys-vm.md) over a network (i.e., [cloud](cs-distsys-cloud.md)) present a host of other issues.

- Stay updated, since missing updates are often exploits waiting to happen.
- A compromised hypervisor can become a breached OS.
- Since VMs are so easy to spin up, there's a very real risk of "VM sprawl", where there are too many VMs with important information.
- By not monitoring VNet traffic, all sorts of issues come around.
