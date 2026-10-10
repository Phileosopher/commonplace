
# Distributed systems explained

Beyond [cybersecurity concerns](cs-infosec-compliance.md), [management issues](mgmt-cs.md), and [enterprise-scale business approaches](cs-distsys-enterprise.md), distributed systems have other issues at scale.

## Making many computers synchronized

One of the issues is the task of making many computers work as one.

The least troublesome approach is to have a distributed set of computing resources:

1. Have at least two big computers that do the heavy lifting as distinctive nodes on a network.
2. Have a smaller computer monitor those two computers, such as an [embedded system](cs-embedded.md).
3. Get a "load balancer" that uses the system monitoring data to relay incoming requests to a free node based on the monitor's data.

Naturally, the [network](cs-networks.md) requirements can become otherworldly complicated with the extra signal processing. They often require special tools to monitor everything simply because there's no way to properly use a cable tester or toner probe.

In large implementations like industrial control systems (ICS), there are additional needs:

- Programmable logic controllers (PLCs) are necessary to regulate flow or trigger actions based on met conditions (e.g., the molten steel has reached a specific temperature).
- A supervisory control and data acquisition (SCADA) system operates as a centralized system to maanger everything.
- Frequently, the controls travel warehouse-sized distances, so they need long-distance WAN capability as well.

And, all of these things require redundancy, so double the systems just to be safe. Add some control systems to monitor the redundant systems as well.

Redundancy is a common necessity in all distributed systems, but it comes with extra things to keep in mind.

- These redundancies implement in various ways:
  - One central source for something, with multiple other systems referencing it at once (i.e., redundant requests).
  - Multiple instances of similar-enough implementations like containers or disk images (i.e., redundant design).
  - Multiple sources of similar-ish things like versions for various uses (e.g., software repositories).
- The answer to this is to interpret the paradigm of "self time" versus "common time".
  - The solo actions that have nothing else associated are, effectively, *not* networked.
  - However, anything that associates to another component that is shared needs to have multiple plans in place:
    1. What happens if the resource times out?
    2. What happens if the resource disappears or moves without a proper redirect?
    3. What happens when the resource is being used by something else?

## More information

Giant piles of things:

- [awesome-distributed-systems](https://github.com/rShetty/awesome-distributed-systems)
- [distributed-systems](https://github.com/brunohenrique/distributed-systems)
