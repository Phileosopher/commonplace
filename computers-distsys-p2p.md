
# Peer-to-peer protocols

Before going into the technical side of it, it's worth understanding how "peer-to-peer" (P2P) [protocols](standards-computers.md) work:

- Instead of conventional networking protocols with a client/host relationship, P2P is designed where every network node is *both* a host *and* a client.
- Information disseminates across every engaged computer in that network (which very often happens to be the internet), and the only way to stop the flow of information is to take down *every* computer that has that information.
- P2P protocols typically hold an entire network together with a "magnet link", which sends out a communication to the other computers that share that magnet link. If they have the same magnet link, they'll share information.
- Magnet links can be quickly and easily converted into a [hash](encryption.md) for quickly referencing the information across the internet.

There are [many P2P protocols](https://en.wikipedia.org/wiki/List_of_P2P_protocols), but the most popular [network protocol](computers-networks.md) for P2P, by far, is the [BitTorrent protocol](computers-distsys-p2p-torrent.md).

P2P creates several legal hurdles:

1. Information on the internet easily travels across international boundaries all the time, making certain local national laws ineffective.
2. It's logistically impossible to press charges against *every* person who owns a computer on a vast network.
