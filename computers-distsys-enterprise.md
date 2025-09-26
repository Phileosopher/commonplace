
# Enterprise systems

As a natural product of [economics](economics.md), Large things cost more than small things. There are various reasons why "enterprise" computers cost more than consumer-grade computers:

- A relatively fast computer for personal use is often running at full capacity when a business is using it for something heavy (like a [website](computers-sofware-webdev.md) or hosting app data).
- Consumer computers are typically designed with the understanding that people won't use it at full capacity very frequently, though that's frequently an exception for [playing games](computers-software-gamedev.md). This means that things like heat management and more error-correcting code are *much* more important in businesses than for consumers.
- When consumer computers "crash", they'll be inconvenienced and might lose data (assuming it's not [cloud-synced](computers-distsys-cloud.md)). When business computers crash, a company will usually lose money.

Consumer computers tend to have prettier-looking cases, but are less efficient and powerful. They also easily cost 1/4 a business computer that's roughly the same specifications.

While it's technically *possible* to run everything in a business on a distributed [Raspberry Pi array](computers-embedded.md), it's typically more labor-intensive for the technicians, so it's not likely saving money in most cases.

Even in not-for-profits, the scale that most organizations need computers is so vast that "enterprise" is a broad catch-all concept.

## History

In the past, the needs for computers were far more niche. At first, every computer was so large and expensive that the only cost-effective solution was in performing extremely heavy number-crunching in the [scientific](science.md) domains.

However, over time, the business world started waking up to how they could dramatically speed up their [accounting reports](accounting.md), and computers became important in many business applications by the mid-1970s.

But, not everyone had to run a computer to run 24/7, so it made much more sense to rent out time to use the computer instead.

Since the computers were vast and had been parallel processing, it made sense to have multiple calculations from different sources happening at once. This was called "time-sharing".

Now, ever since the internet became popular in the mid-1990's, most modern large-scale computer needs are designed for the heavy data management back-end operations and front-end management of public-facing [internet websites](computers-sofware-webdev.md).

## Large Computer Cases

Server-grade computers are often meant to be more reliable, and are therefore often far pricier.

Server racks have very [industry-specific](standards-computers.md) dimensions:

- Width - 17.75 inches wide drawer, with a panel on front that's 19 inches, and inside a housing that can be up to 3 feet wide.
- Height - 1U is 1.75 inches, and a full-size rack is 48U or sometimes 42U (or, informally, a 7-foot rack), with a half-rack being 22U or 27U.
- Depth - 50 inches at the maximum, but can be as small as 0 inches. More depth means more room for cables. 29 inches is a standard size.

Each rack pulls out like a drawer, with a lid on it. That way, you can theoretically hold 48 fully separate motherboards in one rack. Of course, weight can be an issue, which is why racks come as 2-post or 4-post to accommodate affordability versus a heavier build.

Thankfully, if you're starting out, a clever [hack](hacking.md) allows you to [make one with an IKEA coffee table](https://wiki.eth0.nl/index.php/LackRack).

## Large Rooms

Large-scale servers require a *lot* of electricity to run. At the top end, it requires industrial-grade zoning privileges and a power grid that can withstand the constant voltage requirement. This is especially true for CPU-intensive work such as [cryptocurrency mining](computers-blockchain.md).

These rooms need adequate cooling, which often requires plenty of ventilation. Huge companies with data centers use warehouse-sized rooms called "colocations" or colos.

To maximize air conditioning use (and cut down on heat), the servers are arranged in a cold/hot aisle configuration:

1. Servers are placed into Row 1.
2. Other servers are placed into Row 2 behind Row 1, with the back ends (where the fans blow out heat) facing Row 1's back end, making a hot aisle between the two.
3. More servers are put into Row 3 behind Row 2, with the front ends facing Row 2's front end, making a cold aisle between the two.
4. Repeat for all servers.
5. Have fans or air conditioners blow down all the hot aisles to get rid of the hot air from the computes.

## Storage

[Cloud synchronization](computers-distsys-cloud.md) is a good idea for consumer-facing purposes, but there are many situations in "Enterprise File Sharing and Sync" (EFSS) where the data is rarely retrieved. In those situations, the "sync interval" can be every hour or even every day without any real risk.

However, the extra value and availability of that data means it *must* have at least a few more redundancies than a typical consumer "use case":

- Synchronize all the data across multiple hard drives, to avoid the chance that a hard drive fails with that critical data.
- Synchronize all the data across multiple locations, just in case a freak tornado or political insurrection destroys the data center.
- Routinely keep copies in "cold storage" off the network, just in case the servers get [hacked](hacking.md).
- If the organization is large enough, synchronize across multiple data centers across the world to increase data transfer speeds for the customers.

## Computes

Consumers tend to use computers sporadically, where they may have some heavy computations for something like a [game](computers-software-gamedev.md) or [graphics](engineering-graphics.md) development, but won't use it at least 14 hours of the day. Enterprise-grade computers are *constantly* running, especially as [a tech business grows](entrepreneur-6_scaling-cs.md).

Since enterprise computers are often multitasking, they need more "timesharing" than typical software development needs. Across multiple computes, at least one of the CPUs will end up being a "load balancer" to maintain the work across computes, and sometimes across multiple sites.

To that end, multi-core processors aren't the most cost-effective solution, since a core burning out in a 6-core processor would waste 5 cores. For that reason, an industry-standard [hack](hacking.md) is to use GPUs in an array, since they only run 1 processor thread.

For diagnostic reasons, the motherboard often integrates a "baseboard management controller" (BMC), which is basically another computer (a "subsystem") build right onto the motherboard. Then, when the processor fails, the BMC can log exactly what happened.

## Graphics

While software now makes the visual components of [graphics development](engineering-graphics.md) very easy, large-scale rendering often takes tremendous amounts of work to get correct.

For pre-rendered work (such as Pixar movies), the graphics rendering is run through nonstop compute hardware and memory for each scene. Then, each "frame" was "composited" into the final product. Because of all that processing, the heat generation is typically immense, and cooling becomes a major logistical factor.

## Networks

While [networking concepts](networks-computer.md) apply the same in both consumer and enterprise, there are some additional hurdles:

- IP addresses on a network can get complicated, so networks often need "IP address management" (IPAM) software to track them.
- Most of the updates and management of the computers will be "out-of-band" to make life easier for the people running the updates. This will require an "intelligent platform management interface" (IPMI) that tracks everything across a [distributed system](computers-distsys.md).
- Maintaining a "backbone" network that's relatively high-speed (with nothing but expensive routers in it), with the lower-speed computer connections linking to the backbone network.
- [Cybersecurity](computers-cysec-compliance.md) becomes an extremely complicated [design](engineering-design.md) issue, since there are *far* more users, both malicious and innocent. Nothing is ever *entirely* [hack-proof](hacking.md), but hiding that fact will become a full-time job in a mid-sized company. At one time, cybersecurity could make-or-break [a startup](entrepreneur-1_why.md), since software development used to require *very* [creative](mind-creativity.md) solutions.

The room with the servers is often known as the "main distribution frame", while the telecommunications room (with the network switches) may often be in *another* room called the "intermediate distribution frame".

To improve network connection across long distances, most large companies use "content delivery networks" (CDNs), which save a "cached" copy of the content for easy access for the user near the "network edge". These are particularly necessary because there's an inherent latency from long-distance that comes from the speed of light.

There are two major design philosophies for building a CDN:

1. Enter deep - pioneered by Akamai, which involves closely connecting with *thousands* of endpoints, more expensive but more reliable.
2. Bring home - a more popular approach, which connects with Internet Exchange Points (IXPs) to deliver longer-distance from more centralized locations.
3. Some hybrid of the two, which is often what large tech companies end up doing (e.g., bring home for most major metropolitan areas, but enter deep for rural communities).

To string together CDNs, mainframes often use "exchange points" to hold as middle-points between the original site and the network edge.

To load-balance, the easiest solution can be to route the end user to the nearest geographically proximate location, but that doesn't account for the number of hops or latency. Instead, it's more effective (but more to manage) to adjust based on real-time measurements.

[Cloud implementations](computers-distsys-cloud.md) are often popular now for minimizing latency from long-distance internet connections and making CDNs, and there are several tradeoffs when using them:

- [Security and compliance](computers-cysec-compliance.md) issues, which can include trust issues with [FAANG](faang.md).
- Optimizing for [UX](engineering-design.md), including making the experience as fast as possible for the user.
- Costs, where sometimes a mainframe is more expensive when it's sitting idle than simply renting out hosting from somewhere else.

## Testing

[Debugging and testing](computers-software-redesign.md) is just as applicable as with smaller software projects, but the stakes are dramatically higher if anything fails. One missed exit from a [function](computers-programming.md) can cause thousands of people to have their app crash simultaneously in a live environment, and a misplaced comma may mean deleting many clients' data. On the far end, this can lead to some *very* unpleasant [lawsuits](people-contracts.md).

To accommodate this reality, enterprise-grade projects use 3 servers:

1. Prototype server - an experimentation playground, where the developers can easily tweak, modify, and test code.
2. Test server - a close reproduction of the live environment, but with dummy [APIs](computers-software.md) for complete debugging and testing.
3. Live server - the server that users actually interact with.

Ideally, they *should* be using the same "environment", since different environments across them can make software development troublesome, especially between the test and live servers. This can mean each seemingly simple element within a smaller software can become autonomous APIs in entirely different network closets or datacenters.

## Approval

To accommodate all the changes, and the need to make sure everything runs correctly, everyone agrees to a "service-level agreement" (SLA) that conforms to a "service-level objective" (SLO).

## Failing

The trouble with maintaining three environments, though, is that the conditions for each of them might not be precisely the same. Those edge cases will make a dramatic difference if anything goes wrong.

When things *do* go wrong, panic is likely, proportionally to [what you don't understand](understanding.md). However, while your imagination may create fantastic stories of anxiety and catastrophe, the problem can usually be solved by [diligently reviewing the likely sources of the issue](fix-computers.md).

## Decentralized

While it's still not developed much, the conventional host/client relationship (i.e., big computers sending out to comparatively little consumer computers) has a different sort of protocol to contend with: [the P2P protocol](computers-distsys-torrent.md).

## Pricing

If you're managing computers, you'll have various customers. Some will want to host their low-profile project for their family and friends, while others will have profoundly large computing needs. Some will pay the same amount every month, while others will want your service as a "redundant" backup plan if theirs fails.

To specialize with different customers, set up a "dedicated" plan and a "shared" plan. The dedicated customers will have more direct access to everything, while the enthusiasts and small business owners can use the shared tier.
