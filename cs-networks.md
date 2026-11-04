
# Computer networks explained

A "network" is a bunch of computers put together. They're loosely connected, and computers can go off and on the network. Since *all* the computers can be replaced by new ones, a network is more an abstraction than any fixed structure.

There is a vast body of network [standards](cs-standards.md) published and maintained through [the IETF](https://datatracker.ietf.org/). They distill into many RFCs (Request For Comment) that indicate precisely how a computer should be programmed to manage various protocols.

The entire concept of network design is strapped together with absurdly over-defined standards, each one creating so much order that they interfere with other standards, arranged in a stack of functional-but-imperfect implementations that are mostly reliable but an absolute pain to decipher.

[Cybersecurity](cs-infosec.md) is the general set of practices of what computers should *not* take as input, since other computers and people aren't always worth trusting.

## History

The history of computer networks has conventions and [standards](cs-standards.md) dating as far back as the telegraphs and Morse code in the 1840s, and phone switchboards are still networking standards (66 block vs. 110 block). Wi-Fi and cellular networks, though, go back to radio standards set in the 1920s.

The idea of networked computers came *long* before it materialized. Vannevar Bush's essay "[As We May Think](https://en.wikipedia.org/wiki/As_We_May_Think)" implied the concept of a collective memory storage that represented something close to how we see [the internet](cs-sofware-webdev.md) today.

At first, the network connections between computers were small-scale and designed to connect [scientists](science.md) together. As early as the 1970s, they sent the information via analog signals encoded as sound through existing phone lines.

- "Modems" were originally sending typed punchcard information, 3 [ASCII characters](cs-keyboard.md) at a time (which converted to 25 bits/s).
- The ideal packet size for carrying voice traffic is 48 octets (or 384 bits), but the minimum ideal for data transmission is 64 octets (512 bits). For a while, asynchronous transfer mode (ATM) sent 53 octets as a happy medium, but the data transport protocols were sending two packets of 53 and 9 octets with the other 42 being empty space. This was a failure, but the ATM project's label switching and fixed cell size maintains itself throughout networking projects.

As the computers started sending more information back-and-forth using "store and forward" networking, the engineers faced a potentially severe problem: relatively small files were getting bogged down because they were behind the queue for much larger files transferring across the network. Their solution was relatively simple: divide the information into small blocks of data called "packets", which will each operate as separate units for transfer. This allowed quite a few benefits:

- Other data could interrupt the transfer whenever needed without any concern of breaking the flow of data.
- The packets could be sent, sometimes in no particular order, along a label path.
- If any packets were lost ("dropped"), they could be re-sent instead of the entire thing.
- If the network changed (e.g., slow or bad connection, faster alternative connection), the rest of the packets could travel a different path without any concern for the flow of information.
- This was a hybrid of the two conventions of packet switching (breaking down data into small blocks and reassembling them on the other side) and circuit switching (holding a circuit for the data until it is fully sent).
  - Or, from another viewpoint, they decided to do circuit switching on each packet.

For a long time through the 1990s, until broadband internet, the capacity for data transfer through a modem was capped at 56,000 bits per second, or 56k baud.

- This also compounded with the extra memory cost of older standards. In 1984 it cost 1,331 MB to send 1 MB of data with the Motorola 68010, became 1:1 MB by 1999 with the Intel Pentium III, and was 0.001 MB cost for every 1 MB of data by 2014 with the Intel i7.

While networks started getting faster starting in the 1990s, there's still a major latency across large distances that has been mostly unaddressed. While most other computer events have moved from ~100-150ms to ~2-3ms, sending a packet of data across 1,000 miles still takes ~10ms no matter what.

## Topology

There are different types of conventional network "topologies" to connect computers with other computers:

- Point-to-point - Direct connection between two computers.
- Bus - One straight line: A connected to B, B to C, C to D
  - The first computer network, where *all* the information from one computer went to *all* the computers at once.
  - Engineers actually had to install a "terminator" just to prevent data from bouncing back and bringing the whole network down!
- Ring - The same as a bus, but where the last connects to the first to make a circle
  - Didn't have the issues of a bus (since it didn't need a terminator) but a broken cable would still shut down the network.
- Star - All the computers are connected to a central box.
  - This was beautiful because it introduced "fault tolerance" that permitted the network to keep working even with one cable going offline. It was also more expensive than bus or ring.
- Hybrid - A mix-and-match of the bus, ring, and star, mostly as a cost-saving measure because the star topology is awesome.
  - Stick a bus or ring inside a box, with each "port" on the outside of the box acting as a star.
  - To clarify things, there's now a distinction between discussing physical topology and signaling/logical topology.
- Mesh - Since redundancy is the perfect fault tolerance, have more than one of the computers on the network have more than one connection.
  - Partially meshed topologies have 2+ computers each with 2+ connections to other computers.
  - Fully meshed topologies have *all* the computers connected directly to *all* the other computers. Expensive, but safe.
- Tree - Effectively a combination of star and bus, connecting to a central source that feeds to the internet.

Generally, any network topology that values complete "redundancy" should have 2 backup connections for every connection. This can be expensive depending on how it's implemented, so most [enterprise IT](cs-distsys-enterprise.md) only keeps 1 unless they're [very large](cs-bigtech.md).

## Protocols/layers

At its most basic, a computer needs an IP address, subnet mask, gateway, and DNS server to connect to a typical network.

Due to the complexity of a computer network, there is [a specific set of layers](cs-networks-layers.md) to understand how network information is sent. It is an over-simplification, but allows people to understand it more easily.

The journey to finding a loop-free path (where packets aren't traveling in a circle back to a previous node) was *not* an easy problem. The approach eventually landed on the Open Shortest Path First (OSPF) protocol, but there have been three major classes of solutions to solve the issue:

- Distance vector protocols: count the cost of the path through all the hops and choose the lowest cost
- Link state protocols: use a database synchronized across devices of the pathway's hops
- Path vector: keep a record of previous hops

## Signal transmission

Sometimes the sender is simply sending data too fast for the receiver to get it, creating a buffer overflow. To avoid this, the signaling to express non-receipt must be implicit or explicit.

- Implicit signaling, which is the most common, means the transmitter assumes the packet hasn't been received due to some type of context about the traffic stream (e.g., the receiver didn't acknowledge receipt of the packet).
- Explicit signaling means the receiver is directly informing the sender that a packet hasn't been received.

Windowing is the most widely deployed method:

1. A transmitter sends some information, then waits before deciding if the information was sent correctly.
2. If the receiver acknowledges receipt within a specified amount of time, the transmitter sends more information.
3. If the receiver doesn't acknowledge receipt within that window of time, the transmitter sends the same information.

## LANs

"Local area networks" (LANs) are the sections of the network that you have more direct control over. It's the first historical foray into networked computers. Most LANs use shared resources, such as file servers.

A "virtual LAN" (VLAN) is simply a logical separation of physically associated computers.

An "IP address" is a unique identifier designed specifically for that computer. The "Internet of Things" (IoT) is clever [marketing](marketing.md)-speak for "every computer has an IP address". IoT would be harmless, but it opens up many [cybersecurity](cs-infosec.md) risks from the added connectivity.

- In a sense, the largest [cybersecurity](cs-infosec.md) risk comes through the excessive [marketing](marketing.md) that has brought out many [home automation](home-smart.md) options.
- Further, IoT can generate *tons* of useless data, which requires correctly managing.

In a simplified sense, IoT has four phases that work just like almost every other computer:

1. Input: gathers data through devices and sensors
2. Connectivity: transmits that data via a network
3. Data processing: new information derived from that data
4. Output: presentation through the user interface

Besides having private IP addresses on that local network, wireless networks have a "service set identifier" (SSID) as an ID for users to find it. It can be "Family Wi-Fi" or "PETA Van", but can also be "!" or "#". If it isn't [password-protected](cs-infosec-authentication.md), anyone who knows it or can scan wireless networks will be able to access it.

In a telephone system, one implementation of a LAN is a PBX (private branch exchange). When it's customer-facing, it typically has pre-recorded audio with it to communicate what the users can press. However, a phone is still simply a computer interface with a dialpad-only input and audio-only output.

There are several features that router/switches often come equipped with. For cybersecurity reasons, it's worth knowing their features.

## Long-distance routing

"Wide area networks" (WANs) are LANs spread out across a huge area. They can cover vast geographical regions (including across oceans or in space), and are often connected with enormous trunk lines.

Before the internet, a WAN used to be an expensive enterprise option for corporations. Now, most of the internet is WANs through an interconnected grid of cellular networks, satellite networks, and cable/phone internet.

There are sometimes multiple ways for a signal to travel across long distances. There are two ways to decide the best option:

- Link-state routing protocol - build a map of switches connected to each other and picks the route with the fewest jumps between switches. This typically uses the "open shortest path first" (OSPF) protocol to send "link state advertisements" to find open IP addresses.
- Distance-vector routing protocol - build a map that measures the times for a signal to travel (accounting for latency and other issues) and picks the shortest route by perceived distance.

## Multiple sources and destinations

Multicasting is a relatively common concept: broadcast information to many destinations at once from one source.

A less familiar concept with equal validity is anycasting: drawing information from one of multiple sources.

- The easiest solution to this is to use the same reference for all the sources. That way, the computer asking for the information will simply look for the nearest source to itself.

## Documentation

Broadly, a *huge* part of network management involves [documenting](language-writing-documentation.md) *everything* that might help later:

- A physical cable map, with a floor plan if possible
- A mapping of the ports on the network switches and where they're supposed to go
- Information about the service provider connection and how to contact them
- Any IP addresses that are allocated to the network
- A logical network diagram
- A vault with [encrypted credentials](encryption.md)
- Other useful things like layouts for the server rack and "wireless access points" (WAP), asset tracking, and a snapshot of the network's "spanning tree protocol" (STP)

It takes a terrifying amount of time to do a network audit later without any of the above documentation.

## Power

Two specific traits give carriers that control networks a *lot* of [power](power-types.md), proportional to their usage and up to legal constraints:

1. Carriers [have access to *all* the information that travels through their system](cs-bigtech.md).
2. They can also shut off or throttle data at their discretion.

There are only 3 ways to keep carriers accountable to prevent abuse:

1. [Use end-to-end encryption](encryption.md), which is a matter of [each person responsibly making those decisions](cs-infosec.md).
2. [Enact laws to prevent their misuse](people-rules.md), which requires [government intervention](groups-large.md).
3. [Maintain a competitive free market](money-economics.md), which requires government *non*-intervention.

## More information

[Specific networking trivia](cs-networks-specific.md)

[Practical Networking](https://www.practicalnetworking.net/)

[Hello IPv6: a minimal tutorial for IPv4 users](https://metebalci.com/blog/hello-ipv6/)

[Observing my cellphone switch towers](https://fabiensanglard.net/lte/index.html)
