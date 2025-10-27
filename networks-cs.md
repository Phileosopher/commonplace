
# Computer networks explained

A "network" is a bunch of computers put together. They're loosely connected, and computers can go off and on the network. Since *all* the computers can be replaced by new ones, a network is more an abstraction than any fixed structure.

There is a vast body of network [standards](standards-computers.md) published and maintained through [the IETF](https://datatracker.ietf.org/). They distill into many RFCs (Request For Comment) that indicate precisely how a computer should be programmed to manage various protocols.

[Cybersecurity](computers-cysec.md) is the general set of practices of what computers should *not* take as input, since other computers and people aren't always worth trusting.

## History

The history of computer networks has conventions and [standards](standards-computers.md) dating as far back as the telegraphs and Morse code in the 1840's, and phone switchboards are still networking standards (66 block vs. 110 block). WiFi and cellular networks, though, go back to radio standards set in the 1920's.

The idea of networked computers came *long* before it materialized. Vannevar Bush's essay "[As We May Think](https://en.wikipedia.org/wiki/As_We_May_Think)" implied the concept of a collective memory storage that represented something close to how we see [the internet](computers-sofware-webdev.md) today.

At first, the network connections between computers were small-scale and designed to connect [scientists](science.md) together. As early as the 1970s, they sent the information via analog signals encoded as sound through existing phone lines. "Modems" were originally sending typed punchcard information, 3 [ASCII characters](computers-keyboard.md) at a time (which converted to 25 bits/s).

As the computers started sending more information back-and-forth using "store and forward" networking, the engineers faced a potentially severe problem: relatively small files were getting bogged down because they were behind the queue for much larger files transferring across the network. Their solution was relatively simple: divide the information into small blocks of data called "packets", which will each operate as separate units for transfer. This allowed quite a few benefits:

- Other data could interrupt the transfer whenever needed without any concern of breaking the flow of data.
- The packets could be sent in no particular order, if needed.
- If any packets were lost ("dropped"), they could be re-sent instead of the entire thing.
- If the network changed (e.g., slow or bad connection, faster alternative connection), the rest of the packets could travel a different path without any concern for the flow of information.

For a long time through the 1990's, until broadband internet, the capacity for data transfer through a modem was capped at 56,000 bits per second, or 56k baud.

## Topology

There are different types of conventional network "topologies" to connect computers with other computers:

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

Generally, any network topology that values complete "redundancy" should have 2 backup connections for every connection. This can be expensive depending on how it's implemented, so most [enterprise IT](computers-distsys-enterprise.md) only keeps 1 unless they're [very large](faang.md).

## Protocols/layers

Due to the complexity of a computer network, there is [a specific set of layers](networks-cs-layers.md) to understand how network information is sent.

## LANs

"Local area networks" (LANs) are the sections of the network that you have more direct control over. It's the first historical foray into networked computers. Most LANs use shared resources, such as file servers.

Besides having private IP addresses on that local network, wireless networks have a "service set identifier" (SSID) as an ID for users to find it. It can be "Family WiFi" or "PETA Van", but can also be "!" or "#". If it isn't [password-protected](computers-cysec-authentication.md), anyone who knows it or can scan wireless networks will be able to access it.

In a telephone system, one implementation of a LAN is a PBX (private branch exchange). When it's customer-facing, it typically has pre-recorded audio with it to communicate what the users can press. However, a phone is still simply a computer interface with a dialpad-only input and audio-only output.

There are several features that router/switches often come equipped with. For cybersecurity reasons, it's worth knowing their features.

## Long-distance routing

"Wide area networks" (WANs) are LANs spread out across a huge area. They can cover vast geographical regions (including across oceans or in space), and are often connected with enormous trunk lines.

Before the internet, a WAN used to be an expensive enterprise option for corporations. Now, most of the internet is WANs through an interconnected grid of cellular networks, satellite networks, and cable/phone internet.

There are sometimes multiple ways for a signal to travel across long distances. There are two ways to decide the best option:

- Link-state routing protocol - build a map of switches connected to each other and picks the route with the fewest jumps between switches. This typically uses the "open shortest path first" (OSPF) protocol to send "link state advertisements" to find open IP addresses.
- Distance-vector routing protocol - build a map that measures the times for a signal to travel (accounting for latency and other issues) and picks the shortest route by perceived distance.

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

1. Carriers [have access to *all* the information that travels through their system](faang.md).
2. They can also shut off or throttle data at their discretion.

There are only 3 ways to keep carriers accountable to prevent abuse:

1. [Use end-to-end encryption](encryption.md), which is a matter of [each person responsibly making those decisions](computers-cysec.md).
2. [Enact laws to prevent their misuse](people-rules.md), which requires [government intervention](groups-large.md).
3. [Maintain a competitive free market](economics.md), which requires government *non*-intervention.

## Further learning

[Specific networking trivia](networks-cs-specific.md)

[Practical Networking](https://www.practicalnetworking.net/)

[Hello IPv6: a minimal tutorial for IPv4 users](https://metebalci.com/blog/hello-ipv6/)

[Observing my cellphone switch towers](https://fabiensanglard.net/lte/index.html)
