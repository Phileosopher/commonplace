
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

The reason OSPF is so powerful and used constantly, though, is that it's physically impossible for the shortest path to also contain loops.

- As an example, if a path from A to F goes through A-B-C-D-E-F, and E happens to be the same as B, then A-B/E-F is shorter and avoids loops.
- For this reason, it's a dogmatic rule that OSPF is constantly followed.
  - This means that both sides of a connection will very frequently mirror their path information, though not always.
  - The waterfall/continental divide model will prevent one node along the path from broadcasting to a later node, thereby creating a one-way path.
  - The P/Q model divides out the network into separate paths to allow traffic to flow down P or Q without interacting with the other path.
- The effort to find the path is inductive, *not* deductive, so in practice it's often not ideally optimized.
- In practice, finding that shortest path comes through maintaining Minimum Spanning Tree (MST) and Shortest Path Tree (SPT) topologies. MST visits each node and examines their overall cost, while SPT counts the hops.

## Signal transmission

Sometimes the sender is simply sending data too fast for the receiver to get it, creating a buffer overflow. To avoid this, the signaling to express non-receipt must be implicit or explicit.

- Implicit signaling, which is the most common, means the transmitter assumes the packet hasn't been received due to some type of context about the traffic stream (e.g., the receiver didn't acknowledge receipt of the packet).
- Explicit signaling means the receiver is directly informing the sender that a packet hasn't been received.

Windowing is the most widely deployed method:

1. A transmitter sends some information, then waits before deciding if the information was sent correctly.
2. If the receiver acknowledges receipt within a specified amount of time, the transmitter sends more information.
3. If the receiver doesn't acknowledge receipt within that window of time, the transmitter sends the same information.

Sometimes a link aggregation scheme will take multiple physical links and bundle them into a single virtual link. For the sake of the protocols, this is considered a single physical link, but the actual link speeds do *not* scale in proportion (i.e., 2 10Gbps links do not, in fact, make 20Gbps in practice).

- To manage out-of-order packets, it computes a hash from specific packet header fields to make a consistent hash throughout the transmission.
  - The easiest form of hashing involves adding the digits of numbers together (e.g., 2105 becomes 8).
  - Typically, the 5-tuple fields are used: source and destination IP, source and destination port, and protocol.
- The protocol for handling this is the Link Aggregation Control Protocol (LACP) from the IEEE 802.3ad standard.
  - It establishes a link, but then recalculates the flow hash if any links inside the connection go down.
- Very often, any combined links will be unevenly load-balanced, so they will not reflect identical capacities.
- There is also Multichassis Link Aggregation (MLAG) by the Arista corporation, which allows a single aggregated link bundle to span multiple network switches.
  - This is usually for physical redundancy than actual speed.
  - MLAG is proprietary, so its spirit remains even while most networks shy away from it.

Signals are *not* completely reliable:

- Over distance and with interference, the signal will "attenuate".
- Also, over long distances the signal will have a "latency" to it, especially when it's bouncing through many routers (such as the internet).
- And, because of strange and unpredictable interference, signals will often have "jitter" that makes the latency and attenuation wobble around.
- Because of how cheap UTP cables are and how convenient Wi-Fi is, *nearly everything* in a nearby network will suffer from "crosstalk".

By far, jitter is the worst type of network issue because it's often hard to pinpoint exactly what causes it.

Detecting a device that's down is a complex issue, and there are several ways to go about it.

- The source of the signal defines the context of what happens:
  - In-band polling requests the device's status from a neighboring node.
  - Out-of-band polling requests the device's status from beyond a neighbor.
  - Event-driven updates are triggered by the requesting device when something else happens (e.g., a TCP connection fails).
- There are four major factors that affect the information coming back from the device or link:
  1. Device sends out its status
     - OOB: a centralized system gives the status, and it gives a big-picture view of the network
     - IB+ED: local devices send information without the big-picture view and each one needs to send its own information
  2. The forwarding state is tied to the state of the link or device
     - OOB: the state can be falsely reported and isn't tested
     - IB+ED: the link and device state can connect with its forwarding ability
  3. Detection speed
     - OOB+IB: slower to avoid false positives
     - ED: a set timer to avoid false positives, but it's much faster and can be a short time window
  4. Scaling
     - OOB+IB: needs periodic polling that scales within predictable limits
     - ED: tends to scale better than polling
- Event-driven detection seems better overall, but many uses cases make polling better.
- Once a device is informed about a change, it can send information to nearby devices to propagate and update those changes.
  - Flooding sends *all* relevant information to the other devices.
  - Hop-by-hop will simply send all local hop-based information to all its neighbors.
  - A centralized store can also hold all the relevant information instead.

## Transferring through a computer

Unless the signal travels directly on a medium, it will change as it travels.

- Its "time to live" (TTL) will decrement by 1 as it is routed.
- Depending on where it's going, header information may be removed or updated.

As it travels through the computer, it may go down several pathways:

1. Input to main memory and then to an interrupt (which schedules another process in the GPP for later), then possibly to a switching application that modifies the packet.
   - This is called process switching, and is considered the slow path.
2. Input to main memory but then the *input device* sends an interrupt and processes the packet, then to output.
3. Input to an application-specific integrated circuit (ASIC) or its memory with an interrupt, the ASIC treats the interrupt as a packet switch, then sends it to output.
   - This is the high-speed solution, since the interrupt triggers an automatic conversion and it avoids the main [CPU](cs-cpu.md) entirely.

The bus, or fabric, is built into an internal network called a Clos network:

- There are 3 stages: ingress, middle, and egress.
- Each stage has switches called crossbars to connect them.
- The network is built where every ingress crossbar can route to any middle stage crossbar, which can then route to the relevant output.
- The entire system is built on highly precise timing, and the experience is a miniature version of a driver transferring highways (i.e., wait A minutes then get off on exit B, then wait C minutes to get off on exit D).
- Another implementation is called the spine and leaf fabric.
- To avoid contention (multiple packets sending to a single receiver at the same time), the switch will either use an input queue or use multiple virtual output queues (VOQ) per input port.
- the iSLIP algorithm manages crossbar fabric by scheduling traffic to avoid contention:
  1. Request: all ingress with queued traffic ask their egress if they can send.
  2. Grant: each egress determines which ingress should send, doing it round-robin if there are multiple.
  3. Accept: the egress only moves to the next request when it receives a Grant from the ingress
- There are also variations to iSLIP to alter traffic such as prioritized, threshold, and weighted iSLIP.

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

When mapping devices, the device builds a database of known IPs, which it updates as it detects or fails to detect other devices.

- Since computers are the world's fastest idiots, there's a tradeoff between the amount of routing information the device carries and how fast it runs, so constantly purging obsolete information is crucial for a faster network.
- It can reactively learn other devices by simply logging new devices that send packets to it. This takes a comparatively long time, and the entry cache is complicated to purge.
- Alternately, there are four major ways to proactively learn about other devices:
  1. Any type of neighbor discovery protocol that runs between nodes (usually ARP or IPv6 ND). It doesn't usually indicate timely information on whether it's reachable, though.
  2. Device configuration that indicates a network hub that maintains reachability information.
  3. An identity service where nodes register, a bit like a phone directory.
  4. An address management system that maintains locations. This is uncommon, though.

## QoS

Maintaining a network's quality of service (QoS) can be challenging when networks become congested.

- For various reasons (often tied to money), most bandwidth QoS issues are spikes in traffic, and they are usually resolved with specific configurations more than new hardware.

One of the most common money-based discrepancies ties to worse networks over WANs versus local networks.

- As a matter of scale, long-distance networks are more expensive, even when a massive corporation can do it as affordably as possible.
- For that reason, long-distance network costs are more heavily scrutinized than short-range networks like buildings or campuses.

There are various typing services for QoS, and they're all trying to strictly classify the importance of various types of data.

- One of the more popular QoS protocols defined in RFC 2474 is a 6-bit field in IP packets called Differentiated Services Code Point (DSCP), with the field itself called the Type of Service (ToS) field.
- Preferably, any marking that classifies traffic should be marked as closely to the source computer as possible, preferably the ingress point or the sending application itself.
- As the QoS data moves from a trusted domain to an untrusted one, the packets wil be stripped of the marked data.
- To avoid losing QoS packet crafting when tunneling (e.g. VPNs), the marking is reflected in what's called ToS reflection. In the process, the marking often changes to reflect a new value that the service provider (SP) will honor, and may only use 3 bits (thereby losing specificity in the process).
  - The 3-bit marking, in particular, explains part of why tunneling can make your network performance weird (slows down things and speeds up things seemingly at random).

When transmitting information over the public Internet at large, it's a lot cheaper than private network management in institutions, but is also a complete black box to the private parties.

- The answer is to work around the uncontrollable Internet factors by controlling what happens *before* the traffic enters the public Internet. This includes heavily controlling all "edge" traffic as well as path selection for outgoing packets.

Just because the QoS packets are marked doesn't necessarily mean the devices will respect those markings, and that part is defined by the device's policy.

- When congestion is happening (i.e., the packets go to an egress queue instead of an egress transmit ring), most policies default to FIFO (first in first out), which works great in most cases (e.g., HTTP).
- However, sometimes traffic packets should be moved to the head of the queue and sent as quickly as possible to avoid any delay (e.g., VoIP).
- To ensure delivery when timing is less important than avoiding packet drops, the technique is often managed by class-based weighted fair queueing (CBWFQ), where traffic classes are serviced according to the policies they've been assigned with a philosophy toward fairness.
- At the same time, well-written QoS policies will have clear instructions about whether the traffic must be delivered (even if late), must be delivered rapidly, or must not starve bandwidth from other traffic classes.

Traffic shaping is an elegant solution for moving traffic correctly.

- Instead of dropping packets, the higher-priority packets will have imposed limits on packet size during congestion.
- Elephant flows are specific traffic shaping where long-lived traffic moves large amounts of data between endpoints as quickly as possible. They typically override other traffic, so they need to be shaped to permit service to other traffic classes.

Policing is an alternative to traffic shaping, where excess (nonconforming) traffic is treated more harshly and dropped immediately.

- While this behavior works well enough, one consequence of it is that TCP will start the ramp-up process all over again, and the bandwidth graph will look like a sawtooth.
- Policing can also be used to re-mark nonconforming traffic to a lower-priority DSCP value instead of dropping altogether.

Packets can be delayed in a buffer, and this sounds great. However, full buffers create extra problems (bufferbloat).

- To avoid buffer limits and its consequences (the oldest packets in the buffer get dropped), many devices use active queue management to drop packets or minimize the time a packet spends in a buffer.
- Random early detection (RED) will proactively drop randomly selected inbound traffic to keep space, with a higher likelihood of dropping any given incoming packet as the buffer fills.
  - It has been added to with Weighted Random Early Detection (WRED), whic considers the incoming traffic's priority based on its mark. Further, its drops also signal any windowed transport (e.g., TCP) that the transmitter needs to slow down.
- The intuition for many would be to increase the size of the buffer to ensure packet transmission, but it can often create even more delays due to the fact that there are no signals sent while the packet sits in a buffer (i.e., no signal to indicate it was dropped for TCP, longer delays for UDP).

## Long-distance routing

"Wide area networks" (WANs) are LANs spread out across a huge area. They can cover vast geographical regions (including across oceans or in space), and are often connected with enormous trunk lines.

Before the internet, a WAN used to be an expensive enterprise option for corporations. Now, most of the internet is WANs through an interconnected grid of cellular networks, satellite networks, and cable/phone internet.

There are sometimes multiple ways for a signal to travel across long distances. There are two ways to decide the best option:

- Link-state routing protocol - build a map of switches connected to each other and picks the route with the fewest jumps between switches. This typically uses the "open shortest path first" (OSPF) protocol to send "link state advertisements" to find open IP addresses.
- Distance-vector routing protocol - build a map that measures the times for a signal to travel (accounting for latency and other issues) and picks the shortest route by perceived distance.

An emerging model is called the Software-Defined Wide Area Network (SD-WAN), which pools together multiple WAN circuits into a pooled bandwidth.

- This allows redundancy and reliability, since it'll keep performing QoS testing and send the data down the less congested path for each hop.

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
