
TeachYourselfCS:

1. Steen, Tanenbaum's Distributed Systems, 3rd Edition
    [Distributed Systems 4th edition (2023) - DISTRIBUTED-SYSTEMS.NET](https://www.distributed-systems.net/index.php/books/ds4/)
2. Distributed Systems - Steen, Maarten van (2016) (to get)
3. MIT's 6.824
4. Read papers
    [Papers](https://dsrg.pdos.csail.mit.edu/papers/)
    - Attend a local Papers We Love chapter
        [Papers We Love](https://paperswelove.org/)
        [GitHub - papers-we-love/papers-we-love: Papers from the computer science community to read and discuss.](https://github.com/papers-we-love/papers-we-love)
        Papers from the computer science community to read and discuss
        repository of academic computer science papers and a community who loves reading them.

## load balancing

A way to get quick and dirty load balancing among multiple consumer processes: the hungry consumer model. In a hungry consumer model, you replace the central scheduler with a number of independent consumer tasks and a centralized work queue. Each consumer task grabs a piece from the work queue and goes on about the business of processing it. As each task finishes its work, it goes back to the queue for some more. This way, if any particular task gets bogged down, the others can pick up the slack, and each individual component can proceed at its own pace. Each component is temporally decoupled from the others. Tip 40 Design Using Services Instead of components, we have really created services-independent, concurrent objects behind well-defined, consistent interfaces.

## NGINX

NOTE: NGINX is some sort of container that works over HTTP on Linux

## production database

Any sufficiently bad software update is indistinguishable from a cyberattack
