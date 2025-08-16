
# Computer networks summarized

A "network" is a bunch of computers put together. They're loosely connected, and computers can go off and on the network. Since *all* the computers can be replaced by new ones, a network is more an abstraction than any fixed structure.

There is a vast body of network [standards](standards-computers.md) published and maintained through [the IETF](https://datatracker.ietf.org/). They distill into many RFCs (Request For Comment) that indicate precisely how a computer should be programmed to manage various protocols.

[Cybersecurity](computers-cysec.md) is the general set of practices of what computers should *not* take as input, since other computers and people aren't always worth trusting.

## History

The history of computer networks has conventions and [standards](standards-computers.md) dating as far back as the telegraphs and Morse code in the 1840's, and phone switchboards are still networking standards (66 block vs. 110 block). WiFi and cellular networks, though, go back to radio standards set in the 1920's.

The idea of networked computers came *long* before it materialized. Vannevar Bush's essay "[As We May Think](https://en.wikipedia.org/wiki/As_We_May_Think)" implied the concept of a collective memory storage that represented something close to how we see [the internet](computers-webdev.md) today.

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

Computers talk to each other with "[protocols](standards-computers.md)", which keeps the computers from misunderstanding each other. It's an elaborate version of when people say "over" and "copy" on a walkie-talkie. Protocols let *many* computers all talk seamlessly on a large system.

Over any network, the computers break up the data into small pieces that they send via these protocols.

Computers send information in roughly the same way, though the protocols and implementations vary tremendously.

1. Computer A sends out key information in a "header", "body", and "trailer":
   - The header will have a variety of content in it:
     - The type of protocol that Computer B should use
     - How many memory "words" are in the header
     - How long the entire stream of packets is and what number this one is (e.g., 2 of 2,064)
     - The source and destination "nodes" (e.g., IP addresses or MAC addresses)
     - The upper-layer protocol (see below) that will handle the packet
   - The body/payload, which is the actual upper-layer information
   - A "checksum" for verification (usually in the "trailer")
2. Computer B receives it and follows the protocols, which can vary wildly:
   - It'll run the checksum to see if it's still good data, with further rules depending on the protocol if it's bad data.
   - For many protocols, send back information to Computer A specifying that it received the information.
   - Computer B takes the payload data and passes it on through another protocol, following *those* instructions.
3. Repeat dozens, hundreds, maybe thousands or millions of times until all the data is transferred something stops it.

This system is very reliable, though it's ridiculously complex. To keep everything straight, most networking uses sub-standards under the [IEEE 802 committee](https://en.wikipedia.org/wiki/IEEE_802). The entire process "encapsulates" data to go out, then "de-encapsulates" data that comes in.

To ease with this complexity, engineers use an informal Open Standard Interface (OSI) 7-layer model (covered in a two-part [RFC 1122](https://datatracker.ietf.org/doc/html/rfc1122) and [RFC 1123](https://datatracker.ietf.org/doc/html/rfc1123)). It's not an exact science, and anyone can break these rules any way they want, but it adds some order to an insanely elaborate situation.

The layers, in order:

1. Physical - basically cables and hardware
2. Data Link - manages the quality and flow of the data itself, irrespective of *what* that data is
3. Network - directs the data across a large-scale network using IP addresses
4. Transport - manages the quality and flow of information on the network
5. Session - establishes and manages each stream of information from/to applications
6. Presentation - converts the data for sending or presenting
7. Application - the application stores/retrieves the data

It's worth committing the 7 layers to memory in tech because it gives a map to how things could possibly fail. For example, if a computer isn't accessing the internet but it's "pinging" fine, then it has no problems on the network layer downward and you won't have to check for broken cables.

A few good mnemonics for the OSI model:

- Please Do Not Throw Sausage Pizza Away
- All People Seem To Need Data Processing

Since the OSI model didn't think about the internet, the TCP/IP model is 5 layers, with the Session and Presentation model rolled together as part of the Application model.

As the protocols get more complex up the chain, the data gets bigger. Each of the layers uses a different "protocol data unit" (PDU) to specify how large a chunk of information that it's working with.

## Layer 1: physical

The PDU on the physical layer a bit-by-bit perspective: one 0 or 1 at a time.

Most of the physical layer involves understanding cabling, connectors, and [wireless signals](radio.md).

It's worth noting here that I'm stripping away a *lot* of extra information, most of it being trivia about network standards. There are dozens of certifications and hundreds of textbooks on the subject. If you're curious, [look here](https://en.wikipedia.org/wiki/Category:Networking_standards).

- Coaxial - copper cable on an axis (hence, co"axi"al) surrounded by insulation, surrounded by braiding, surrounded by a sheath.
  - Often uses an RG rating (e.g., RG-6 for old TVs), which stands for Radio Guide because they usually use radio frequencies to send the signal over copper.
  - Can have one core with a fat strand of copper, or be multi-core with many thin strands.
  - While they're largely obsolete for home use, they still have functionality when you want to send information across comparatively long distances.
- Twisted pair - tiny copper wires (usually 8) twisted into pairs, surrounded by a sheath, can be unshielded or shielded.
  - Shielded twisted pair (STP) prevents electromagnetic interference, but is more expensive than unshielded twisted pair (UTP)
  - There are currently 7 major "Categories" of twisted pair cables with "Cat 5e" being the standard as I'm writing this.
  - RJ11 is the standard old-timey telephone cable and only has 4 wires, RJ45 is what everyone thinks of when they say "ethernet cable". Ethernet has been a prevalent standard since the 1970s, mostly because they [publicly released their standards](legal-ip-floss.md) to the [IEEE](standards-computers.md).
- Fiber optic - slightly flexible glass tubes that are about the size of a human hair, surrounded by a reflective cladding, surrounded by protective Kevlar, surrounded by a sheath.
  - Instead of electricity, fiber optics send infrared light (850, 1300, or 1550 nanometers, compared to visible light being ~300-750 nanometers). They can send one beam of light (single-mode fiber, or SMF) or multiple beams of light at once (multimode fiber, or MMF).
  - Generally, SMF is more useful for long distances because the light won't fade as fast.
- WiFi - local radio wave transmission, uses [802.11 standard](standards-computers.md).
  - New standards are rolling out all the time, including (in relative chronological/quality order) a, b, g, n, ac, and ax
  - The older standard runs on the 2.4 GHz band and is divided into either 11 or 14 "channels" depending on the country, but the newer 5 GHz band has dozens to accommodate its popularity.
    - 11 channels is a bit misleading, since channels tend to bleed into each other. In practice, only channels 1, 6, and 11 don't bleed into other channels!
  - It's worth noting that the popular Bluetooth standard uses the *exact same* 2.4 GHz frequency as WiFi, though it's not used for networking.
  - The 5 GHz band also has wide channels, where it can stick multiple parallel channels together if nothing else is in the way, which can dramatically speed up data transfer.
- Cellular data - long-distance [radio wave](radio.md) transmission.
  - 3G, 4G, 4G LTE, 5G, and so on.
  - The signals connect via a "cellular network" of towers:
    1. The mobile device connects to a local "cell" tower by sending a signal.
    2. The cell tower connects, then sends [location information](logistics-navigation.md) about the towers next in range.
    3. Beyond other data uses (e.g., a phone call), the cell tower doesn't update any new information.
    4. When the mobile device gets near the perimeter, it sends a coded signal for the new cell tower.
    5. Return to #2, repeat as necessary.
  - There are "mobile network operators" (MNOs) who manage the towers, and they will rent out the extra bandwidth out to "mobile variable network operators" (MVNOs), which is how you can get super-cheap phone plans that don't always work during peak hours.

Signals are *not* completely reliable:

- Over distance and with interference, the signal will "attenuate".
- Also, over long distances the signal will have a "latency" to it, especially when it's bouncing through many routers (such as the internet).
- And, because of strange and unpredictable interference, signals will often have "jitter" that makes the latency and attenuation wobble around.
- Because of how cheap UTP cables are and how convenient WiFi is, *nearly everything* in a nearby network will suffer from "crosstalk".

By far, jitter is the worst type of network issue because it's often hard to pinpoint exactly what causes it.

If the signal is relatively slow, it's usually because it's either traveling through a bad connection or because one of the connectors is slow. It's not hard to understand, but it's amazing how some people don't realize a 10-gigabit/second SFP connection that's connected later on the network to a 1-gigabit/second Cat 5e cable will travel at 1-gigabit/second.

There's an invisible line called a demarc that separates the customer's and the service provider's cabling. It determines who manages and pays if something breaks. The demarc gets more complicated when the customer uses the service provider's hardware (e.g., cable modem or router).

Network technicians are typically savvy in cutting and crimping cables, and it's not uncommon for them to have huge spools of cable with a pile of tips in their vans alongside a wide variety of testing equipment.

Every device has a 36-character "universally unique identifier" (UUID) or "globally unique identifier" (GUID) that's unique to each part. The different versions of UUID all have different conventions to make it unique, but it's used to clarify differences and it's insanely unlikely any 2 network devices will have the same one.

Internet service providers (e.g., AT&T, Verizon, TimeWarner) define hard limits on how much download/upload ("bandwidth") consumers can use. Because they can cut down on service costs and make more money, most providers sell an asymmetric bandwidth allocation that favors downloading to most consumers: uploading large files will take a long time, but downloading them (such as online videos) is relatively fast.

## Layer 2: data link

Sometimes the Data Link layer is called "link-level". It concerns itself mostly with whether data is reliably making it across the network. Most of the action in Layer 2 is in network interface cards (NICs) and switches/hubs.

At one time, "hubs" were the best way to send network information: simply make a device that was effectively a "repeater" for any information that went through it. This meant that *all* the computers got the information and the other computers received it and discarded it.

To speed up networks by avoiding all that useless data transfer, engineers designed the "switch", which is directing the data only to where it's supposed to go using a variety of [multiplexing protocols](computers-alu.md). One of those protocols is the "spanning tree protocol" (STP)

Wireless networks add a few complications:

1. [Wireless technologies](radio.md) are extremely volatile, and seemingly unrelated things can disrupt wireless signals. So, while they're merely a matter of activating hardware to set up (as opposed to running cables), they're a headache to troubleshoot.
2. Most of the [cybersecurity concerns](computers-cysec.md) with wireless networks comes from the physics-based reality that a WiFi signal can only exist as a network hub.

Unlike the other 6 layers, Layer 2 has two sub-layers:

1. MAC - media access control, which clarifies what device is being used.
   - The "MAC addresses" are built onto NICs by manufacturers, who have to request a block of them from the [IEEE](standards-computers.md).
   - MAC addresses are assigned during manufacturing and can't be changed (theoretically).
   - Network switches keep track of all the MAC addresses.
2. LLC - logical link control, which handles where things go and how fast.
   - It uses MAC information and routing instructions.
   - LLC also manages the timing of how long a computer is permitted to send information continuously.

MAC address FF:FF:FF:FF:FF:FF is the Layer 2 "broadcast address", which means *every* NIC on that network will process that frame.

The Data Link layer's PDUs are called "frames", and each has their own subsections:

1. Preamble, a 7-byte series of alternating 1s and 0s (101010...) and then a "start frame delimiter" that demarcates the start of the frame.
2. Header, which has MAC addresses and source/destination nodes.
3. Body, which has the actual data getting transmitted.
4. Trailer, which includes "error-correcting code" (ECC) known as a "frame check sequence" (FCS) that often includes a "cyclic redundancy check" (CRC).

The math for calculating CRC is challenging, but it allows an FCS that's only 4 bytes to accurately verify up to 1,500 bytes of data!

There's a maximum transmission unit (MTU) size that determines how big frames can get, but if you have a situation like [virtualization](computers-distsys-vm.md) where there's technically nothing long-distance, you can use what's called "jumbo frames" to speed everything up.

Most of the issues on the Data Link layer and higher are tied to "frame collisions", where two computers are sending information at the exact same time along the exact same cable to a third computer. Both computers are *supposed* to stop, wait a random time, then try again, with the longer-time computer waiting to use that cable after the first one is finished.

There have been different ways to fix frame collisions before switches:

- Token Ring was popular for a while by using a 3-byte "token" that passed around a ring.
- Carrier sense multiple access with collision detection/avoidance (CSMA/CD / CSMA/CA) is a system within the Ethernet [protocol](standards-computers.md) that either detects a frame collision or prevents it beforehand.
  - The original collision detection was a cleverly simple system pulling from [ALOHAnet](https://en.wikipedia.org/wiki/ALOHAnet): if it detected a collision, it would randomly time the re-send to try again.
  - It worked perfectly because all the network modems likely used the same timing for subsequent packet intervals, so the transfer only collided the first time around.

But, now with switches, a frame collision is usually caused by a bad switch.

## Layer 3: network

The Network layer manages interaction across multiple networks, and concerns itself with whether data can make it between 2 points on any given network(s).

The PDU of the Network layer is called a "packet", though it can become confusing because some Layer 4 PDUs are also packets.

Most of Layer 3 uses routers, which are serving a bit like switches but across multiple networks. Since most network boxes are serving both as a switch and a router, they're often called "router switches".

While Layer 2 uses MAC addresses, Layer 3 uses IP (internet protocol) addresses. "Address resolution protocol" (ARP) is the routing protocol that links MAC and IP addresses together.

IP addresses have an amusing story behind them:

1. IPv4 was the standard for a long time (e.g., 192.168.0.1). It used 32 [bits](computers-alu.md): four octets of binary information (0-255, 4 times).
2. Once they started running out of IP addresses (4,294,967,296 possible, with 588,514,304 reserved for special things), they started getting creative by using contrasting public/private IP addresses by using "subnets" (e.g., your private IP is 192.168.0.3 but your public IP is 165.25.1.65). This entire process is called "Network Address Translation" (NAT) and requires some [two-based math](logic-cs.md), as well as configuring a "gateway" that has 2 IP addresses.
3. Engineers designed IPv6, which used 128 bits (IPv5 didn't work right). This permitted 340,282,366,920,938,463,463,374,607,431,768,211,456 possible IP addresses (which, for reference, is 340,282,366,920,938 times more than the number of estimated stars in the galaxy).
   - IPv6 uses hexadecimal quartets with colons to make it readable (2607:f0d0:1002:0051:0000:0000:0000:0004), but a convention helps remove the extra zeroes (2607:f0d0:1002:51::4).
   - 64 bits are the network ID on the front, and the other 64 bits are the interface ID, which means it's obvious what's going on at a glance.
4. Selling companies on transitioning from IPv4 to IPv6 has been *very* difficult, so it creates strange bottlenecks and technical issues throughout the internet as the scarcity of IPv4 addresses keeps growing.
5. Marketers developed the "Internet of Things" (IoT) to sell IPv6 to consumers. This meant simply that all sorts of devices, from fridges to cars to slow cookers, got an IP address.
6. While there are tremendous opportunities of having special-use devices that operate as independent network assets, it created tremendous [cybersecurity risks](computers-cysec.md) as well.

On Layer 3, computers individually look at packets without any context to a broader channel of information, meaning that they're "connectionless".

Layer 3 issues are often caused by faulty hardware in the router or one of the computers (or simply a faulty configuration), as well as an incorrectly configured IP address. Because manual IP management is such a pain (especially [at scale](computers-distsys-enterprise.md)), many of these tie to automatic IP address systems like the [DHCP protocol](standards-computers.md). Even then, sometimes you *do* want a static IP address instead of DHCP.

To prevent signals from bouncing around forever in an infinite loop between 3 nodes, there's a "time to live" (TTL) that indicates how many "hops" until the signal drops. In fact, the "tracert" [CLI command](computers-cli.md) works by sending a packet with a TTL of 1 and getting a report from it, then a TTL of 2 with a report, and so on.

[Web domains](computers-webdev.md) are a key part of the internet, but they don't really "fit" into the OSI network model. However, the DNS *does* resolve domains to IP addresses, so Layer 3 is likely the best place to cram it. In fact, some of the tech-savvy internet users in the late 1980's found domains in web browsers to be *more* trouble than working with IPs.

Most issues on the Network layer and higher can be resolved with [command-line tools](computers-cli.md) like ping and trace to resolve IP issues.

## Layer 4: transport

The Transport layer expands the Network layer to include the functionality of Layer 2 (i.e., get a data connection), but spread across an entire network. This layer was meant to manage the many streams of data that came as a result of the internet, as well as resolve any issues that came from faulty packets.

Transport layer protocols are each peer-to-peer, without any awareness of the network at large. This allows the computer to only focus on the transfer of each file instead of broader issues it may not be able to do anything about. It resolves the scaling problems that come with the conventional host-centered model compared to the information-centered model of the internet.

The Transport layer's PDU has different names.

- If it's using "transmission control protocol" (TCP), it's managing "packets".
  - TCP will establish a connection and will verify all the packets were sent (a "connection-oriented protocol").
  - TCP uses what's called a "three-way handshake" to make sure both computers are talking:
    1. Computer A sends a SYN (synchronize) command to Computer B.
    2. Computer B sends back a SYN-ACK (sync-acknowledge) command back.
    3. Computer A sends back an ACK command.
- If it's using "user datagram protocol" (UDP), it's managing "datagrams".
  - A "datagram" speeds up data transfer by cutting down on data use through not asking for a reply to confirm that the information was received (a "connectionless protocol").
- In practice, the PDU is simply the same data as Layer 3, but with the option of TCP involved.

Sometimes, packets get dropped. TCP's header makes sure the packets are successfully reassembled on the other side, and will ask for any missing packets. UDP, on the other hand, is a little faster but not as reliable because it doesn't account for missing packets, which is great for specific time-sensitive things (like [streaming video or audio](standards-computers.md)).

TCP uses the slow start [algorithm](programming-algorithms.md), which is a genius and simple solution for attaining a fast connection without knowledge of how reliable the network is.

The Transport layer adds a port number. That port is 16 bits (so it ranges from 0 to 65535). There are [*many* predefined ports](https://en.wikipedia.org/wiki/List_of_TCP_and_UDP_port_numbers). When an IP address is assigned to a port, it's called a "socket".

The packets/datagrams have a ton of various information that gives lots of context (source/destination addresses near the front, ports, sequence numbers for the application to reassemble the information, URLs all over). To save processing time reading through all of it, Layer 4 headers have a summarized "name" at the beginning of it that allows the computer easy access to what it needs to know without having to sift through all the extra data.

Issues on the Transport layer can come from the firewall blocking certain ports or from Quality of Service (QoS) settings, which are router/switch features that prioritize certain traffic to make the user experience better.

## Layer 5: session

At this point, the perspective changes a bit. The first 4 layers deal with network nodes and connections, but that's not necessary on the last 3 layers. Instead, it's looking at the relationships between applications (e.g., the text message app on one phone with the text message app on another).

Computers are sending information over a block of time, which is called a "session". The session layer deals with starting, maintaining, and ending sessions. Sessions can be for a few milliseconds or months, context-depending.

There are two methods for how a computer establishes a session:

- Client and server model - The application requesting the information is called the "client" and initiates a request for information from the "host", and most of the information travels in one direction.
- Request and response model - The information travels back-and-forth constantly, with each computer asking for information and the other one responding with it or stating it doesn't have it.

[P2P](computers-distsys-torrent.md) is a relatively newer standard that involves a request and response model where *all* the computers are sending and receiving information simultaneously.

Depending on the protocol, the data will transfer differently:

- Simplex - one way only (e.g., [keyboard](computers-keyboard.md) or [screen](computers-screen.md))
- Half Duplex - one way at a time (e.g., text messaging)
- Full Duplex - both ways at the same time (e.g., a phone call)

At the Session layer, the PDU is the data that gets passed to the network. In effect, this is the lowest layer where you can be certain that you have *all* the data (though it's likely not easily viewable). The higher layers are for managing the data "locally" on both sides.

Most of the failures on the Session layer are dealing with application settings and configurations. If the other 4 layers don't apply, the best solution is to poke around inside the settings on both applications to see if it's blocking anything or mishandling the data.

## Layer 6: presentation

The Presentation layer packages the data for transfer, then unpacks it on the other side.

This mostly has to do with [character encoding](computers-keyboard.md) along with [encryption](encryption.md).

The PDU at the Presentation layer is the data formatted for delivery (if outgoing) or presentation (if incoming).

Often, the issues on the Presentation layer are tied to bad [operating system](computers-os.md) drivers or permissions issues involving the user's access level, and sometimes [malware](computers-cysec-malware.md).

## Layer 7: aplication

The Application layer is a bit of a weird catchall. It merges closely with [front-end development](computers-software-design.md), since it deals heavily with [how the user perceives the information](design-uxui.md).

There are *many* Layer 7 protocols:

- File Transfer Protocol (FTP)
- Secure Shell (SSH)
- Email protocols like Simple Mail Transfer Protocol (SMTP) and Internet Message Access Protocol (IMAP)
- Internet protocols like Domain Name Service (DNS) and Hypertext Transfer Protocol (HTTP)

The PDU at the Application layer is the data as it is inputted and outputted within the application.

Applications can be bandwidth-sensitive (e.g., a streaming movie) or elastic (e.g., email or a [web browser](/browser/)). Faster bandwidth is always better, but not always necessary.

Applications can also be loss-tolerant (e.g., a streaming video chat) or no-loss (e.g., web documents).

The purpose of these protocols is to package up information for moving to the other layers, which is why the TCP/IP model piles the top three layers together.

The line between Layer 7 and [most individual operating system elements](computers-os.md) mostly differentiates with whether data transfers from one device to another, though that can get *very* blurry due to [distributed systems](computers-distsys.md).

Most of the issues on the Application layer involve either bad configurations inside the operating system or user error. Most of these resolutions involve plenty of [customer service](customerservice.md).

## Layers implementation

In short, here's how it ends up looking with 2 computers directly linked to each other with a simple messaging app. I've included a representation as well on how that data will roughly look.

1. At Computer A's Application layer, someone types "Hi" and hits SEND.
   - (computer code that says "Hi", with the source and destination)
   - (using [this ASCII table](https://www.asciitable.com/), those letters convert to 72 and 105)
2. At Computer A's Presentation layer, the message is encoded, with a header to indicate the source and destination.
   - `[01001000 01101001](for 72 and 105)` - to make it easier, we'll call this whole thing L6 from here on out
   - (for simplicity's sake, we'll ignore [encryption](encryption.md))
3. At Computer A's Session layer, it makes a connection to the other computer and loads up the payload.
   - `[header with something that says it's text data][L6]` - we'll call this whole thing L5 now.
4. At Computer A's Transport layer, it breaks up the entire thing into sections and sends them separately.
   - `[header with source/destination IP address][L5, part 1]` = L4-1 packet
   - `[header with source/destination IP address][L5, part 2]` = L4-2 packet
   - (it can keep going, but this is a simple message so we'll stop at 2)
5. At Computer A's Network layer, each of the packages is prepped to send over the network.
   - `[header][L4-1]` = `[L3-1]`
   - `[header][L4-2]` = `[L3-2]`
   - (etc.)
   - (NOTE: Layer 3 only works 1 packet at a time)
6. At Computer A's Data Link layer, it breaks up the data further into frames and connects it to MAC addresses.
   - `[header with source/destination MAC address][L3-1, part 1]` = `[L2-1]`
   - `[header with source/destination MAC address][L3-1, part 2]` = `[L2-2]`
   - (NOTE: Layer 2 only works 1 frame at a time)
7. At the Physical layer, Computer A sends the data bit-by-bit to the Computer B.
   - 1
   - 0
   - 1
   - etc.
8. At Computer B's Data Link layer, it reassembles the information back into frames based on header information.
   - `[L2-1]` minus header
   - `[L2-2]` minus header
   - (etc.)
   - At this point, it'd send it off again via a "frame relay" if the data was traveling through a network switch/hub.
9. At Computer B's Network layer, it reassembles the frames back into packets based on header information.
   - `[L2-1] [L2-2]` minus headers = `[L3-1]`
   - `[L2-3] [L2-4]` minus headers = `[L3-2]`
   - (etc.)
   - At this point, it'd send it off again via Layers 1-2 if the data was relaying via a router.
10. At Computer B's Transport layer, it reassembles the packets together into the payload.
    - `[L3-1]` minus header = `[L4-1]`
    - `[L3-2]` minus header = `[L4-2]`
    - (etc.)
    - `[L4-1] [L4-2]` (etc.) = `[L5]`
11. At Computer B's Session layer, it keeps the stream continuously going until the data is complete.
    - SESSION OPENED -> `[L5]` -> SESSION CLOSED
12. At Computer B's Presentation layer, it converts the data into something the receiving application can use.
    - `[L5]` -> ASCII code page -> `[L6]`
13. At Computer B's Application layer, the application follows that code, which usually leads to an output.
    - `[L6]` -> "Hi"

## Layer weirdness

Because of how much TCP works with IP, the two pair into a frequently used term of TCP/IP, which makes a simpler version of the OSI layers called the Internet Protocol Suite:

- Link Layer - Layers 1-2 together
- Internet Layer - Layer 3
- Transport Layer - Layer 4
- Application Layer - Layers 5-7

For [cybersecurity reasons,](computers-cysec.md) some information must be [encrypted](encryption.md) across the internet. While this is *usually* done on Layer 3, it can also be done on Layer 2 (such as L2TP).

Further, some protocols run across *multiple* layers. [Mobile](radio.md) carrier [protocols](standards-computers.md) run across L1, L2, and L3:

- GSM - global system for mobile communications, a European standard on the 900-1800 MHz band that the whole world uses (though the US uses the 1900 MHz band which makes its phones incompatible without dual-band hardware).
- CDMA - code division multiple access, high-quality [proprietary](legal-ip-floss.md) WWII-era protocol that gives full-band data to multiple connections at once
- WOO - wireless in local loop, a LAN protocol
- GPRS - general packet radio services, the standard for 2G and 3G data services

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
2. [Enact laws to prevent their misuse](rules.md), which requires [government intervention](groupslarge.md).
3. [Maintain a competitive free market](economics.md), which requires government *non*-intervention.

## Further learning

[Practical Networking](https://www.practicalnetworking.net/)

[Hello IPv6: a minimal tutorial for IPv4 users](https://metebalci.com/blog/hello-ipv6/)

[Observing my cellphone switch towers](https://fabiensanglard.net/lte/index.html)
