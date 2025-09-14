
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

[Operating a Large, Distributed System in a Reliable Way: Practices I Learned - The Pragmatic Engineer](https://blog.pragmaticengineer.com/operating-a-high-scale-distributed-system)

[Distributed Systems Reading List | Hacker News](https://news.ycombinator.com/item?id=25327077)
[Distributed Systems Reading List](https://dancres.github.io/Pages/)

[Alpine Linux Wiki](https://wiki.alpinelinux.org/wiki/How_to_get_regular_stuff_working)
How to get regular stuff working
curl, man pages, compiling, disk mgmt, ...

[Putting Z-Library on IPFS | Hacker News](https://news.ycombinator.com/item?id=33675224)
[Putting 5,998,794 books on IPFS - Anna's Blog](https://annas-blog.org/putting-5,998,794-books-on-ipfs.html)
- the first comment lines up EVERYTHING you'd need for complete cyber redundancy

Important idea for distributed systems:
- if you do not need a particularly fast computer, have the load balancer underclock the CPU to make the computer last longer and run with less power (and therefore more affordably).

[Distributed hash table - Wikipedia](https://en.wikipedia.org/wiki/Distributed_hash_table)
- already in TT/torrent

[Seeing like a bank | Hacker News](https://news.ycombinator.com/item?id=38180477)
[Seeing like a Bank](https://www.bitsaboutmoney.com/archive/seeing-like-a-bank/)
- will probably go to Mgmt pages as well, probably in Communication

[Caitie McCaffrey](https://queue.acm.org/detail.cfm?id=2889274)
(2016) The Verification of a Distributed System
A practitioner's guide to increasing confidence in system correctness

[Ask HN: Do you find working on large distributed systems exhausting? | Hacker News](https://news.ycombinator.com/item?id=30396454)

[Distributed Systems Shibboleths | Hacker News](https://news.ycombinator.com/item?id=31217802)
[Distributed Systems Shibboleths | Joey Lynch's Site](https://jolynch.github.io/posts/distsys_shibboleths/)

## architectures

the design across the various systems is either client-server, or peer-to-peer
- will it have a fixed IP address?

## design patterns

[terminology - What is a Shim? - Stack Overflow](https://stackoverflow.com/questions/2116142/what-is-a-shim)
- shims are design patterns, which can be licensed software designs in their own right
- Gang of Four text, w/ 3 well-established design patterns:
[Design Patterns - Wikipedia](https://en.wikipedia.org/wiki/Design_Patterns)
- it's a way to protect against legal liability

[GitHub - google/eng-practices: Google's Engineering Practices documentation](https://github.com/google/eng-practices)

## enterprise software

Large-scale [enterprise-grade](https://trendless.tech/enterprise/) software must be maintained by [large-scale entities](https://gainedin.site/groups-large/), so their service is counter-intuitively _more_ likely to fall apart if they don't provide [an open-source implementation](https://trendless.tech/floss/).

## load balancing

A way to get quick and dirty load balancing among multiple consumer processes: the hungry consumer model. In a hungry consumer model, you replace the central scheduler with a number of independent consumer tasks and a centralized work queue. Each consumer task grabs a piece from the work queue and goes on about the business of processing it. As each task finishes its work, it goes back to the queue for some more. This way, if any particular task gets bogged down, the others can pick up the slack, and each individual component can proceed at its own pace. Each component is temporally decoupled from the others. Tip 40 Design Using Services Instead of components, we have really created services-independent, concurrent objects behind well-defined, consistent interfaces.

## NGINX

NOTE: NGINX is some sort of container that works over HTTP on Linux

## production database

Any sufficiently bad software update is indistinguishable from a cyberattack

## self-hosting

[potatoqualitee/eol-dr: A crowd-sourced guide to help techs help their non-tech spouses/partners/parents/kids when we are at the end-of-life](https://github.com/potatoqualitee/eol-dr)
- consider your succession plan!

[Self Hosting a Google Maps Alternative with OpenStreetMap | Hacker News](https://news.ycombinator.com/item?id=33704801)
[Self Hosting a Google Maps Alternative with OpenStreetMap](https://wcedmisten.fyi/post/self-hosting-osm/)
- may consider DOING this one?

## Ansible

[Ansible is Simple IT Automation](https://www.ansible.com/)

[Ansible](https://www.ansible.com/blog)
Ansible Blog

[Joseph Kahn](https://blog.josephkahn.io/articles/ansible/)
Ansible or: How I Learned to Stop Wasting Time Setting Up My Computer and Script It

[Joseph Kahn](https://blog.josephkahn.io/articles/ansible-modules/)
For a Few Ansible Modules More

[Michel Blanc](https://leucos.github.io/articles/ansible-contract-inventory/)
Making dynamic inventory usable with Ansible and Digital Ocean

[Corban Raun](https://blog.serverdensity.com/what-ive-learnt-from-using-ansible-exclusively-for-2-years/)
Lessons from using Ansible exclusively for 2 years.

[Bjoern Meier](http://reinout.vanrees.org/weblog/2017/10/26/6-ansible.html)
(2017) PyCon.de: use ansible properly or stick to your scripts.
[Slides in PDF](https://github.com/blue-yonder/documents/blob/master/presentations/PyCon.DE%202017/No_Compromise-Use_Ansible_properly%20_or_stick_to_your_scripts.pdf)

[Will Thames](http://willthames.github.io/2017/10/31/making-the-most-of-inventory.html)
(2017) Making The Most Of Inventory

[Greg DeKoenigsberg](https://www.ansible.com/blog/2017-community-year-in-review)
(2018) Take a look back at 2017 with Ansible's community review.

[/r/devops](https://www.reddit.com/r/devops/comments/629dj3/jenkinsansible_vs_jenkinsansibleansible_tower/)
Jenkins+Ansible vs Jenkins+Ansible+Ansible Tower

[Ansible](https://www.ansible.com/resources/videos/ansiblefest-london-2017)
(2017) AnsibleFest London Videos

[Matt Jaynes](https://hvops.com/articles/ansible-vs-shell-scripts/)
(2019) Shell Scripts vs Ansible: Fight!

[AnsibleFest](https://www.ansible.com/ansiblefest)
brings together Ansible users, developers and industry partners to share best practices, case studies and Ansible news.

## Ansible+Openshift

[Ansible Docs](https://docs.ansible.com/ansible-container/openshift/minishift.html)
Minishift role for Ansible

## Ansible - testing and debugging

[Ross Tuck](http://rosstuck.com/slightly-faster-ansible-testing-with-vagrant)
(Slightly) Faster Ansible Testing with Vagrant

[Dan Tehranian](https://dantehranian.wordpress.com/2015/06/18/testing-ansible-roles-with-test-kitchen/)
(2015) Testing Ansible Roles with Test Kitchen

[Will Thames](http://willthames.github.io/2014/04/28/debugging-ansible-for-fun-and-no-profit.html)
(2014) Debugging Ansible for fun and no profit

## Ansible Vault

[Chris Short](https://opensource.com/article/16/12/devops-security-ansible-vault)
Improve your DevOps security game with Ansible Vault

[Michel Blanc](https://leucos.github.io/articles/transparent-vault-revisited/)
Transparent encryption with ansible vault revisited

## Ansible vs Chef

[Bryan Friedman](https://content.pivotal.io/pivotal-blog/comparing-bosh-ansible-chef-part-1)
(2017) Infrastructure as Code is Not Enough: Comparing BOSH, Ansible, and Chef - Part 1.
[Part 2](https://content.pivotal.io/blog/comparing-bosh-ansible-chef-part-2)

## Ansible vs Puppet

[Dan Tehranian](https://dantehranian.wordpress.com/2015/01/20/ansible-vs-puppet-hands-on-with-ansible/)
(2015) Ansible vs Puppet – Hands-On with Ansible

## authentication

[Daniel Miessler](https://danielmiessler.com/blog/the-connected-web-why-its-time-for-strong-authentication/)
The Connected Web: Why It’s Time For Strong Authentication

[Biarity](https://biarity.gitlab.io/2018/02/23/passwordless/)
(2018) An argument for passwordless
consider alternatives to password authentication

[Getting my library cards onto my phone the hard way | Hacker News](https://news.ycombinator.com/item?id=38050535)
[Getting my library cards onto my phone the hard way - iliana.fyi](https://iliana.fyi/blog/ios-wallet-library-card/)

## authentication software - OAuth

[Why is OAuth still hard in 2023? | Hacker News](https://news.ycombinator.com/item?id=35713518)
[Why is OAuth still hard in 2023? | Nango Blog](https://www.nango.dev/blog/why-is-oauth-still-hard)

## billing systems

[Pains of building your own billing system | Hacker News](https://news.ycombinator.com/item?id=39510147)
[🦑 The 14 pains of building your own billing system - Arnon Shimoni](https://arnon.dk/the-14-pains-of-billing/)

## bi tool

[Self-Serve Dashboards | Hacker News](https://news.ycombinator.com/item?id=40646312)
[Self-serve dashboards | Briefer](https://briefer.cloud/blog/posts/self-serve-bi-myth/)

## branch by abstraction

[Jez Humble](https://continuousdelivery.com/2011/05/make-large-scale-changes-incrementally-with-branch-by-abstraction/)
(2011) Make Large Scale Changes Incrementally with Branch By Abstraction

## build systems

[Electric Cloud](http://electric-cloud.com/plugins/build-automation/)
Build Automation: Top 3 Problems and How to Solve Them

[Phillip Holmes](http://doatt.com/2015/02/02/fourth-the-build-system/index.html)
(2015) Fourth - The Build System

[Phillip Holmes](http://doatt.com/2015/04/27/the-build-methodology-decision/index.html)
(2015) The Build Methodology Decision

[Nicolas De Nayer](https://medium.com/doctolib-engineering/the-duty-guy-the-key-to-empowering-engineers-a43d1fc4706b)
(2017) The Duty Guy: the key to empowering engineers

[Nathan Hurst](http://engineering.teacherspayteachers.com/2015/12/01/from-10-hours-to-10-minutes-scaling-release-automation-at-teachers-pay-teachers.html)
(2015) From 10 Hours to 10 Minutes: Scaling Release Automation at Teachers Pay Teachers

[Theo Schlossnagle](https://omniti.com/seeds/online-application-deployment-reducing-risk)
(2010) Online Application Deployment: Reducing Risk

[Cyriac Thomas](https://www.compile.com/blog/product/be-lazy-build-better-systems/)
Be lazy, build better systems

## c4 model

[Simon Brown](http://www.codingthearchitecture.com/2014/08/24/c4_model_poster.html)
(2014) Software architecture and the C4 model
context, container, component, class diagrams

## CDNs

[Please stop using CDNs for external JavaScript libraries | Hacker News](https://news.ycombinator.com/item?id=24745194)
[Please stop using CDNs for external Javascript libraries - Terence Eden's Blog](https://shkspr.mobi/blog/2020/10/please-stop-using-cdns-for-external-javascript-libraries/)

[Writing a Mini-CDN to Learn Nginx/Prometheus/Grafana/Lua | Hacker News](https://news.ycombinator.com/item?id=34137065)
[GitHub - leandromoreira/cdn-up-and-running: CDN Up and Running - Building a CDN from Scratch to Learn about CDN, Nginx, Lua, Prometheus, Grafana, Load balancing, and Containers.](https://github.com/leandromoreira/cdn-up-and-running)

[Jim Nielsen on Twitter: "Why choose a JS CDN when you can let them compete for your love and affection? First one that resolves wins. Ready? Go! const MyModule = await Promise.any([ import("unpkg/...") import("cdnjs.cloudflare/...") import("cdn.jsdelivr/...") import("cdn.skypack/...") ]);"/Twitter](https://twitter.com/jimniels/status/1539976086645268480)

## checklists

[Viss: "food for thought: zero commer…" - Mastodon](https://mastodon.social/@Viss/112176699070565675)

## Chef

[Michael Hedgpeth](https://blog.chef.io/2017/04/13/guest-post-why-habitat/)
(2017) Why Habitat? - Chef Blog

## ci-cd

[Container Journal](https://containerjournal.com/2017/10/17/using-cicd-containerization-drive-pre-production-costs/)
(2017) Using CI/CD Over Containerization to Drive Down Pre-Production Costs

[Eric Myhre](https://gist.github.com/warpfork/0ad12d99d2b4de32412f7f294c23fde5)
You probably don't really want CI-triggered CD

[DevOpsGuys](https://www.devopsguys.com/2013/02/06/maturing-the-continuous-delivery-pipeline/)
(2013) Maturing the Continuous Delivery Pipeline

[Didier Caroff](https://medium.com/devopslinks/how-we-switch-to-a-continuous-delivery-pipeline-in-3-months-9667b9f65f7a)
(2018) How We Switched to a Continuous Delivery Pipeline in 3 months

[Don Macvittie](https://devops.com/moving-big-project-cicd/)
Moving That Big Project to CI/CD

[Jan Krag](https://www.praqma.com/stories/survival-of-the-fittest/)
(2017) Survival of the Fittest; Evolution in the CI ecosystem

[Samuele Resca](https://dev.to/samueleresca/continuos-delivery-using-feature-toggle)
Continuous Delivery using feature toggle

[topics/awesome-ci](https://github.com/topics/awesome-ci)
GitHub repositories matching awesome-ci topic

[Balaji Vajjala](http://bvajjala.github.io/blog/2014/05/07/6-challenges-in-implementing-enterprise-continuous-delivery/)
(2014) 6 Challenges in implementing Enterprise Continuous Delivery

[DevOps.com](https://devops.com/7-best-practices-continuous-delivery-success/)
(2016) 7 Best Practices for Continuous Delivery Success

[Naresh Jain](https://www.industriallogic.com/blog/impact-of-continuous-integration-on-team-culture/)
(2011) Impact of Continuous Integration on Team Culture

[Continuous Delivery](https://continuousdelivery.com/)
What is / Why Continuous Delivery ?

[James Shore](http://www.jamesshore.com/Blog/Continuous-Integration-is-an-Attitude.html)
(2005) Continuous Integration is an Attitude, Not a Tool

[James Shore](http://www.jamesshore.com/Blog/Continuous-Integration-on-a-Dollar-a-Day.html)
(2006) Continuous Integration on a Dollar a Day

[Yegor Bugayenko](https://devops.com/continuous-integration-doesnt-work/)
(2014) Why Continuous Integration Doesn’t Work
Don't forget it's Yegor writing this... :-)

[CI/CD Life](http://cicd.life/)
Continuous Integration / Continuous Delivery 4 Life - tips & tricks

[Martin Fowler](https://www.martinfowler.com/articles/continuousIntegration.html)
(2006) Continuous Integration

[Electric Cloud](http://electric-cloud.com/plugins/continuous-integration/)
Continuous Integration Best Practices: Vision and Reality
Are you really practicing the principles of Continuous Integration?

[Balaji Vajjala](http://bvajjala.github.io/projects/cd/continuous-delivery-patterns-and-antipatterns/)
(2017) continuous delivery patterns & antipatterns

[Joshua Kerievsky](https://www.industriallogic.com/blog/benefits-continuous-deployment/)
(2014) Benefits of Continuous Deployment : Lower Stress, Greater Flow, Less WIP, Easier Recovery

[Mark Seemann](http://blog.ploeh.dk/2013/12/10/semantic-versioning-with-continuous-deployment/)
(2013) Semantic Versioning with Continuous Deployment
Versioning is a programmer decision

[Nathen Harvey](https://speakerdeck.com/nathenharvey/the-journey-to-continuous-automation)
(2017) The Journey to Continuous Automation

[Steve Ropa](https://about.gitlab.com/2018/01/17/craftsman-looks-at-continuous-integration/)
(2018) A Craftsman looks at continuous integration

[Derek Greer](http://aspiringcraftsman.com/2016/02/28/separation-of-concerns-application-builds-continuous-integration/)
(2016) Separation of Concerns: Application Builds & Continuous Integration

[Eero Laukkanena & Juha Itkonena & Casper Lassenius](https://www.sciencedirect.com/science/article/pii/S0950584916302324)
(2015) Problems, causes and solutions when adopting continuous delivery - A systematic literature review
> When adopting continuous delivery, problems related to system design are common, critical and little studied. The found problems, causes and solutions can be used to solve problems when adopting continuous delivery in practice.

[Dave Farley](http://www.davefarley.net/?p=247)
(2018) Continuous Integration and Feature Branching
> * TLDR; Any form of branching is antithetical to Continuous Integration.

[Continuous Delivery Service (CDS)](https://ovh.github.io/cds/)
Enterprise-Grade Continuous Delivery & DevOps Automation Open Source Platform, by OVH. CDS is open-source and completely free.

[/r/cicd](https://www.reddit.com/r/cicd/)
Everything CI/CD on reddit

[Suzie Prince](https://www.gocd.org/2017/05/16/its-not-CI-its-CI-theatre/)
(2017) It's not CI, it's just CI Theatre

[We built the fastest CI and it failed | Hacker News](https://news.ycombinator.com/item?id=37481513)
[We built the fastest CI in the world. It failed. Here's what we learned - Earthly Blog](https://earthly.dev/blog/shutting-down-earthly-ci/)

## ci-cd - java

[Dustin Barnes](https://dev9.com/blog-posts/2014/9/java-release-process-with-continuous-delivery)
(2014) Java Release Process with Continuous Delivery
maven-release-plugin sucks

## colocation

[Angie Jones](https://techbeacon.com/6-reasons-co-locate-your-app-automation-code)
(2018) 6 reasons to co-locate your app and automation code

## complex systems

[How Complex Systems Fail (1998) | Hacker News](https://news.ycombinator.com/item?id=25550685)
[How Complex Systems Fail](https://how.complexsystems.fail/)

## datacenter infrastructure management

[Shouting in the Datacenter (2008) [video] | Hacker News](https://news.ycombinator.com/item?id=32513240)
[Shouting in the Datacenter - YouTube](https://www.youtube.com/watch?v=tDacjrSCeq4)
[Unusual Disk Latency](https://www.brendangregg.com/blog/2008-12-31/unusual-disk-latency.html)
[Brendan at Intel.com | Hacker News](https://news.ycombinator.com/item?id=31236157)
[Brendan@Intel.com](https://www.brendangregg.com/blog/2022-05-02/brendan-at-intel.html)

## data-oriented design

[Data-Oriented Design (2018) | Hacker News](https://news.ycombinator.com/item?id=36571110)
[Data-Oriented Design](https://www.dataorienteddesign.com/dodbook/dodmain.html)

## decentralized - freenode

[Leaving Freenode for a new network | Hacker News](https://news.ycombinator.com/item?id=27207440)
[freenode now belongs to Andrew Lee, and I'm leaving for a new network.](https://www.kline.sh/)

## decentralized

[Todd Hoff](http://highscalability.com/blog/2018/8/22/what-do-you-believe-now-that-you-didnt-five-years-ago-centra.html)
(2018) What Do You Believe Now That You Didn't Five Years Ago? Centralized Wins. Decentralized Loses.

[Noé Baylac Jacqué aka Deluvi](https://deluvi.com/blog/webmention/)
(2018) Implementing Webmention on a static website
An explanation of Webmentions and an implementation on Hugo
> Webmention is a web standard that allows having interactions in a decentralized way.
> The big advantage of Webmention is that the protocol is very simple: it only relies on an HTTP POST request.

[Let's Decentralize](https://letsdecentralize.org/)
[Let's Decentralize](http://xanthexikes7btjqlkakrxjf546rze2n4ftnqzth6qk52jdgrf6jwpqd.onion/)

[Spritely Networked Communities Institute -- Spritely Institute](https://spritely.institute/)
[Spritely](https://spritelyproject.org)

[elRepo.io | AlterMundi](https://elrepo.io/)

[Decentralized Internet for a Free Future | Skynet Labs](https://skynetlabs.com)
[Startup Behind Siacoin Storage Platform Raises $3M, Rebrands as Skynet Labs - CoinDesk](https://www.coindesk.com/business/2020/09/22/startup-behind-siacoin-storage-platform-raises-3m-rebrands-as-skynet-labs)

[urbit.org](https://urbit.org/)

## deployments - legacy code

[Matt Fletcher](https://spin.atomicobject.com/2018/01/22/archive-software-project/)
(2018) Today’s Code Is Tomorrow’s Legacy Project – Make It Easy to Resurrect

## deployments

[Michal Charemza](https://charemza.name/blog/posts/devops/aws/non-atomic-deployments/)
(2017) Non atomic deployments
Cron-free deferred delete of obsolete static resources
The best infrastructure is the one that doesn't exist

[Stephen Mann](https://stephenmann.io/post/dont-do-this-in-production/)
(2018) Don't Do This in Production

[Cody Boggs](https://sysdig.com/blog/deploying-private-paas-good-meh-aw-crap/)
(2016) Deploying a private PaaS: The good, the meh, and the aw crap
> "moving to a PaaS is certainly not a decision to be made lightly – but it’s still probably the right decision."

[Rachel Andrew](https://24ways.org/2014/developing-robust-deployment-procedures/)
(2014) Developing Robust Deployment Procedures

[Nathen Harvey](https://speakerdeck.com/nathenharvey/compliance-as-code)
(2017) Compliance as Code

[Cloud Custodian Docs](https://cloudcustodian.io/docs/deployment.html#compliance-as-code)
Compliance as Code
Custodian is a tool for managing cloud environments by ensuring compliance to security policies, tag policies, garbage collection of unused resources, and cost management from a single tool.

[DigitalOcean](https://www.digitalocean.com/community/questions/what-do-you-do-with-your-first-five-minutes-on-a-new-server)
What do you do with your first five minutes on a new server?

[Dan McKinley](https://blog.skyliner.io/no-way-out-but-through-1db41c648697)
(2016) No Way Out But Through
how Skyliner deploys applications and why they built it like that

[Zach Holman](https://zachholman.com/posts/deploying-software)
(2018) How to Deploy Software
Make your team’s deploys as boring as hell and stop stressing about it.

## deployments - reversing direction

[Dan McKinley](https://blog.skyliner.io/you-cant-have-a-rollback-button-83e914f420d9)
(2017) You Can’t Have a Rollback Button
The internet is a big truck. It’s really hard to drive it backwards.

## devops

[Dmitriy Samovskiy](http://www.somic.org/2016/04/12/rise-of-new-operations/)
(2016) The Rise of New Operations

[Gruntwork](https://gruntwork.io/devops-resources/)
A collection of blog posts, talks, books, and checklists for learning about DevOps, AWS, Terraform, Docker, Packer, and more

[Anonymous DevOps Confessions](https://totalcloud.io/DevOpsConfessions.html)
regrets and confessions of DevOps felows

[Tony Bradley](https://devops.com/devops-just-automation/)
(2017) DevOps is More Than Just Automation

[Christoph Görn](http://rhelblog.redhat.com/2016/10/03/peace-in-our-time/)
(2016) Peace in Our Time: Bringing Ops and Dev Together

[Pete Cheslock](https://blog.threatstack.com/how-to-create-a-security-minded-devops-organization-three-best-practices)
How to Create a Security-Minded DevOps Organization: Three Best Practices

[Jeff Knupp](https://jeffknupp.com/blog/2014/04/15/how-devops-is-killing-the-developer/)
(2014) How 'DevOps' is Killing the Developer

[Jessie Frazelle](https://blog.jessfraz.com/)
articles about DevOps, Containers, Linux, etc

[Stackify](https://stackify.com/content/DevOps/)
all posts tagged as DevOps

[Chris Short](https://opensource.com/open-organization/17/5/5-devops-laws)
5 laws every aspiring DevOps engineer should know

[Michael Cote](http://www.theregister.co.uk/2018/02/06/devops_no_ops_less_ops/)
(2018) The many-faced god of operational excellence, DevOps and now 'site reliability engineering'

[Esther Schindler](https://blog.newrelic.com/2016/04/11/devs-ops-wishlist/)
(2016) 3 Way Ops Can Help Devs: A Developer Perspective

[Esther Schindler](https://blog.newrelic.com/2016/04/26/ops-dev-wishlist/)
(2016) 3 Ways Devs Can Help Ops: An Operations Perspective

[Travis Greene](https://techbeacon.com/7-arguments-against-noops)
(2018) 7 arguments against NoOps
just say no

[Vladimir Fedak](https://hackernoon.com/10-disruptive-devops-trends-of-2018-b0b6d5719376)
(2018) 10 disruptive DevOps trends of 2018

[Devops Weekly](https://www.devopsweekly.com/)
A weekly slice of devops news

[DevOps Newsletters](https://devopsnewsletters.com/)
a one stop shop for the best DevOps news content from around the world.

[Ted Dziuba](http://widgetsandshit.com/teddziuba/2011/03/devops-scam.html)
(2011) Devops Is a Poorly Executed Scam
> You need to change the culture the hard way, or replace people as necessary until the culture works.

[Andrew Hatch](https://medium.com/seek-blog/platform-engineering-why-we-dont-need-a-devops-team-e88c8b97cc4f)
(2017) Why We Don’t Need a DevOps Team
Rename your DevOps Team

[Joe McKendrick](http://www.zdnet.com/article/time-to-move-on-from-devops-and-continuous-delivery-says-google-executive/)
(2017) Time to move on from DevOps and continuous delivery, says Google advocate

[Mike Bursell](https://opensource.com/article/18/2/most-important-issue-devops-transformation)
(2018) Tackling the most important issue in a DevOps transformation
Why culture is the most important issue in a DevOps transformation

[Eser Gozcu](https://hackernoon.com/devops-behind-scenes-817d586a1548)
(2018) DevOps and Behind the Scenes
BEST EFFORT != BEST PRACTICE
DevOps starts with a real communication. Moving towards a common goal requires social engineering

[Josh Johnson](https://lionfacelemonface.wordpress.com/2015/03/08/devops-is-bullshit-why-one-programmer-doesnt-do-it-anymore/)
(2015) DevOps Is Bullshit: Why One Programmer Doesn’t Do It Anymore

[Derek Weeks](http://blog.sonatype.com/embedding-ownership-a-devops-best-practice)
Embedding Ownership: A DevOps Best Practice

[chris-short/DevOps-README.md](https://github.com/chris-short/DevOps-README.md)
What to Read to Learn More About DevOps

[bridgetkromhout/devops-against-humanity](https://github.com/bridgetkromhout/devops-against-humanity)
DevOps Against Humanity (an expansion for Cards Against Humanity)

[Jim Leonardo](https://jimsrulesregardingeverything.com/2017/04/05/is-it-devops/)
(2017) Is it DevOps? What is DevOps and what is not DevOps

[Jason Bloomberg](http://websphere.sys-con.com/node/4122435)
(2017) Is #DevOps Falling into the Maturity Trap?

[Gary Woodfine](https://garywoodfine.com/not-devops-engineer/)
(2018) You are not a DevOps Engineer
Your organisation won’t be saved by a terminal wonder kid in a hoody churning awesome BASH scripts during his lunch break.
Changing your department names form Software Development and IT operations and moving them to a co-located zone with a pool & Ping Pong tables, open plan kitchen and bean bags and then calling them DevOps is not really going to make your customers any happier.

[IdeasForDevOps/100IdeasForDevOps](https://github.com/IdeasForDevOps/100IdeasForDevOps)
100 Ideas to bring DevOps into an Organization

[Darío Blanco](https://medium.com/@dariobit/devops-is-counterintuitive-47979d6bc54d)
(2018) DevOps is counterintuitive
Reliability without sacrificing speed

[Redbubble](https://www.redbubble.com/shop/devops+stickers)
DevOps stickers

[Jeroen van Wilgenburg](https://vanwilgenburg.wordpress.com/2018/08/22/lessons-learned-after-serving-thousands-of-concurrent-users-in-a-devops-team-for-a-year/)
(2018) Lessons learned after serving thousands of concurrent users in a devops team for a year

[Tiexin Guo](https://medium.com/4th-coffee/on-devops-9-infrastructure-as-code-clean-code-terraform-introduction-and-best-practices-5d266132c70a)
(2021) On DevOps — 9. Infrastructure as Code — Clean Code, Terraform Introduction, and Best Practices

[Matt Watson](https://stackify.com/supporting-production-applications-devops-way/)
(2014) Supporting Production Applications the DevOps Way

[DevOps Topologies](http://web.devopstopologies.com/). There is no ‘right’ team topology, but several ‘bad’ topologies for any one organisation. Original article -> [Matthew Skelton](https://blog.matthewskelton.net/2013/10/22/what-team-structure-is-right-for-devops-to-flourish/)
(2013) What Team Structure is Right for DevOps to Flourish?

[Dmitriy Samovskiy](http://www.somic.org/2010/03/02/the-rise-of-devops/)
(2010) The Rise of DevOps

[Cameron van Orman](https://enterprisersproject.com/article/2014/7/devops-not-synonym-application-development)
(2014) DevOps is not a synonym for application development

[Helen Beal](https://www.infoq.com/news/2017/10/devops-teams-good-or-bad)
(2017) The Industry Just Can't Decide about DevOps Teams

[Carla Rudder](https://enterprisersproject.com/article/2018/1/10-bad-devops-habits-break)
(2018) 10 bad DevOps habits to break

[Google](https://www.google.be/search?q=why+devops+is+bad)
Why devops is bad
interesting search results

[Alison DeNisco Rayome](https://www.techrepublic.com/article/10-bad-habits-devops-admins-must-break/)
(2018) 10 bad habits DevOps admins must break

[Daniel Oh](https://opensource.com/article/18/8/getting-started-devops-6-mistakes-avoid)
(2018) 6 DevOps mistakes to avoid

[Carla Rudder](https://enterprisersproject.com/article/2018/7/how-be-stronger-devops-leader-9-tips)
(2018) How to be a stronger DevOps leader: 9 tips

[Cornelia Davis](https://itrevolution.com/devops-who-does-what-cornelia-davis/)
(2018) DevOps Who Does What

[Mark Pundsack](https://about.gitlab.com/2017/10/04/devops-strategy/)
(2017) Beyond CI/CD: GitLab's DevOps vision
How we're building GitLab into the complete DevOps toolchain.

[GitLab](https://gitlab.com/gitlab-org/gitlab-ee/issues/2517)
[Sid Sijbrandij](https://about.gitlab.com/2017/06/29/whats-next-for-gitlab-ci/)
From 2/3 of the self-hosted Git market, to the next-generation CI system, to Auto DevOps
Auto DevOps is next via (2017)

[Jim Bird](http://swreflections.blogspot.be/2016/04/devopsdays-empathy-scaling-docker.html)
(2016) DevOpsDays: Empathy, Scaling, Docker, Dependencies and Secrets
interesting takeaways

[Mike Loukides](https://www.oreilly.com/ideas/the-evolution-of-devops)
(2017) The evolution of DevOps
:star:

[Markus Harrer](https://www.feststelltaste.de/session-summary-devops-camp-compact-2017/)
(2017) What prevents you from doing software development effectively?”

[Dan Barker](https://opensource.com/article/18/2/essential-roles-devops-culture-success)
(2018) Your DevOps attempt will fail without these 7 departments buying in
Achieving customer value requires more than just software development and IT operations.

[Russ Collier](https://www.devopsonwindows.com/it-takes-dev-and-ops-to-make-devops/)
(2013) It Takes Dev and Ops to Make DevOps

[arvind](https://www.codementor.io/arvindsoni/in-devops-dev-is-killing-ops-d8gr1zdkh)
(2017) In DevOps, Dev is Killing Ops // read the full article + conclusion to have a better understanding

[The Disciplined Agile (DA) Framework](http://www.disciplinedagiledelivery.com/disciplineddevops/)
Disciplined DevOps

[Manisha Sahasrabudhe](https://sdtimes.com/stuck-new-devops-matrix-hell/)
(2017) Are you stuck in the new DevOps matrix from hell?
about complexity of env-app configuration management

[Aymen El Amri](https://medium.com/devopslinks/the-most-popular-devops-stories-in-2016-954d10698d67)
The Most Popular DevOps Stories In 2016

[mumble.org.uk](https://mumble.org.uk/blog/2022/02/02/infrastructure-in-this-post-devops-world/)
(2022) Infrastructure in this post-DevOps world ?

[Devoxx Belgium](https://devoxx.be/2017/11/the-top-100-rated-devoxx-belgium-2017-talks/)
(2017) The Top-100 rated Devoxx Belgium 2017 talks

[Joran Le Cren](http://squad-twelve.com/2017/07/03/7-specific-suggestions-to-sabotage-devops-simply/)
(2017) 7 Specific Suggestions to Sabotage DevOps Simply

[Grant Fritchey](https://www.red-gate.com/blog/database-devops/youre-not-delivering-devops-database/amp?__twitter_impression=true)
(2017) You’re not delivering DevOps to the database
> Please, developers, don’t get smug. I’m starting with you because you’re a core part of the problem here. Go back and re-read the definitions of DevOps … I’ll wait … You have to notice one salient point. Nowhere does it say, “Developers rule the world”, or “Developers have ‘SA’ privileges”, or “We get to ignore the Operations side of IT and do anything we want”. No, instead, it talks about cooperation.

[DevOpsGuys](https://www.red-gate.com/blog/database-devops/wheres-the-ops-in-devops-part-1)
(2017) Where’s the Ops in DevOps? Part 1.
[Part 2](https://www.red-gate.com/blog/database-devops/wheres-the-ops-in-devops-part-2)
[Part 3](https://www.red-gate.com/blog/database-devops/wheres-the-ops-in-devops-part-3)
> DevOps does not equal ‘Developers managing Production’

[Mirco Hering](https://notafactoryanymore.com/2018/02/01/why-you-are-probably-not-as-advanced-in-your-agile-devops-journey-as-you-think-you-are/)
(2018) Why you are probably not as advanced in your Agile/DevOps journey as you think you are

[Cold-blooded software | Hacker News](https://news.ycombinator.com/item?id=38793206)
[Cold-blooded software](https://dubroy.com/blog/cold-blooded-software/)

[The Big DevOps Misunderstanding | Hacker News](https://news.ycombinator.com/item?id=29617794)
[The Big DevOps Misunderstanding. When the term DevOps came up it was all… | by Oliver Wolf | Medium](https://linkedrecords.com/the-big-devops-misunderstanding-8435a910a5fd)

[DevOps is broken | Hacker News](https://news.ycombinator.com/item?id=33274988)
[DevOps Is Bullshit (2022) | Hacker News](https://news.ycombinator.com/item?id=36354049)
[DevOps is Bullshit | Massdriver Blog](https://www.massdriver.cloud/blogs/devops-is-bullshit)

[Knightmare: A DevOps Cautionary Tale (2014) | Hacker News](https://news.ycombinator.com/item?id=37459495)
[Knightmare: A DevOps Cautionary Tale - Doug Seven](https://dougseven.com/2014/04/17/knightmare-a-devops-cautionary-tale/)

[Gruntwork - The Modern Alternative to Devops Consultants](https://www.gruntwork.io/)

## devops community

[Electric Cloud Blog](https://electric-cloud.com/blog/)
DevOps, Continuous Delivery, and all that jazz...

[GitLab](https://about.gitlab.com/blog/archives.html)
Blog archives, mixed content about GitLab, DevOps and CI/CD

[Codeship](https://blog.codeship.com/archive/)
Codeship Blog, about CI/CD

[The Continuous Delivery Aliance](http://alliance.praqma.com/initiatives/)
a community of Continuous Delivery and DevOps companies who work together to learn and facilitate best practices shared among the members.

[DevOps Con](https://devopsconference.de/program/)
The Conference for Continuous Delivery, Microservices,
Containers, Clouds and Lean Business

[DevOps Conferences 2018](https://www.gotodevops.org/)

[John P. Mello Jr.](https://techbeacon.com/best-devops-conferences-2018)
(2018) The best DevOps conferences of 2018

[fabric8 Blog](https://blog.fabric8.io/)
Blog of fabric8, the open source microservices platform for developers, based on Docker, Kubernetes and Jenkins

[ACM Queue](https://queue.acm.org/)
studies on Software, DevOps, Computing Machinery ...

[StackStorm Exchange](https://exchange.stackstorm.org/)
Automate all the things you already know and use with dozens of ready-made integration packs. Cloud providers, monitoring services, lightbulbs. It’s extendable, flexible, and built with love for DevOps and ChatOps

[DevOps'ish](https://devopsish.com/)
DevOps, Cloud Native, Open Source, and the ‘ish in between.
:star:

[DEV](https://dev.to/t/devops)
DevOps related articles on dev.to()

[Stack Exchange](https://devops.stackexchange.com/)
DevOps questions & answers

[/r/devops](https://www.reddit.com/r/devops/)
Everything Devops on reddit

[Puppet Blog](https://puppet.com/blog)
educates readers on configuration management, cloud migration and cloud management, DevOps, security, compliance, Windows ...

[Medium](https://medium.com/tag/devops)
DevOps Stories on medium

[InfoWorld](https://www.infoworld.com/category/devops/)
information, news, how-to advices about DevOps

[DevOpsLinks](https://medium.com/devopslinks)
The Must-Read Publication for Aspiring DevOps Professionals
:star:

[CloudBees](https://www.cloudbees.com/blog)
CloudBees Blog
[CloudBees](https://www.youtube.com/channel/UCKlF3GIFy9KVUefVbycx_vw)
CloudBees TV Youtube Channel

[DZone](https://dzone.com/devops-tutorials-tools-news/list)
DZone Devops latest articles

[Netflix](https://medium.com/@NetflixTechBlog)
[Netflix](https://medium.com/netflix-techblog)
NetFlix Technology Blog

[All Things Distributed](http://www.allthingsdistributed.com/)
Werner Vogels' (Amazon' CTO) weblog on building scalable and robust distributed systems.

[GoCD Blog](https://www.gocd.org/blog/)
Continuous Delivery techniques, thoughts, learnings

[Redgate Blog](https://www.red-gate.com/blog/database-devops)
Database / DevOps articles

[Pivotal](https://content.pivotal.io/)
featured news & stories about DevOps, Cloud, Containers, Software etc.

[Build to Adapt at Pivotal](https://builttoadapt.io/)
Stories and insights on how software is changing the way society and businesses are built, from Pivotal.

[Paul Hammant](https://paulhammant.com/archive/)
articles about CD, DevOps, etc.
[Continuous_Delivery](https://paulhammant.com/categories.html#Continuous_Delivery)
[DevOps](https://paulhammant.com/categories.html#DevOps)

[sysadvent](https://sysadvent.blogspot.be/)
One article for each day of December, ending on the 25th article
great articles about systems administration topics written by fellow sysadmins.

[HangOps](https://signup.hangops.com/)
is a large, active DevOps slack community.

[Devops Engineers](https://devopsengineers.com/)
A group of engineers talking about devops related topics in a Slack channel

[DevOpsChat](https://devopschat.co/)
Get involved with the Largest DevOps Slack Community

[DevOpsLinks on Slack](http://devopslinks.com/)
Where “software DEVelopment” meets “information technology OPerationS”

[SweetOps](https://slack.cloudposse.com/)
is a collaborative DevOps community for engineers of all skill levels, sponsored by Cloud Posse.

[A Cloud Guru Blog](https://acloudguru.com/blog)
Cloud Technology Updates and More
Stay up to date on what's happening in technology, industry insights, technical skills development and all things cloud learning, and cloud certifications.

[Honeycomb Blog](https://www.honeycomb.io/blog/)
Honeycomb helps engineering teams deeply understand their own production systems through observability. Their mission : Give all software engineering teams the observability they need to eliminate toil and delight their users.

[netsys - Networks and Distributed Systems (NetSys) Lab](https://www.netsys.ovgu.de/)

## devops conferences

[A reawakening of systems programming meetups | Hacker News](https://news.ycombinator.com/item?id=40897506)
[A reawakening of systems programming meetups | notes.eatonphil.com](https://notes.eatonphil.com/2024-07-07-systems-meetups.html)

[Berlin Buzzwords 2022 | Berlin Buzzwords 2022](http://berlinbuzzwords.de/)
[How to measure Diversity of Search Results | Berlin Buzzwords 2021](https://2021.berlinbuzzwords.de/session/how-measure-diversity-search-results)

## dynamic loading

[Amir Rachum](http://amir.rachum.com/blog/2016/09/17/shared-libraries/)
(2016) Shared Libraries: Understanding Dynamic Loading

## embedded systems

[Adrian Colyer](https://blog.acolyer.org/2017/12/01/analyzing-software-requirements-errors-in-safety-critical-embedded-systems/)
(2017) Analyzing software requirements errors in safety-critical embedded systems

## enterprise computing

[Is this what enterprise means? | Hacker News](https://news.ycombinator.com/item?id=27051985)
[Stefano Verna on X: "Over a year ago we signed a @Salesforce Enterprise contract for @Heroku. Since then we're experiencing a real nightmare. 🧵 A distressing thread" / X](https://twitter.com/steffoz/status/1389946268764475394)

## enterprise-grade storage systems

[All my servers have an 8 GB empty file on disk | Hacker News](https://news.ycombinator.com/item?id=26583791)
[Why All My Servers Have an 8GB Empty File - BiteofanApple](https://brianschrader.com/archive/why-all-my-servers-have-an-8gb-empty-file/)

## enterprise-scale computing

[Internet Archive Infrastructure | Hacker News](https://news.ycombinator.com/item?id=26300191)
[Jonah Edwards - Internet Archive Infrastructure : Free Download, Borrow, and Streaming : Internet Archive](https://archive.org/details/jonah-edwards-presentation)

[Why does this code execute more slowly after strength-reducing multiplications? | Hacker News](https://news.ycombinator.com/item?id=31549050)
[assembly - Why does this code execute more slowly after strength-reducing multiplications to loop-carried additions? - Stack Overflow](https://stackoverflow.com/questions/72306573/why-does-this-code-execute-more-slowly-after-strength-reducing-multiplications-t)

[Mementos: System Support for Long-Running Computation on RFID-Scale Devices | Hacker News](https://news.ycombinator.com/item?id=36174893)
[UM-CS-2010-060.pdf](https://web.cs.umass.edu/publication/docs/2010/UM-CS-2010-060.pdf?ssp=1&setlang=sv-SE&safesearch=off)

## enterprise software

[Why Enterprise Software Sucks | Hacker News](https://news.ycombinator.com/item?id=21224209)
[Arvind Narayanan on X: "My university just announced that it's dumping Blackboard, and there was much rejoicing. Why is Blackboard universally reviled? There's a standard story of why "enterprise software" sucks. If you'll bear with me, I think this is best appreciated by talking about… baby clothes!" / X](https://twitter.com/random_walker/status/1182635589604171776)

## erasure coding

[Erasure Coding for Distributed Systems | Hacker News](https://news.ycombinator.com/item?id=41361281)
[Erasure Coding for Distributed Systems](https://transactional.blog/blog/2024-erasure-coding)

## everyone is bad at making it at scale

[Everyone is still terrible at creating software at scale | Hacker News](https://news.ycombinator.com/item?id=26759680)
[Everyone Is Still Terrible At Creating Software At Scale - Marginally Interesting by Mikio L. Braun](https://margint.blog/2021/04/05/creating-software-at-scale/)

## foundation models

[Apple's On-Device and Server Foundation Models | Hacker News](https://news.ycombinator.com/item?id=40639506)
[Introducing Apple’s On-Device and Server Foundation Models - Apple Machine Learning Research](https://machinelearning.apple.com/research/introducing-apple-foundation-models)

## get the design right from the beginning

[Leslie Lamport says if you don't get the design right from the beginning, then every piece of the code you write is a patch. Do you agree or disagree with his approach?](https://old.reddit.com/r/programming/comments/16dba6a/leslie_lamport_says_if_you_dont_get_the_design/)

## Hashicorp Vault

[strothj/vault/](https://hub.docker.com/r/strothj/vault/)
Vault Unofficial Docker Image

[HashiCorp](https://www.hashicorp.com/blog/vault-0-6/)
Vault 0.6 Release announcement

[Sreenivas Makam](https://sreeninet.wordpress.com/2016/10/01/vault-use-cases/)
(2016) Vault – Use cases

[Armon Dadgar](https://www.hashicorp.com/blog/why-we-need-dynamic-secrets)
(2018) Why We Need Dynamic Secrets
how applications do a terrible job keeping secrets, and why we need to embrace ephemeral credentials, or "Dynamic Secrets" in Vault.

## industry shifts

## info ops

[Antonio Cangiano](https://programmingzen.com/building-better-software-info-ops-daniel-b-markham-interview/)
(2018) Building Better Software With Info-Ops: An Interview With Daniel B. Markham

## infrastructure-from-code

[GitHub - ehsanmok/awesome-infrastructure-from-code: Awesome list of Infrastructure-from-Code](https://github.com/ehsanmok/awesome-infrastructure-from-code)

## infrastructure

[Almost every infrastructure decision I endorse or regret | Hacker News](https://news.ycombinator.com/item?id=39313623)
[(Almost) Every infrastructure decision I endorse or regret after 4 years running infrastructure at a startup · Jack's home on the web](https://cep.dev/posts/every-infrastructure-decision-i-endorse-or-regret-after-4-years-running-infrastructure-at-a-startup/)

[Yevgeniy Brikman](https://blog.gruntwork.io/5-lessons-learned-from-writing-over-300-000-lines-of-infrastructure-code-36ba7fadeac1)
(2018) 5 Lessons Learned From Writing Over 300,000 Lines of Infrastructure Code

[Marvin Pinto](https://disjoint.ca/writing/2015/11/26/a-framework-for-deployment-of-immutable-infrastructure/)
(2015) A Framework for Deployment of Immutable Infrastructure

[Dan Tehranian](https://dantehranian.wordpress.com/2014/08/11/building-a-better-dashboard-for-virtual-infrastructure/)
(2014) Building a Better Dashboard for Virtual Infrastructure

[David Futcher](https://blog.usejournal.com/you-dont-need-all-that-complex-expensive-distracting-infrastructure-a70dbe0dbccb)
(2019) You Don’t Need All That Complex/Expensive/Distracting Infrastructure

## it ops and sysadmin

[Linda Rosencrance](https://techbeacon.com/best-cloud-it-ops-conferences-2018)
(2018) The best cloud and IT Ops conferences of 2018

[TechBeacon](https://techbeacon.com/25-it-ops-pros-experts-follow-twitter)
25 IT Ops pros and experts to follow on Twitter

[TechBeacon](https://techbeacon.com/it-ops)
IT-OPS articles & resources

[O'Reilly Media](https://www.oreilly.com/topics/operations)
The latest ideas, articles about operations.

[Code as Craft](https://codeascraft.com/category/operations/)
Posts in category operations

[sysadvent](https://sysadvent.blogspot.be/)
One article for each day of December, ending on the 25th article
great articles about systems administration topics written by fellow sysadmins.

[SysAdvent Calendar](https://www.redpill-linpro.com/sysadvent/)
Pre Christmas Tips and Tricks for Sysadmins

[IT Landscape for sysadmins](https://sysadmin.it-landscape.info/)
Open source projects aggregator for system administrators.

[Nexthink](https://www.nexthink.com/periodic-table/)
Periodic Table of IT Ops Tools

[Show HN: Sysadmin Casts - simple bite-sized sysadmin screencasts | Hacker News](https://news.ycombinator.com/item?id=8011081)
[System Administration Screencasts](https://sysadmincasts.com/)
Good resources for sysadmin / ops / devops
[Justin Weissig](https://sysadmincasts.com/episodes/25-bits-sysadmins-should-know)
Bits Sysadmins Should Know

[Softpanorama](http://www.softpanorama.org/Admin/admin_horror_stories.shtml)
classification of sysadmin horror stories

[Robert Treat](https://sysadvent.blogspot.be/2017/12/day-6-sysadmins-evolution-of-role.html)
(2017) sysadmins - the evolution of a role amidst revolutionary hype.

[Deb Shinder](http://techgenix.com/fall-of-all-powerful-admin/)
The rise and fall of the all-powerful admin

[Paul English](https://opensource.com/article/17/7/truth-about-sysadmins)
(2017) The truth about sysadmins

[Ericka Chickowski](https://techbeacon.com/it-ops-fails-5-worst-blunders-2017)
(2017) Epic IT Ops fails: The 5 worst blunders of 2017

## Jenkins

[Jenkins](https://www.jenkins.io/)
CI/CD tools
NOTE: FROM FCC ARTICLE ON DEVOPS ENGINEER, FIND CHEAPER ALTERNATIVES
[Jenkins Update Sites](https://updates.jenkins-ci.org/)

[Jenkins World](https://www.cloudbees.com/jenkinsworld)
usually in USA, but by 2018 will also occur [Jenkins World Europe](https://dzone.com/articles/call-for-papers-is-open-for-jenkins-world-2018)

[Faheetah](https://gist.github.com/Faheetah/e11bd0315c34ed32e681616e41279ef4)
Jenkinsfile idiosynchrasies with escaping and quotes : Examples of weirdness of Jenkinsfile / Groovy syntax

[Maksym Grebenets](http://mgrebenets.github.io/mobile%20ci/2015/02/01/jenkins-remote-node)
(2015) Jenkins Remote Node on Mac OS X

[Damon Edwards](http://rundeck.org/news/2014/01/08/Jenkins-is-for-development-Rundeck-is-for-operations.html)
(2014) Jenkins is for Development. Rundeck is for Operations.

[Jenkins Jenkins : Security vulnerabilities, CVEs](https://www.cvedetails.com/vulnerability-list.php?vendor_id=15865&product_id=34004&version_id=0&page=1&hasexp=0&opdos=0&opec=0&opov=0&opcsrf=0&opgpriv=0&opsqli=0&opxss=0&opdirt=0&opmemc=0&ophttprs=0&opbyp=0&opfileinc=0&opginf=0&cvssscoremin=6&cvssscoremax=0&year=0&month=0&cweid=0&order=1&trc=29&sha=972b519195a324e211440860f0337f2d75a9aad6)

[Benjamin Muschko](https://bmuschko.com/blog/jenkins-shared-libraries/)
(2019) Best practices for writing Jenkins shared libraries

[Jenkins CI](https://www.youtube.com/channel/UC5JBtmoz7ePk-33ZHimGiDQ)
Jenkins CI Youtube Channel

## large-scale systems descriptions

[MangaDex infrastructure overview | Hacker News](https://news.ycombinator.com/item?id=28440742)
[Infrastructure overview](https://mangadex.dev/mangadex-v5-infrastructure-overview/)

[Google's infamous internal 2010 "I just want to serve 5TB" video now public | Hacker News](https://news.ycombinator.com/item?id=29082014)
[I just want to serve 5 terabytes. - YouTube](https://www.youtube.com/watch?v=3t6L-FlfeaI)

[Intel Problems | Hacker News](https://news.ycombinator.com/item?id=25833667)
[Intel Problems - Stratechery by Ben Thompson](https://stratechery.com/2021/intel-problems/)

[Cloudflare's Disruption | Hacker News](https://news.ycombinator.com/item?id=28707317)
[Cloudflare's Disruption - Stratechery by Ben Thompson](https://stratechery.com/2021/cloudflares-disruption/)

## load balancing

[DOESConsulting](http://www.doesconsulting.com/faq.shtml)
Load Balancing FAQs and Key Concepts

[Load Balancing | Hacker News](https://news.ycombinator.com/item?id=35588797)
[Load Balancing](https://samwho.dev/load-balancing/)

[Implementation of load balancer - Consistent hashing | by Jimmy leo | Medium](https://jimmyleo.medium.com/implementation-of-load-balancer-consistent-hashing-3c3f95f97ff6)

## microservices - go

[Shalitha Suranga ](https://blog.logrocket.com/building-microservices-go-gin/)
(2022) Building microservices in Go with Gin

## microservices

[Richard Clayton](https://rclayton.silvrback.com/failing-at-microservices)
(2014) Failing at Microservices.
Please avoid our mistakes!

[Martin Nally](https://apigee.com/about/blog/developer/12-goals-microservices)
(2016) The 12 Goals of Microservices

[Brian Kelly](https://www.datawire.io/using-fallacies-of-distributed-computing-to-build-resilient-microservices/)
Building Resilient Microservices from the Fallacies of Distributed Computing

[Brian Kelly](https://www.datawire.io/creating-a-microservice-answer-these-10-questions-first/)
Creating a Microservice? Answer these 10 Questions First

[Death by a Thousand Microservices | Hacker News](https://news.ycombinator.com/item?id=37477095)
[Death by a thousand microservices](https://old.reddit.com/r/programming/comments/16g7f3y/death_by_a_thousand_microservices/)
[Death By a Thousand Microservices](https://renegadeotter.com/2023/09/10/death-by-a-thousand-microservices.html)

[Monolith First (2015) | Hacker News](https://news.ycombinator.com/item?id=26190584)
[Monolith First](https://martinfowler.com/bliki/MonolithFirst.html)

[Bilgin Ibryam](https://thenewstack.io/introducing-microservices-hierarchy-needs/)
The Microservices Hierarchy of Needs and Where Kubernetes fits

[Manisha Sahasrabudhe](http://blog.shippable.com/7-things-to-consider-while-moving-to-microservices)
(2017) 7 things to consider while moving to a microservices architecture

[Hacker News](https://news.ycombinator.com/item?id=16166645)
(2018) Ask HN: How do you keep track of releases/deployments of dozens micro-services?

## microservices vs modules

[Modules, not microservices | Hacker News](https://news.ycombinator.com/item?id=34230641)
[You Want Modules, Not Microservices](https://blogs.newardassociates.com/blog/2023/you-want-modules-not-microservices.html)

## microservices vs monolith - 14

[Give me back my monolith (2019) | Hacker News](https://news.ycombinator.com/item?id=31327766)
[Give me back my monolith - Craig Kerstiens](https://www.craigkerstiens.com/2019/03/13/give-me-back-my-monolith/)

[The costs of microservices (2020) | Hacker News](https://news.ycombinator.com/item?id=38069915)
[The costs of microservices | Roberto Vitillo's Blog](https://robertovitillo.com/costs-of-microservices/)

[Why Segment Went Back to a Monolith | Hacker News](https://news.ycombinator.com/item?id=23017160)
[To Microservices and Back Again - Why Segment Went Back to a Monolith - InfoQ](https://www.infoq.com/news/2020/04/microservices-back-again/)

[Don't start with microservices - monoliths are your friend | Hacker News](https://news.ycombinator.com/item?id=29576352)
[Don't start with microservices in production - monoliths are your friend - Arnold Galovics](https://arnoldgalovics.com/microservices-in-production/)

[It's not microservice or monolith; it's cognitive load you need to understand first](https://fernandovillalba.substack.com/p/its-not-microservice-or-monolith)

[Ben Stopford](https://www.confluent.io/blog/data-dichotomy-rethinking-the-way-we-treat-data-and-services/)
(2016) The Data Dichotomy: Rethinking the Way We Treat Data and Services

[IcaliaLabs/guides](https://github.com/IcaliaLabs/guides/wiki/Monolithic-vs-Micro-Repos)
Monolithic vs Micro Repos

[Matt Butcher](https://gist.github.com/technosophos/9c706b1ef10f42014a06)
(2015) Why We Should Not Return to Monolithic Repositories

[Avi Cavale](http://blog.shippable.com/our-journey-to-microservices-and-a-mono-repository)
(2016) Our journey to microservices: mono repo vs multiple repositories

[Zhamak Dehghani](https://www.martinfowler.com/articles/break-monolith-into-microservices.html)
(2018) How to break a Monolith into Microservices
What to decouple and when

[mozilla.dev.developer-tools](https://groups.google.com/forum/m/#!topic/mozilla.dev.developer-tools/W17drvVMFhY)
Discussion about Multiple repos vs Monolithic repo

[Gregory Szorc](https://gregoryszorc.com/blog/2014/09/09/on-monolithic-repositories/)
(2014) On Monolithic Repositories
in favor of monolithic repos

[Aaron Schlesinger](https://gist.github.com/arschles/5d7ba90495eb50fa04fc)
(2015) Why We Should Use Monolithic Repositories

[Nathan Leiby](https://medium.com/always-a-student/mo-repos-mo-problems-how-we-make-changes-across-many-git-repositories-293ad7d418f0)
(2017) Mo Repos, Mo Problems? How We Make Changes Across Many Git Repositories

## monitoring

[Monitoring energy usage with smart plugs, Prometheus and Grafana | Hacker News](https://news.ycombinator.com/item?id=40266845)
[Monitoring energy usage with smart plugs, Prometheus and Grafana :: ./techtipsy](https://ounapuu.ee/posts/2024/05/02/smartplugs/)

## Mozilla hubs

[Hubs by Mozzila](https://hubs.mozilla.com/)
[The Next Generation of Mozilla Hubs is Here](https://hubs.mozilla.com/labs/mozilla-hubs-early-access-release)
VRChat-like hangout room (PC & PCVR)
[End of support for Mozilla Hubs | Hubs Help](https://support.mozilla.org/en-US/kb/end-support-mozilla-hubs)

## NGINX

[Nginx 1.25.0: experimental HTTP/3 support | Hacker News](https://news.ycombinator.com/item?id=36047524)
[nginx.org/en/CHANGES](https://nginx.org/en/CHANGES)

[The future of Nginx: Getting back to our open source roots | Hacker News](https://news.ycombinator.com/item?id=32572153)
[The Future of NGINX: Getting Back to Our Open Source Roots - NGINX](https://www.nginx.com/blog/future-of-nginx-getting-back-to-our-open-source-roots/)

[Do svidaniya, Igor, and thank you for Nginx | Hacker News](https://news.ycombinator.com/item?id=29985871)
[Do Svidaniya, Igor, and Thank You for NGINX - NGINX](https://www.nginx.com/blog/do-svidaniya-igor-thank-you-for-nginx/)

## NGINX vs Caddy

[35M Hot Dogs: Benchmarking Caddy vs. Nginx | Hacker News](https://news.ycombinator.com/item?id=32865497)
[Tyblog | 35 Million Hot Dogs: Benchmarking Caddy vs. Nginx](https://blog.tjll.net/reverse-proxy-hot-dog-eating-contest-caddy-vs-nginx/)

## observability and monitoring

[Fred Hébert](https://ferd.ca/operable-software.html)
(2019) Operator Experience (OpEx), Observability, and making observable systems

## on-premise servers

[Ask HN: Is your company sticking to on-premise servers? Why? | Hacker News](https://news.ycombinator.com/item?id=23089999)

## Openshift

[OpenShift Blog](https://blog.openshift.com/)
OpenShift latest news

[OpenShift](https://www.openshift.com/container-platform/features.html)
Features and Benefits of OpenShift

[Red Hat Customer Portal](https://access.redhat.com/documentation/en-us/openshift_enterprise/3.1/html/cluster_administration/admin-guide-sdn-troubleshooting)
Troubleshooting OpenShift SDN

[openshift/debugging-openshift](https://github.com/openshift/origin/blob/master/docs/debugging-openshift.md)
Debugging / Troubleshooting OpenShift

[OpenShift Origin](https://github.com/openshift/origin/tree/master/examples)
OpenShift Origin examples on GitHub

[Curtis Yanko](http://blog.sonatype.com/nexus-in-openshift)
Nexus in Openshift

## openstack

[Thierry Carez](http://superuser.openstack.org/articles/openstack-relevant-containers)
What makes OpenStack relevant in a container-driven world.
[Related Video](https://www.youtube.com/watch?v=2QnHdncpypI)

## operability

[Matthew Skelton](https://blog.softwareoperability.com/2013/10/16/operability-can-improve-if-developers-write-a-draft-run-book/)
(2013) Operability can Improve if Developers Write a Draft Run Book

[Steve Smith](https://www.continuousdeliveryconsulting.com/blog/aim-for-operability-not-devops-as-a-cult/)
(2017) Aim for Operability, not DevOps As A Cult

## operations

[Cindy Sridharan](https://medium.com/@copyconstruct/the-death-of-ops-is-greatly-exaggerated-ff3bd4a67f24)
(2017) Everyone is not Ops

[Doug Tedder](https://www.dougtedder.com/2017/09/03/ops-just-get-out-of-the-way/)
(2017) Ops, just get out of the way

[Rob Kinyon](https://sysadvent.blogspot.be/2016/12/day-10-what-does-operations-do.html)
:star:
(2016) What does Operations *do*?

[Ian Miell](https://zwischenzugs.com/2020/11/30/gitops-decisions/)
(2020) GitOps Decisions

[Charity Majors aka mipsytipsy](https://opensource.com/article/17/7/state-systems-administration)
(2017) Ops: It's everyone's job now

[Ask HN: How do you deal with operational work as a software engineer? | Hacker News](https://news.ycombinator.com/item?id=15737215)
(2017) How do you deal with operational work as a software engineer?

[Coda Hale](https://codahale.com/risky-business-requires-active-operators/)
(2017) Risky Business Requires Active Operators
about the risks of automation in order to successfully and safely wield its power.

[Charity Majors](https://www.honeycomb.io/blog/the-future-of-ops-careers/)
(2020) The Future of Ops Careers.
[Christine Yen](https://www.honeycomb.io/blog/the-future-of-developer-careers/)
on the same blog.

[Jan Schaumann](https://www.netmeister.org/blog/ops-lessons.html)
(2020) (A few) Ops Lessons We All Learn The Hard Way

[ops.tips](https://ops.tips/)
articles, tutorials and guides about cloud-native technologies: AWS, Golang, Containers, Linux, Infrastructure as a Service and DevOps. [All gists](https://ops.tips/gists/)
[All articles](https://ops.tips/blog/)

## parallel processing

[GNU Parallel, where have you been all my life? | Hacker News](https://news.ycombinator.com/item?id=37208083)
[GNU Parallel, where have you been all my life? | Alex Plescan](https://alexplescan.com/posts/2023/08/20/gnu-parallel/)

## performance optimization

[Ask HN: How can I learn about performance optimization? | Hacker News](https://news.ycombinator.com/item?id=39564632)

[Cassandra at Apple: 1000s of Clusters, 300k Nodes, 100 PB | Hacker News](https://news.ycombinator.com/item?id=33124631)
[Erick Ramirez on X: "Wait for it... @Cassandra 👁️ at @Apple 🍎 = thousands of clusters + 100s PB of data + 300K nodes + millions of QPS. @cscotta teases the audience @ApacheCon with the size of their environment. 🔥 #ACNA2022 #ApacheCassandra https://t.co/ZiBIleaDL9" / X](https://twitter.com/erickramirezau/status/1578063811495477248)

[300ms Faster: Reducing Wikipedia's total blocking time | Hacker News](https://news.ycombinator.com/item?id=36113430)
[300ms Faster: Reducing Wikipedia's Total Blocking Time](https://www.nray.dev/blog/300ms-faster-reducing-wikipedias-total-blocking-time/)

[Seeing through hardware counters: A journey to 3x performance increase | Hacker News](https://news.ycombinator.com/item?id=33540091)
[Seeing through hardware counters: a journey to threefold performance increase | by Netflix Technology Blog | Netflix TechBlog](https://netflixtechblog.com/seeing-through-hardware-counters-a-journey-to-threefold-performance-increase-2721924a2822)

## persistent connections

[Achieving 5M persistent connections with Project Loom virtual threads | Hacker News](https://news.ycombinator.com/item?id=31214253)
[ebarlas/project-loom-c5m: Experiment to achieve 5 million persistent connections with Project Loom virtual threads](https://github.com/ebarlas/project-loom-c5m)

## persistent uptime

[Careful with That Lock, Eugene | Hacker News](https://news.ycombinator.com/item?id=40025148)
[Robin's blog - Careful with That Lock, Eugene](https://kaveland.no/careful-with-that-lock-eugene.html)

## PKI

[Patrick Cable](https://sysadvent.blogspot.be/2017/12/day-4-this-christmas-build-your-own-pki.html)
(2017) This Christmas, build your own PKI

[Walter Goulet](http://blog.securism.com/2009/01/summarizing-pki-certificate-validation/)
(2009) Summarizing PKI certificate validation

## plugin system

[How to build a plugin system on the web and also sleep well at night | Hacker News](https://news.ycombinator.com/item?id=20770105)
[How to build a plugin system on the web and also sleep well at night | Figma Blog](https://www.figma.com/blog/how-we-built-the-figma-plugin-system/)

## postmortems

[GitHub - danluu/post-mortems: A collection of postmortems. Sorry for the delay in merging PRs!](https://github.com/danluu/post-mortems)
is a collection of postmortems (config errors, hardware failures, and more).

["I am literally losing sleep" over Java (1996) | Hacker News](https://news.ycombinator.com/item?id=29822042)
[Internal Tech Emails on X: "Bill Gates: I'm literally losing sleep over Java September 30, 1996 https://t.co/u9lduCtkW9" / X](https://twitter.com/TechEmails/status/1478785899009875968)

[Microsoft Exchange stops passing mail due to bug on 1/1/22 | Hacker News](https://news.ycombinator.com/item?id=29756714)
[Exchange 2019 Anti-Malware - Bad Update? : sysadmin](https://old.reddit.com/r/sysadmin/comments/rt91z6/exchange_2019_antimalware_bad_update/)

[Issues with Cloudflare Images | Hacker News](https://news.ycombinator.com/item?id=29474743)
[Daniel Skogly's blog | Cloudflare Images has a lot of issues](https://blog.klungo.no/2021/12/07/cloudflare-images-has-a-lot-of-issues/)

[HBO Max accidentally sent an integration email test to users | Hacker News](https://news.ycombinator.com/item?id=27546017)
[Internet of Shit on X: "Tfw when the integration test environment blasts literally everyone who uses the service 🤪 https://t.co/VntRiEfSDT" / X](https://twitter.com/internetofshit/status/1405682888545349635)

[The absolute worst scenario happened | Hacker News](https://news.ycombinator.com/item?id=26539495)
[The absolute worst case scenario happened, what should we do now? : sysadmin](https://old.reddit.com/r/sysadmin/comments/ma4mwl/the_absolute_worst_case_scenario_happened_what/)

[Bank tells customers to disable updates and not upgrade to iOS 16 | Hacker News](https://news.ycombinator.com/item?id=32790387)
[Your upgraded digital service | Coutts](https://www.coutts.com/coutts-digital/Bank-In-the-App.html)

[Watt's the worst thing you can do to a datacenter?](https://www.theregister.com/2023/09/11/who_me/)

[Sharing details on a recent incident impacting one of our customers | Hacker News](https://news.ycombinator.com/item?id=40466810)
[Details of Google Cloud GCVE incident | Google Cloud Blog](https://cloud.google.com/blog/products/infrastructure/details-of-google-cloud-gcve-incident/)

[How Figma's databases team lived to tell the scale | Hacker News](https://news.ycombinator.com/item?id=39706968)
[How Figma's Databases Team Lived to Tell the Scale | Figma Blog](https://www.figma.com/blog/how-figmas-databases-team-lived-to-tell-the-scale/)

[Making Greeble](https://web.archive.org/web/20190919204905/http://code.ryanmalm.com/JS13k_2017_postmortem)

[Kontra.js Postmortem. A postmortem about maintaining… by Steven Lambert - js13kGames - Medium](https://medium.com/js13kgames/kontra-js-postmortem-e1290f634283)

[The undocumented Android change that led to aCropalypse was reported during beta | Hacker News](https://news.ycombinator.com/item?id=35378109)
[The undocumented Android change that led to aCropalypse was reported during the beta - iliana.fyi](https://iliana.fyi/blog/acropalypse-now/)

[An incident impacting 5M accounts and private information on Twitter | Hacker News](https://news.ycombinator.com/item?id=32399949)
[An incident impacting some accounts and private information on Twitter](https://privacy.twitter.com/en/blog/2022/an-issue-affecting-some-anonymous-accounts)

[Stripe down for 4 hours (and counting) for all those with Stripe Tax enabled | Hacker News](https://news.ycombinator.com/item?id=32558191)
[Stripe system status](https://status.stripe.com/)

[Let us serve you, but don't bring us down | Hacker News](https://news.ycombinator.com/item?id=36110527)
[Let us serve you, but don't bring us down | Internet Archive Blogs](https://blog.archive.org/2023/05/29/let-us-serve-you-but-dont-bring-us-down/)

[Accident Forgiveness | Hacker News](https://news.ycombinator.com/item?id=41312834)
[Accident Forgiveness · The Fly Blog](https://fly.io/blog/accident-forgiveness/)

## postmortems - anticipated failures

[Why Twitter didn't go down: From a real Twitter SRE | Hacker News](https://news.ycombinator.com/item?id=33701371)
[Why Twitter Didn't Go Down: From a Real Twitter SRE](https://matthewtejo.substack.com/p/why-twitter-didnt-go-down-from-a)

[Friday night's near-disaster at JFK airport | Hacker News](https://news.ycombinator.com/item?id=34393078)
[What We Know Now About Friday Night's Near-Disaster At JFK Airport - View from the Wing](https://viewfromthewing.com/what-we-know-now-about-friday-nights-near-disaster-at-jfk-airport/)

[Tell HN: The 10-bit timers are about to overflow on September 17th | Hacker News](https://news.ycombinator.com/item?id=32700184)

["In roughly two hours, 1647 devices are about to be wiped" | Hacker News](https://news.ycombinator.com/item?id=34597387)
[Security Writer :verified: :donor:: "We have one client which we ma…" - Infosec Exchange](https://web.archive.org/web/20230607145927/https://infosec.exchange/@SecurityWriter/109777576538835360)

[SSD will fail at 40k power-on hours (2021) | Hacker News](https://news.ycombinator.com/item?id=32048148)
[Field Notice: FN70545 - SSD Will Fail at 40,000 Power-On Hours - BIOS/Firmware Upgrade Recommended - Cisco](https://www.cisco.com/c/en/us/support/docs/field-notices/705/fn70545.html)

## postmortems - aws

[Tell HN: AWS appears to be down again | Hacker News](https://news.ycombinator.com/item?id=29648286)
[Tell HN: AWS appears to be down again | Hacker News](https://news.ycombinator.com/item?id=29567170)

[AWS us-east-1 outage | Hacker News](https://news.ycombinator.com/item?id=29473630)
[AWS Cognito is having issues and health dashboards are still green | Hacker News](https://news.ycombinator.com/item?id=25209773)
[Service health | AWS Health Dashboard | Global](https://health.aws.amazon.com/health/status)

[AWS us-east-1 down | Hacker News](https://news.ycombinator.com/item?id=36315300)

[AWS us-east-2 outage | Hacker News](https://news.ycombinator.com/item?id=32267222)

[Summary of the AWS Service Event in the Northern Virginia (US-East-1) Region | Hacker News](https://news.ycombinator.com/item?id=29516482)
[Summary of the AWS Service Event in the Northern Virginia (US-EAST-1) Region](https://aws.amazon.com/message/12721/)

[Amazon packages pile up after AWS outage spawns delivery havoc | Hacker News](https://news.ycombinator.com/item?id=29480392)
[Amazon packages pile up after AWS outage spawns delivery havoc](https://www.detroitnews.com/story/business/2021/12/07/amazon-aws-cloud-users-report-issues-accessing-websites/6419088001/)

## postmortems - azure

[Ask HN: Azure has run out of compute - anyone else affected? | Hacker News](https://news.ycombinator.com/item?id=33743567)

## postmortems - CrowdStrike - 13

[Crowdstrike Outage Causing Widespread Issues | Hacker News](https://news.ycombinator.com/item?id=41002677)
[Microsoft CrowdStrike global outage hits Deloitte Qantas Woolworths and several countries around the world](https://www.afr.com/technology/businesses-crippled-by-widespread-it-outage-20240719-p5jv2t)

[CrowdStrike Update: Windows Bluescreen and Boot Loops | Hacker News](https://news.ycombinator.com/item?id=41002195)
[BSOD error in latest crowdstrike update : crowdstrike](https://old.reddit.com/r/crowdstrike/comments/1e6vmkf/bsod_error_in_latest_crowdstrike_update/)

[Multiple airlines disrupted due to Microsoft Azure outage | Hacker News](https://news.ycombinator.com/item?id=41001959)
[Frontier Airlines Briefly Grounds All Flights Amid Microsoft Outage - The New York Times](https://www.nytimes.com/2024/07/18/us/frontier-flights-grounded-microsoft.html)

[Initial details about why CrowdStrike's CSAgent.sys crashed | Hacker News](https://news.ycombinator.com/item?id=41021366)
[Patrick Wardle on X: "I don't do Windows but here are some (initial) details about why the CrowdStrike's CSAgent.sys crashed Faulting inst: mov r9d, [r8] R8: unmapped address ...taken from an array of pointers (held in RAX), index RDX (0x14 * 0x8) holds the invalid memory address @_JohnHammond https://t.co/oqlAVwSlJj" / X](https://x.com/patrickwardle/status/1814343502886477857)

[No More Blue Fridays | Hacker News](https://news.ycombinator.com/item?id=41033579)
[No More Blue Fridays](https://www.brendangregg.com/blog/2024-07-22/no-more-blue-fridays.html)

[CrowdStrike will be liable for damages in France, based on the OVH precedent | Hacker News](https://news.ycombinator.com/item?id=41066811)
[CrowdStrike will be liable for damages in France, based on the OVH precedent – The HFT Guy](https://thehftguy.com/2024/07/25/crowdstrike-will-be-liable-for-damages-in-france-based-on-the-ovh-precedent/)

[CrowdStrike's impact on aviation | Hacker News](https://news.ycombinator.com/item?id=41103101)
[CrowdStrike's Impact on Aviation - heavymeta.org](https://heavymeta.org/2024/07/28/crowdstrikes-impact-on-aviation.html)

[Microsoft technical breakdown of CrowdStrike incident | Hacker News](https://news.ycombinator.com/item?id=41095530)
[Windows Security best practices for integrating and managing security tools | Microsoft Security Blog](https://www.microsoft.com/en-us/security/blog/2024/07/27/windows-security-best-practices-for-integrating-and-managing-security-tools/)

[Matt Hamilton: "Crowdstrike BSOD offers us an …" - NAS](https://noauthority.social/@eriner/112813282721058872)

[CrowdStrike representatives issue trademark infringement notice to ClownStrike | Hacker News](https://news.ycombinator.com/item?id=41133917)
[Clown Services Company - Unregistered Agent, Incompliance, Welfare, Debt Market, Analog, and Imaginary-Risk Solutions](https://clownstrike.lol/crowdmad/)

[With Companies Like CrowdStrike, Who Needs Viruses?](https://tbot.substack.com/p/with-companies-like-crowdstrike-who)

[Parody site ClownStrike refused to bow to CrowdStrike's bogus DMCA takedown | Hacker News](https://news.ycombinator.com/item?id=41173486)
[Parody site ClownStrike refused to bow to CrowdStrike’s bogus DMCA takedown | Ars Technica](https://arstechnica.com/tech-policy/2024/08/parody-site-clownstrike-refused-to-bow-to-crowdstrikes-bogus-dmca-takedown/)

[CrowdStrike accepting the PwnieAwards for "most epic fail" at defcon | Hacker News](https://news.ycombinator.com/item?id=41217037)
[Dominic White 👾 on X: "CrowdStrike accepting the @PwnieAwards for “most epic fail” at @defcon. Class act. https://t.co/e7IgYosHAE" / X](https://x.com/singe/status/1822324795645575263)

## postmortems - gcp

[GCP Incidents | Hacker News](https://news.ycombinator.com/item?id=38495204)
[Not Everything Is Google's Fault (Just Most Things)](https://blog.railway.app/p/gcp-incidents)

## postmortems - instability stories

[Post-mortem for last week's incident at Kagi | Hacker News](https://news.ycombinator.com/item?id=39019119)
[Kagi.com is unstable for all regions | Kagi Status](https://web.archive.org/web/20240121000935/https://status.kagi.com/issues/2024-01-12-kagi-down-on-some-regions/)

[Netflix's new player breaks the ability to modify the seeking of a playing video | Hacker News](https://news.ycombinator.com/item?id=28896514)
[Single Page Apps for GitHub Pages](https://plopdown.video/blog/netflix-open-web-failure)

[Rogers network outage across Canada hits banks, businesses and consumers | Hacker News](https://news.ycombinator.com/item?id=32026637)
[Rogers network resuming after major outage hits millions of Canadians | Reuters](https://www.reuters.com/business/media-telecom/rogers-communications-services-down-thousands-users-downdetector-2022-07-08/)

## postmortems - security incidents

[Thanksgiving 2023 security incident | Hacker News](https://news.ycombinator.com/item?id=39220528)
[Thanksgiving 2023 security incident](https://blog.cloudflare.com/thanksgiving-2023-security-incident)

[March 7th, 2023 Incident update: cache configuration change leading to account vulnerability | Loom](https://www.loom.com/blog/march-7-incident-update)

## postmortems - slowdown stories

[A single line of code made a 24-core server slower than a laptop | Hacker News](https://news.ycombinator.com/item?id=29747921)
[A single line of code made a 24-core server slower than a laptop (2021) | Hacker News](https://news.ycombinator.com/item?id=36376669)
[How a Single Line of Code Made a 24-core Server Slower Than a Laptop | Piotr Kołaczkowski](https://pkolaczk.github.io/server-slower-than-a-laptop/)

[The Case of the Extra 40ms | Hacker News](https://news.ycombinator.com/item?id=25426195)
[The case of the extra 40 ms | Netflix TechBlog](https://netflixtechblog.com/life-of-a-netflix-partner-engineer-the-case-of-extra-40-ms-b4c2dd278513)

## postmortems - total outage stories - 38

[UK air traffic control meltdown | Hacker News](https://news.ycombinator.com/item?id=37461695)
[James Haydon - UK air traffic control meltdown](https://jameshaydon.github.io/nats-fail/)

[Tarsnap outage postmortem | Hacker News](https://news.ycombinator.com/item?id=36888954)
[2023-07-02 -- 2023-07-03 Tarsnap outage post-mortem](https://mail.tarsnap.com/tarsnap-announce/msg00050.html)

[Cloudflare outage on June 21, 2022 | Hacker News](https://news.ycombinator.com/item?id=31823132)
[Cloudflare outage on June 21, 2022](https://blog.cloudflare.com/cloudflare-outage-on-june-21-2022/)

[Roblox October Outage Postmortem | Hacker News](https://news.ycombinator.com/item?id=30013919)
[Roblox Return to Service 10/28-10/31 2021 - Roblox Blog](https://blog.roblox.com/2022/01/roblox-return-to-service-10-28-10-31-2021/)

[An Update on Our Outage | Hacker News](https://news.ycombinator.com/item?id=29062557)
[An Update on Our Outage - Roblox Blog](https://blog.roblox.com/2021/10/update-recent-service-outage/)

[Tell HN: GitHub is down again | Hacker News](https://news.ycombinator.com/item?id=29363169)

[GitHub issue - resolved | Hacker News](https://news.ycombinator.com/item?id=35325709)
[GitHub Status - Incident with Actions, API Requests, Codespaces, Git Operations, Issues, Pages and Pull Requests](https://www.githubstatus.com/incidents/52z0j6phhnjs)

[Error 404 (Not Found) | Hacker News](https://news.ycombinator.com/item?id=29243617)
[Spotify - Web Player: Music for everyone](https://open.spotify.com/)

[More details about the October 4 outage | Hacker News](https://news.ycombinator.com/item?id=28762611)
[More details about the October 4 outage - Engineering at Meta](https://engineering.fb.com/2021/10/05/networking-traffic/outage-details/)

[What Happened to Facebook, Instagram, and WhatsApp? | Hacker News](https://news.ycombinator.com/item?id=28750930)
[What Happened to Facebook, Instagram, & WhatsApp? - Krebs on Security](https://krebsonsecurity.com/2021/10/what-happened-to-facebook-instagram-whatsapp/)

[Fastly Outage | Hacker News](https://news.ycombinator.com/item?id=27432408)
[Powering the best of the internet | Fastly](https://www.fastly.com/)

[A former Uber engineer's disaster story | Hacker News](https://news.ycombinator.com/item?id=25373462)
[McLaren Stanley on X: "Alright folks, gather round and let me tell you the story of (almost) the biggest engineering disaster I've ever had the misfortune of being involved in. It's a tale of politics, architecture and the sunk cost fallacy [I'm drinking an Aberlour Cask Strength Single Malt Scotch]" / X](https://twitter.com/StanTwinB/status/1336890442768547845)

[Post Mortem of Google Outage on 14 December 2020 | Hacker News](https://news.ycombinator.com/item?id=25472455)
[Google Cloud Status Dashboard](https://status.cloud.google.com/incident/zall/20013#20013004=)

[Google outage - resolved | Hacker News](https://news.ycombinator.com/item?id=25415989)
[Google Workspace Status Dashboard](https://www.google.com/appsstatus/dashboard/)

[Why HN was down | Hacker News](https://news.ycombinator.com/item?id=5239673)

[A terrible, horrible, no-good, very bad day at Slack | Hacker News](https://news.ycombinator.com/item?id=23755843)
[A Terrible, Horrible, No-Good, Very Bad Day at Slack - Slack Engineering](https://slack.engineering/a-terrible-horrible-no-good-very-bad-day-at-slack/)

[Cloudflare was down | Hacker News](https://news.ycombinator.com/item?id=23875692)
[Cloudflare Is Having Issues | Hacker News](https://news.ycombinator.com/item?id=36294750)
[Cloudflare Status](https://www.cloudflarestatus.com/)
[Cloudflare Status](https://www.cloudflarestatus.com/?hn=2020)

[Level 3 Global Outage | Hacker News](https://news.ycombinator.com/item?id=24322861)
[Welcome to puck.nether.net](https://puck.nether.net/pipermail/outages/2020-August/013187.html)

[Facebook Messenger, Instagram and WhatsApp Outage | Hacker News](https://news.ycombinator.com/item?id=25372309)

[Slack is down | Hacker News](https://news.ycombinator.com/item?id=25632346)
[Status Site](https://slack-status.com/2021-01/9ecc1bc75347b6d1)

[March 20 ChatGPT outage: Here's what happened | Hacker News](https://news.ycombinator.com/item?id=35291112)
[March 20 ChatGPT outage: Here's what happened](https://openai.com/blog/march-20-chatgpt-outage)

[Western Digital cloud services down for 4 days | Hacker News](https://news.ycombinator.com/item?id=35478007)
[status.mycloud.com/os4](https://status.mycloud.com/os4)

[Reddit.com appears to be having an outage | Hacker News](https://news.ycombinator.com/item?id=36294244)

[Ask HN: Is GitHub down? | Hacker News](https://news.ycombinator.com/item?id=36523878)

[GitHub.com is down | Hacker News](https://news.ycombinator.com/item?id=36523843)
[github.com/status](https://github.com/status)

[Statement regarding the ongoing Sourcehut outage | Hacker News](https://news.ycombinator.com/item?id=38966035)
[Statement regarding the ongoing SourceHut outage](https://web.archive.org/web/20240114143300/https://outage.sr.ht/)

[How not to blow up the production database | Hacker News](https://news.ycombinator.com/item?id=28881151)
[How not to blow up the production database](https://blog.battlefy.com/how-not-to-blow-up-the-production-database-424c162dccc6)

[How to Recover from Deployment Hell - What I Learned After My Discord Bot Crashed on a 1,000+ User Server](https://www.freecodecamp.org/news/recovering-from-deployment-hell-what-i-learned-from-deploying-my-discord-bot-to-a-1000-user-server)

[Pirate Bay founder thinks Parler's inability to stay online is 'embarrassing' | Hacker News](https://news.ycombinator.com/item?id=25769730)
[Pirate Bay Founder Thinks Parler's Inability to Stay Online Is 'Embarrassing'](https://www.vice.com/en/article/3an7pn/pirate-bay-founder-thinks-parlers-inability-to-stay-online-is-embarrassing)

[Post Mortem on Cloudflare Control Plane and Analytics Outage | Hacker News](https://news.ycombinator.com/item?id=38138640)
[Post mortem on the Cloudflare Control Plane and Analytics Outage](https://blog.cloudflare.com/post-mortem-on-cloudflare-control-plane-and-analytics-outage/)

[FAA NOTAM System Outage | Hacker News](https://news.ycombinator.com/item?id=34337158)
[ATCSCC Advisory](https://www.fly.faa.gov/adv/adv_otherdis.jsp?advn=13&adv_date=01112023&facId=DCC&title=NOTAM+SYSTEM+EQUIPMENT+OUTAGE_FYI&titleDate=01/11/23)

[Cellular outage in U.S. hits AT&T, T-Mobile and Verizon users | Hacker News](https://news.ycombinator.com/item?id=39465517)
[AT&T cellular service restored after daylong outage; cause still unknown](https://www.cnbc.com/2024/02/22/cellular-outages-hit-thousands-in-us-and-att-users-most-affected.html)

[About the Tailscale.com outage on March 7, 2024 | Hacker News](https://news.ycombinator.com/item?id=39875822)
[About the Tailscale.com outage on March 7, 2024](https://tailscale.com/blog/tls-outage-20240307)

[Gitlab melts down](https://about.gitlab.com/2017/02/10/postmortem-of-database-outage-of-january-31/)
postmortem on the database outage of January 31 2017 with the lessons we learned.

[Meta outage | Hacker News](https://news.ycombinator.com/item?id=39604590)
[Status and outages of Meta business products](https://metastatus.com/)

[Don MacAskill](https://don.blogs.smugmug.com/2011/04/24/how-smugmug-survived-the-amazonpocalypse/)
(2011) How SmugMug survived the Amazonpocalypse

[Denny Cherry](http://itknowledgeexchange.techtarget.com/sql-server/another-cloud-outage-awsdown-this-time-another-group-of-companies-show-they-dont-have-dr/)
(2017) Another Cloud Outage (#awsdown this time) Another Group of Companies Show They Don’t Have DR

[Simon Sharwood](https://www.theregister.co.uk/2017/02/01/gitlab_data_loss/)
(2017) GitLab.com melts down after wrong directory deleted, backups fail

## postmortems - vulnerabilities

[This shouldn't have happened: A vulnerability postmortem | Hacker News](https://news.ycombinator.com/item?id=29407636)
[Project Zero: This shouldn't have happened: A vulnerability postmortem](https://googleprojectzero.blogspot.com/2021/12/this-shouldnt-have-happened.html)

## production database

[cscareerthrowaway567](https://www.reddit.com/r/cscareerquestions/comments/6ez8ag/accidentally_destroyed_production_database_on/)
(2017) Accidentally destroyed production database on first day of a job, and was told to leave, on top of this i was told by the CTO that they need to get legal involved, how screwed am i?

[Things I learned from building a production database | Hacker News](https://news.ycombinator.com/item?id=29322515)
[42 things I learned from building a production database | mahesh's blog](https://maheshba.bitbucket.io/blog/2021/10/19/42Things.html)

## protocol buffers

[Michael Bernstein](https://codeclimate.com/blog/choose-protocol-buffers/)
(2014) 5 Reasons to Use Protocol Buffers Instead of JSON For Your Next Service

## resilience engineering

[GitHub - lorin/resilience-engineering: Resilience engineering papers](https://github.com/lorin/resilience-engineering)

## RTOS

[Zephyr Project – A proven RTOS ecosystem, by developers, for developers](https://www.zephyrproject.org/)
[GitHub - golioth/awesome-zephyr-rtos: A curated list of awesome projects and resources for the Zephyr RTOS project.](https://github.com/golioth/awesome-zephyr-rtos)

## Saltstack vs Ansible vs Puppet

[Martin Rusev](https://web.archive.org/web/20170712022233/https://www.amon.cx/blog/saltstack-review/)
(2015) SaltStack - Review and how it fares against Ansible and Puppet?

[Josh Dreyfuss](http://blog.takipi.com/deployment-management-tools-chef-vs-puppet-vs-ansible-vs-saltstack-vs-fabric/)
Deployment Management Tools: Chef vs. Puppet vs. Ansible vs. SaltStack vs. Fabric

## scalability

[Scalability is overrated | Hacker News](https://news.ycombinator.com/item?id=34656776)
[Scalability is overrated - by Waseem Daher](https://waseem.substack.com/p/scalability-is-overrated)

[binhnguyennus/awesome-scalability: The Patterns of Scalable, Reliable, and Performant Large-Scale Systems](https://github.com/binhnguyennus/awesome-scalability)
best practices in building High Scalability, High Availability, High Stability, and more.

[Serving Netflix Video Traffic at 800Gb/s and Beyond [pdf] | Hacker News](https://news.ycombinator.com/item?id=32519881)
[2022-Streaming-Summit-Netflix.pdf](https://nabstreamingsummit.com/wp-content/uploads/2022/05/2022-Streaming-Summit-Netflix.pdf)

[The end of a myth: Distributed transactions can scale | Hacker News](https://news.ycombinator.com/item?id=35520044)
[The end of a myth: Distributed transactions can scale](https://muratbuffalo.blogspot.com/2023/04/the-end-of-myth-distributed.html)

## search engine - Amazon_Elasticsearch

[Official Elasticsearch Python library no longer works with open-source forks | Hacker News](https://news.ycombinator.com/item?id=28110610)
[Verify connection to Elasticsearch by sethmlarson · Pull Request #1623 · elastic/elasticsearch-py](https://github.com/elastic/elasticsearch-py/pull/1623)

[Amazon: Not OK - Why we had to change Elastic licensing | Hacker News](https://news.ycombinator.com/item?id=25833781)
[Amazon: NOT OK - why we had to change Elastic licensing | Elastic Blog](https://www.elastic.co/blog/why-license-change-aws)

[Boosting the power of Elasticsearch with synonyms](https://www.elastic.co/blog/boosting-the-power-of-elasticsearch-with-synonyms)

[Analyzing online search relevance metrics with Elasticsearch & the Elastic Stack](https://www.elastic.co/blog/analyzing-online-search-relevance-metrics-with-the-elastic-stack)

[Better than Average: Sort by Best Rating with Elasticsearch](https://www.elastic.co/blog/better-than-average-sort-by-best-rating-with-elasticsearch)

[Practical BM25 Part 1: How Shards Affect Relevance Scoring in Elasticsearch](https://www.elastic.co/blog/practical-bm25-part-1-how-shards-affect-relevance-scoring-in-elasticsearch)

[ElasticON conference events for Elasticsearch and ELK Stack users](https://www.elastic.co/elasticon)

[Implementing a Linkedin like search as you type with Elasticsearch](https://spinscale.de/posts/2020-05-29-implementing-a-linkedin-like-search-as-you-type-with-elasticsearch.html)

[Migrating to Elasticsearch with dense vector for Carousell Spotlight search engine](https://medium.com/carousell-insider/migrating-to-elasticsearch-with-dense-vector-for-carousell-spotlight-search-engine-e328b16155fc)

## separation of concerns

[Derek Greer](http://aspiringcraftsman.com/2008/01/03/art-of-separation-of-concerns/)
(2008) The Art of Separation of Concerns

## serverless

[Finnian Anderson](https://finnian.io/blog/colourising-video-with-openfaas-serverless-functions/)
(2017) Colourising Video with OpenFaaS Serverless Functions

[Rethinking serverless with FLAME | Hacker News](https://news.ycombinator.com/item?id=38542764)
[Rethinking Serverless with FLAME · The Fly Blog](https://fly.io/blog/rethinking-serverless-with-flame/)

[Paul Johnston](https://hackernoon.com/serverless-is-about-automation-not-functions-3f816c90ce61)
(2017) Serverless is about Automation, not Functions

[Richard Clayton](https://rclayton.silvrback.com/serverless-isn-t-effortless)
(2017) Serverless isn't Effortless
Lessons we learned in our first serious Serverless project.

[Introducing serverless SFTP and infinitely-scalable data storage Stedi](https://www.stedi.com/blog/introducing-serverless-sftp-and-infinitely-scalable-data-storage)

## server racks

[The first Oxide rack being prepared for customer shipment | Hacker News](https://news.ycombinator.com/item?id=36552015)
[Oxide Computer Company: "The first Oxide rack being pre…" - Hachyderm.io](https://hachyderm.io/@oxidecomputer/110635621269494973)

## server side rendering

[The future (and the past) of the web is server side rendering | Hacker News](https://news.ycombinator.com/item?id=34644558)
[The Future (and the Past) of the Web is Server Side Rendering](https://deno.com/blog/the-future-and-past-is-server-side-rendering)

## service discovery

[Engin Yöyen](http://enginyoyen.com/service-discovery-choosing-the-right-tool/)
Service Discovery : Choosing the Right Tool

## software architectures

[Ask HN: Why do message queue-based architectures seem less popular now? | Hacker News](https://news.ycombinator.com/item?id=40723302)

[Software Architecture Is Overrated, Clear and Simple Design Is Underrated | Hacker News](https://news.ycombinator.com/item?id=21001676)
[Software Architecture is Overrated, Clear and Simple Design is Underrated - The Pragmatic Engineer](https://blog.pragmaticengineer.com/software-architecture-is-overrated/)

[A Theory of Software Architecture | Hacker News](https://news.ycombinator.com/item?id=24915497)
[The Grand Unified Theory of Software Architecture - danuker | freedom & tech](https://danuker.go.ro/the-grand-unified-theory-of-software-architecture.html)

[Unified Architecture - A Simpler Way to Build Full-Stack Apps](https://www.freecodecamp.org/news/full-stack-unified-architecture)

## software architectures - offline first

[Offline First | Hacker News](https://news.ycombinator.com/item?id=28690427)
[Local First / Offline First | RxDB - JavaScript Database](https://rxdb.info/offline-first.html)
[Downsides of Offline First | Hacker News](https://news.ycombinator.com/item?id=28717848)
[Downsides of Local First / Offline First | RxDB - JavaScript Database](https://rxdb.info/downsides-of-offline-first.html)

## software architectures - type-driven design

[Parse, don't validate (2019) | Hacker News](https://news.ycombinator.com/item?id=35053118)
[Parse, Don't Validate (2019) | Hacker News](https://news.ycombinator.com/item?id=41031585)
[Parse, don’t validate](https://lexi-lambda.github.io/blog/2019/11/05/parse-don-t-validate/)

## software dev outsourcing

[Ask HN: Should we bring software dev in-house? | Hacker News](https://news.ycombinator.com/item?id=41161315)

## SRE - 11

[Reliability: It's Not Great | Hacker News](https://news.ycombinator.com/item?id=35044516)
[Reliability: It's Not Great - Fly.io](https://community.fly.io/t/reliability-its-not-great/11253)

[How to contact Google SRE by dropping a shell in Cloud SQL | Hacker News](https://news.ycombinator.com/item?id=24216009)
[How to contact Google SRE: Dropping a shell in cloud SQL - Offensi](https://offensi.com/2020/08/18/how-to-contact-google-sre-dropping-a-shell-in-cloud-sql/)

[Josh @ Overseer](https://engr.overseerlabs.io/the-devops-tool-arsenal-results-from-100-devops-sre-surveys-c453483742f)
The DevOps tool arsenal: Results from ~100 DevOps/SRE surveys

[Engineering WordPress for 10,000 Visitors per Second](https://b3n.org/engineering-wordpress-for-10000-visitors-per-second/)

[We handle 80TB and 5M page views a month for under $400 | Hacker News](https://news.ycombinator.com/item?id=29816504)
[How we handle 80TB and 5M page views a month for under $400 - Poly Haven Blog](https://blog.polyhaven.com/how-we-handle-80tb-and-5m-page-views-a-month-for-under-400/)

[Josh @ Overseer](https://engr.overseerlabs.io/clouds-containers-microservices-infra-and-architecture-from-100-devops-sre-surveys-cb636b1a1589)
Clouds, containers & microservices: infra and architecture from ~100 DevOps/SRE surveys

[Josh @ Overseer](https://engr.overseerlabs.io/fears-and-favorites-from-100-devops-sre-surveys-84a1365a9f18)
Fears and favorites from 100+ DevOps/SRE surveys

[Alex Aitken](https://www.alexaitken.nz/blog/sre-role-in-team/)
(2018) SRE role in team

[AJ Ross, Adrian Hilton, Dave Rensin](https://cloudplatform.googleblog.com/2017/01/availability-part-deux--CRE-life-lessons.html)
(2017) SLOs, SLIs, SLAs, oh my - CRE life lessons
for DevOps professionals / SRE

[upgundecha/howtheysre](https://github.com/upgundecha/howtheysre)
A curated collection of publicly available resources on how technology and tech-savvy organizations around the world practice Site Reliability Engineering (SRE)

[SRE Weekly](https://sreweekly.com/)
is a newsletter devoted to everything related to keeping a site or service available as consistently as possible.
SRE (Site/Service Reliability Engineering) isn’t just about automated failover or fault-tolerant architectures — although of course those are important.  It’s about a holistic view of reliability that takes into account everything from servers to human factors to processes to automation and more.

## SRE vs devops

[Asaf Yigal](https://devops.com/sre-vs-devops-false-distinction/)
(2017) SRE vs. DevOps — a False Distinction?

[Aymen El Amri](https://hackernoon.com/50-best-devops-sre-blog-posts-tutorials-of-2017-451a7d69c4ef)
(2018) 50 Best DevOps & SRE Blog Posts & Tutorials Of 2017

## story points

[Story points are pointless, measure queues | Hacker News](https://news.ycombinator.com/item?id=40969693)
[Story Points are Pointless, Measure Queues | Brightball](https://www.brightball.com/articles/story-points-are-pointless-measure-queues)

## supercomputers

[TOP500 Supercomputers](https://www.top500.org/)
shows the 500 most powerful commercially available computer systems known to us.

[CERN Data Centre](https://home.cern/science/computing)
3D visualizations of the CERN computing environments (and more).

## system monitoring

[Andrew Wulf](http://thecodist.com/article/monitor_or_fail)
Monitor Or Fail

[John Allspaw](http://www.kitchensoap.com/2007/09/26/the-term-monitoring-needs-clarification/)
(2007) The term “monitoring” needs clarification.

[Vivek Gite](https://www.cyberciti.biz/hardware/howto-see-historical-statistical-uptime-on-linux-server/)
Linux Server See the Historical and Statistical Uptime of System With tuptime Utility

[Netflix](https://medium.com/netflix-techblog/linux-performance-analysis-in-60-000-milliseconds-accc10403c55)
Linux Performance Analysis in 60,000 Milliseconds

## systems design

[I/O Is Faster Than CPU - Let's Partition Resources and Eliminate OS Abstractions [pdf] | Hacker News](https://news.ycombinator.com/item?id=19818899)
[I/O Is Faster Than the CPU - Let's Partition Resources and Eliminate (Most) OS Abstractions - parakernel-hotos19.pdf](https://penberg.org/parakernel-hotos19.pdf)
[Pekka Enberg](https://penberg.org/)

[Jesse Weaver](https://medium.com/s/story/a-simple-framework-for-designing-choices-ab93e0fc6610)
(2015) A Simple Framework for Designing Choices
No design is neutral

[System design and the cost of architectural complexity (2013) | Hacker News](https://news.ycombinator.com/item?id=35470905)
[System design and the cost of architectural complexity](https://dspace.mit.edu/handle/1721.1/79551)

## task management

[The server chose violence | Hacker News](https://news.ycombinator.com/item?id=40178652)
[The server chose violence - Cliffle](https://cliffle.com/blog/hubris-reply-fault/)

## uptime

[The Backrooms of the Internet Archive | Hacker News](https://news.ycombinator.com/item?id=40618079)
[The Backrooms of the Internet Archive | Internet Archive Blogs](https://blog.archive.org/2024/06/01/the-backrooms-of-the-internet-archive/)

## Vagrant

[CoreOS Docs](https://coreos.com/os/docs/latest/booting-on-vagrant.html)
Running CoreOS Container Linux on Vagrant

## web services

[Building a highly-available web service without a database | Hacker News](https://news.ycombinator.com/item?id=41206908)
[Building a highly-available web service without a database – Screenshotbot Blog](https://blog.screenshotbot.io/2024/08/10/building-a-highly-available-web-service-without-a-database/)

## decentralized

[GitHub - mjovanc/awesome-decentralized: A curated list of awesome projects, books, articles, tutorials, courses and other useful resources regarding decentralized technologies.](https://github.com/mjovanc/awesome-decentralized)

[GitHub - ong/awesome-decentralized-finance: A curated list of awesome decentralized finance projects](https://github.com/ong/awesome-decentralized-finance)

## devops

[Kevin London](https://www.kevinlondon.com/2016/09/19/devops-from-scratch-pt-1.html)
(2016) DevOps from Scratch, Part 1: Vagrant & Ansible
[Kevin London](https://www.kevinlondon.com/2016/09/20/devops-from-scratch-pt-2.html)
(2016) DevOps from Scratch, Part 2: Amazon & Terraform

[Pavan Belagatti](http://blog.shippable.com/devops-resources-top-5-devops-books-every-devops-enthusiast-must-read)
(2017) DevOps Resources: 5 Books Every DevOps Enthusiast Must Read!

[Matt Watson](https://stackify.com/15-metrics-for-devops-success/)
(2017) 15 Metrics for DevOps Success

[bregman-arie/devops-exercises](https://github.com/bregman-arie/devops-exercises)
Linux, Jenkins, AWS, SRE, Prometheus, Docker, Python, Ansible, Git, Kubernetes, Terraform, OpenStack, SQL, NoSQL, Azure, GCP, DNS, Elastic, Network, Virtualization

[Ask HN](https://news.ycombinator.com/item?id=16357368)
(2018) Which books describe modern devops?

[DevelopIntelligence Blog](http://www.developintelligence.com/blog/devops-for-non-technical-people/)
DevOps Simplified for Non-Technical People

[E.G. Nadhan](https://enterprisersproject.com/article/2017/5/9-key-phrases-devops)
(2017) 9 key phrases of DevOps

[Carlos Nunez](https://opensource.com/article/18/1/getting-devops)
(2018) How to get into DevOps

[Thomas Steinborn](https://opensource.com/article/18/1/future-devops)
(2018) The future of DevOps is mastery of multi-cloud environments

[Matt Watson](https://stackify.com/what-is-devops/)
(2017) What is DevOps? – Give Your Development Team Ownership

[DZone](https://dzone.com/guides/devops-culture-and-process)
(2018) [Book] DZone's free 50 pages Guide to DevOps: Culture and Process

[eon01/DevOpsLinks-Is-Awesome](https://github.com/eon01/DevOpsLinks-Is-Awesome)
curated list of useful resources for DevOps, SysAdmin and Full Stack Developers

[Maxime Choffat](https://mrrandol.github.io/devops_meetup_slides/index.html#/cover)
(2018) Slides of You said DevOps ? - Introduction to DevOps
[Meetup](https://www.meetup.com/fr-FR/Brussels-WeCraft-DevOps/events/246397252/)

[What is DevOps? DevOps Explained | Microsoft Azure](https://azure.microsoft.com/en-us/resources/cloud-computing-dictionary/what-is-devops#devops-overview)

[Tikam Singh Alma - DEV Community Profile](https://dev.to/tikam02)
[DevOps-Guide](https://github.com/Tikam02/DevOps-Guide)
DevOps Guide from basic to advanced with Interview Questions and Notes.

[A beginner's guide to building DevOps pipelines with open source tools | Opensource.com](https://opensource.com/article/19/4/devops-pipeline)

[GitHub - philemonnwanne/projects: I'll often come here to drop stuff about my Cloudy DevOps journey ✍🏾](https://github.com/philemonnwanne/projects)

[GitHub - milanm/DevOps-Roadmap: DevOps Roadmap for 2022. with learning resources](https://github.com/milanm/DevOps-Roadmap)

## devops roadmap

[Rocky Bhatia on LinkedIn: #cloud #devops #kubernetes #networking #rockybhatia | 252 comments](https://www.linkedin.com/posts/rocky-bhatia-a4801010_cloud-devops-kubernetes-activity-7074233926705119232-FIPo/)

## distributed systems - large scale

[The Four Innovation Phases of Netflix's Trillions Scale Real-time Data Infrastructure | by Zhenzhong Xu | Medium](https://zhenzhongxu.com/the-four-innovation-phases-of-netflixs-trillions-scale-real-time-data-infrastructure-2370938d7f01)

## software design principles

[My Principles for Building Software](https://kevinmahoney.co.uk/articles/my-principles-for-building-software)

[Ayooluwa Isaiah](https://freshman.tech/philosophy-of-software-design-summary/)
(2021) Book summary: A Philosophy of Software Design 

[Steve McConnell](http://stevemcconnell.com/articles/software-ten-essentials/)
(1997) Software’s Ten Essentials

[Steve Yegge](https://steve-yegge.blogspot.com/2007/01/pinocchio-problem.html)
(2007) The Pinocchio Problem
Great systems :
> * should never reboot (Rebooting is Dying). 
> * must be able to grow without rebooting.
> * Have a command shell.
> * Always have an extension language and a plug-in system (mods).
> * Are introspective.
> * Have to be a killer app, or they need one.

## SRE

[New Google SRE book: Building Secure and Reliable Systems | Hacker News](https://news.ycombinator.com/item?id=22815453)
[Books For Site Reliability Engineering](https://sre.google/books/)

[GitHub - linkedin/school-of-sre: At LinkedIn, we are using this curriculum for onboarding our entry-level talents into the SRE role.](https://github.com/linkedin/school-of-sre)
[LinkedIn](https://linkedin.github.io/school-of-sre/)
School of SRE : LinkedIn, uses this curriculum for onboarding their entry-level talents into the SRE role.

[Google - Site Reliability Engineering](https://sre.google/sre-book/eliminating-toil)

[GitHub - dastergon/awesome-sre: A curated list of Site Reliability and Production Engineering resources.](https://github.com/dastergon/awesome-sre)

[Google](https://landing.google.com/sre/book.html)
[Book] Site Reliability Engineering
free book about how SRE at Google build, deploy, monitor, and maintain some of the largest software systems in the world.

[New Relic](https://newrelic.com/resource/site-reliability-engineering)
[Book] Site Reliability Engineering
Philosophies, Habits, and Tools for SRE Success

[Matt Watson](https://stackify.com/site-reliability-engineering/)
(2017) What Is Site Reliability Engineering and Why You Should Embrace It

[Krishelle Hardson-Hurley](https://hackernoon.com/so-you-want-to-be-an-sre-34e832357a8c)
(2017) So you want to be an SRE?

## staging environments

[Alice Goldfuss](https://increment.com/development/center-stage-best-practices-for-staging-environments/)
(2017) Center stage: Best practices for staging environments

## sysadmin

[DigitalOcean](https://www.digitalocean.com/community/tutorials)
development and sysadmin tutorials.

[GitHub - trimstray/test-your-sysadmin-skills: A collection of Linux Sysadmin Test Questions and Answers. Test your knowledge and skills in different fields with these Q/A.](https://github.com/trimstray/test-your-sysadmin-skills)

[Stephan Zielinski](http://www.stokely.com/lighter.side/sysadm.field.guide.html)
Know Your UNIX System Administrator: A Field Guide

[Ramesh Natarajan](https://www.thegeekstuff.com/2010/12/50-unix-linux-sysadmin-tutorials/)
(2010) 50 UNIX / Linux Sysadmin Tutorials

[Show HN: Linux sysadmin course, eight years on | Hacker News](https://news.ycombinator.com/item?id=24380969)
[GitHub - livialima/linuxupskillchallenge: Learn the skills required to sysadmin a remote Linux server from the commandline.](https://github.com/livialima/linuxupskillchallenge)
learn the skills required to sysadmin.

[GitHub - snori74/linuxupskillchallenge: Learn the skills required to sysadmin a remote Linux server from the commandline.](https://github.com/snori74/linuxupskillchallenge)

[How can you build a strong team in system administration?](https://www.linkedin.com/comm/advice/3/how-can-you-build-strong-team-system-administration-4nkac)

## systems design

[Systems design explains the world: volume 1 | Hacker News](https://news.ycombinator.com/item?id=25552267)
[Systems design explains the world: volume 1 - apenwarr](https://apenwarr.ca/log/20201227)
- this may be an interesting pattern, or technical idiocy

[GitHub - donnemartin/system-design-primer: Learn how to design large-scale systems. Prep for the system design interview. Includes Anki flashcards.](https://github.com/donnemartin/system-design-primer)
Learn how to design large-scale systems. Prep for the system design interview.
:star:

[GitHub - prasadgujar/low-level-design-primer: Dedicated Resources for the Low-Level System Design. Learn how to design and implement large-scale systems. Prep for the system design interview.](https://github.com/prasadgujar/low-level-design-primer)

## systems engineering

[GitHub - kktse/awesome-systems-engineering: A collection of resources about systems engineering and its practice - pull requests welcome!](https://github.com/kktse/awesome-systems-engineering)

[System Design Interview Cheatsheet | Hacker News](https://news.ycombinator.com/item?id=11516923)
[System Design Cheatsheet](https://gist.github.com/vasanthk/485d1c25737e8e72759f)

## web ops

[Matt Watson](https://stackify.com/web-operations/)
(2017) What is Web Operations? How Does it Relate to DevOps and SRE?

## post-mortem

[What is a Software Post-Mortem and How Do You Write One?](https://www.freecodecamp.org/news/what-is-a-software-post-mortem)

## systems design

[Systems Design for Advanced Beginners | Hacker News](https://news.ycombinator.com/item?id=23904000)
[Systems design for advanced beginners | Robert Heaton](https://robertheaton.com/2020/04/06/systems-design-for-advanced-beginners/)

## Ansible

[Ansible](https://www.ansible.com/videos-ansible-automates-2017)
(2017) Ansible Automates Videos

[Timothy Appnel - Ansible Best Practices: The Essentials.](https://www.ansible.com/blog/ansible-best-practices-essentials)
[Timothy Appnel - Ansible Best Practices: The Essentials.](https://www.ansible.com/videos-ansible-automates-ansible-best-practices-the-essentials)

[enginyoyen/ansible-best-practises](https://github.com/enginyoyen/ansible-best-practises)
A project structure that outlines some best practices of how to use ansible

[Pierre Baillet](http://blog.ippon.tech/ansible-tips-and-tricks/)
10 Ansible tips and tricks

[Timothy Appnel, James Martin - Ansible best practices for startups to enterprises](https://www.redhat.com/en/about/videos/ansible-best-practices-startups-enterprises)

[C.J. Scarlett aka Scarlz](http://www.tricksofthetrades.net/2017/03/20/ansible-adhoc-modules/)
(2017) Tricks of the Trades : Ansible - Ad Hoc Commands and Modules

[Ansible](https://www.ansible.com/blog/ansible-performance-tuning)
Ansible Performance Tuning (for Fun and Profit)

[Remy van Elst](https://raymii.org/s/tutorials/Ansible_-_Only_if_a_file_exists_or_does_not_exist.html)
Ansible - Only if a file exists or does not exist

[Jens Depuydt](http://jensd.be/587/linux/tips-tricks-for-ansible)
Tips & tricks for Ansible

[Maxim Chernyak](http://hakunin.com/six-ansible-practices)
6 practices for super smooth Ansible experience
[Maxim Chernyak](http://hakunin.com/six-ansible-practices#avoid-perpetually-changed-and-skipping-tasks)
Avoid perpetually “changed” and “skipping” tasks

[Justin Ellingwood](https://www.digitalocean.com/community/tutorials/how-to-manage-multistage-environments-with-ansible)
How to Manage Multistage Environments with Ansible

[Stack Overflow](https://stackoverflow.com/questions/32526774/multistage-deployment-with-ansible)
Multistage deployment with ansible

[Osvaldo Toja](http://toja.io/using-host-and-group-vars-files-in-ansible/)
Organizing Group Vars Files in Ansible

[Ross Tuck](http://rosstuck.com/multistage-environments-with-ansible/)
Multistage environments with Ansible

[Maxime Thoonsen](https://www.theodo.fr/blog/2015/10/best-practices-to-build-great-ansible-playbooks/)
(2015) Best practices to build great Ansible playbooks

[Raphael Campardou](https://reinteractive.com/posts/167-ansible-real-life-good-practices)
Ansible (Real Life) Good Practices

[Deni Bertović](https://goodcode.io/articles/ansible-tips/)
Ansible tips

[Marlon Bernardes](http://codeheaven.io/15-things-you-should-know-about-ansible/)
15 Things You Should Know About Ansible

[Dan Tehranian](https://dantehranian.wordpress.com/2015/08/10/automating-linux-security-best-practices-with-ansible/)
(2015) Automating Linux Security Best Practices with Ansible

[Andreas Sommer](https://andidog.de/blog/2017-04-24-ansible-best-practices)
Ansible best practices
:star:

[Stack Exchange](https://devops.stackexchange.com/a/706/3072)
How to test provisioning and configuration in Ansible setup?
[Stack Exchange](https://devops.stackexchange.com/questions/98/how-to-test-provisioning-and-configuration-in-ansible-setup)
(2017) How to test provisioning and configuration in Ansible setup? Solutions : Goss, Testinfra, Serverspec, Inspec

[Pedro Artino](https://velenux.wordpress.com/2017/07/31/ansible-how-to-skip-a-specific-host-or-group-in-a-playbook/)
(2017) Ansible: how to skip a specific host or group in a playbook

[GitHub - mikeroyal/Ansible-Guide: Ansible Guide](https://github.com/mikeroyal/Ansible-Guide)

[ansible-community/awesome-ansible: Awesome Ansible List](https://github.com/ansible-community/awesome-ansible)

[jdauphant/awesome-ansible](https://github.com/jdauphant/awesome-ansible)
A collaborative curated list of awesome Ansible resources

[Jeff Geerling](https://www.jeffgeerling.com/blog/2017/get-started-using-ansible-awx-open-source-tower-version-one-minute)
(2017) Get started using Ansible AWX (Open Source Tower version) in one minute

[pmarkham/writing-ansible-modules-in-bash](https://github.com/pmarkham/writing-ansible-modules-in-bash/blob/master/ansible_bash_modules.md)
Writing Ansible Modules in Bash

[Jeff Geerling](https://www.jeffgeerling.com/blog/automating-your-automation-ansible-tower)
(2015) Automating Your Automation with Ansible Tower

[Jakub Skałecki](https://rock-it.pl/managing-multiple-environments-with-ansible-best-practices/)
(2017) Managing multiple environments with Ansible - best practices

[Jonathan Lozada De La Matta (Red Hat)](https://opensource.com/article/18/7/sysadmin-tasks-ansible)
(2018) A sysadmin's guide to Ansible: How to simplify tasks

[Kat Dober](https://blog.newrelic.com/engineering/ansible-best-practices-guide/)
(2018) New to Ansible? Check Out Our Best Practices Guide

[C.J. Scarlett aka Scarlz](https://www.tricksofthetrades.net/2017/10/02/ansible-local-playbooks/)
(2017) Ansible - Local Playbook Execution

## Ansible - testing and debugging

[Roland Wolters](https://liquidat.wordpress.com/2016/02/25/howto-keeping-temporary-ansible-scripts/)
(2016) Keeping temporary Ansible scripts

## Ansible Vault

[Dan Tehranian](https://dantehranian.wordpress.com/2015/07/24/managing-secrets-with-ansible-vault-the-missing-guide-part-1-of-2/)
(2015) Managing Secrets with Ansible Vault – The Missing Guide (Part 1 of 2)
[Dan Tehranian](https://dantehranian.wordpress.com/2015/07/24/managing-secrets-with-ansible-vault-the-missing-guide-part-2-of-2/)
(2015) Managing Secrets with Ansible Vault – The Missing Guide (Part 2 of 2)

[Marvin Pinto](https://disjoint.ca/til/2016/04/25/using-git-diff-with-ansible-vault-encrypted-files/)
(2016) Using git diff with Ansible Vault encrypted files

[Tristan Fisher](https://gist.github.com/tristanfisher/e5a306144a637dc739e7)
Working with ansible-vault : A short tutorial on how to use Vault in your Ansible workflow

## anticipating load

[The C10K problem](http://www.kegel.com/c10k.html)
it's time for web servers to handle ten thousand clients simultaneously, don't you think?

## CDNs

[What is a CDN? How do CDNs work? | Hacker News](https://news.ycombinator.com/item?id=34690656)

[Image and Video Upload, Storage, Optimization and CDN](https://cloudinary.com/)
[GitHub - Developerayo/awesome-cloudinary: A curated list of awesome resources : books, videos, articles about getting started and using Cloudinary (A comprehensive cloud-based image and video management platform)](https://github.com/Developerayo/awesome-cloudinary)

## cgroups

[A Linux sysadmin's introduction to cgroups | Hacker News](https://news.ycombinator.com/item?id=25008941)
[A Linux sysadmin's introduction to cgroups | Enable Sysadmin](https://www.redhat.com/sysadmin/cgroups-part-one)

## chaos engineering

[GitHub - dastergon/awesome-chaos-engineering: A curated list of Chaos Engineering resources.](https://github.com/dastergon/awesome-chaos-engineering)

[Principles of Chaos Engineering](http://principlesofchaos.org/)

[Krishnan Subramanian](https://www.cloudave.com/11973/designing-for-failure-some-key-facts/)
Designing For Failure: Some Key Facts

## chatops

[Jaikumar Vijayan](https://techbeacon.com/how-securely-scale-chatops-enterprise)
How to securely scale ChatOps in the enterprise

[Oded Zilinsky](https://techbeacon.com/how-use-chatops-boost-business-engagement-across-teams)
(2018) How to use ChatOps to boost business engagement across teams
Go cross-silo with chatbots

## decentralized networks - activitypub

[ActivityPub - Wikipedia](https://en.wikipedia.org/wiki/ActivityPub)

## design patterns - js

[JavaScript Design Patterns - Explained with Examples](https://www.freecodecamp.org/news/javascript-design-patterns-explained)

## design patterns

[Design Patterns for Modern Backend Development - with Example Use Cases](https://www.freecodecamp.org/news/design-pattern-for-modern-backend-development-and-use-cases)

[GitHub - DovAmir/awesome-design-patterns: A curated list of software and architecture related design patterns.](https://github.com/DovAmir/awesome-design-patterns)

[Google Cloud Architecture Center](https://cloud.google.com/architecture/scalable-and-resilient-apps)
Patterns for scalable and resilient apps 

[iOSDesignPatternSamples](https://github.com/marty-suzuki/iOSDesignPatternSamples)
GitHub user search app with variety of design patterns

[The Design Patterns for Distributed Systems Handbook - Key Concepts Every Developer Should Know](https://www.freecodecamp.org/news/design-patterns-for-distributed-systems)

[4 Design Patterns You Should Know for Web Development: Observer, Singleton, Strategy, and Decorator](https://www.freecodecamp.org/news/4-design-patterns-to-use-in-web-development)

[GitHub - DovAmir/awesome-design-patterns: A curated list of software and architecture related design patterns.](https://github.com/DovAmir/awesome-design-patterns)

[GitHub - kamranahmedse/design-patterns-for-humans: An ultra-simplified explanation to design patterns](https://github.com/kamranahmedse/design-patterns-for-humans)

## domain-driven design

[GitHub - heynickc/awesome-ddd: A curated list of Domain-Driven Design (DDD), Command Query Responsibility Segregation (CQRS), Event Sourcing, and Event Storming resources](https://github.com/heynickc/awesome-ddd)

## financial systems

[Engineering principles for building financial systems | Hacker News](https://news.ycombinator.com/item?id=40933110)
[Engineering Principles for Building Financial Systems](https://substack.wasteman.codes/p/engineering-principles-and-best-practices)

[GitHub - kdeldycke/awesome-billing: 💰 Billing & Payments knowledge for cloud platforms](https://github.com/kdeldycke/awesome-billing)

## Hashicorp Vault

[Vault Docs](https://www.vaultproject.io/intro/getting-started/deploy.html)
Deploy Vault

[Aun Raza](https://linoxide.com/how-tos/secure-secret-store-vault/)
How to Securely Store Passwords and Api Keys Using Vault

[Katacoda](https://www.katacoda.com/courses/docker-production/vault-secrets)
Interactive Course : Docker in Production - Store Secrets using HashiCorp Vault

[Vyacheslav Voronenko](https://www.codementor.io/slavko/how-to-install-vault-hashicorp-secure-deployment-secrets-du107xlqd)
Using Vault to Secure Your Deployment Secrets

[Seth Vargo](https://www.hashicorp.com/blog/codifying-vault-policies-and-configuration/)
Codifying Vault Policies and Configuration

[Martin Rusev](https://web.archive.org/web/20170118081713/https://www.amon.cx/blog/managing-all-secrets-with-vault/)
(2016) Managing all your secrets with Vault - Review and Walkthrough

## Hashicorp Vault+Openshift

[Raffaele Spazzoli](https://blog.openshift.com/managing-secrets-openshift-vault-integration/)
Managing Secrets on OpenShift – Vault Integration

## Jenkins

[Hanxue Lee](http://flummox-engineering.blogspot.com/2016/01/installing-jenkins-os-x-homebrew.html)
(2016) Installing Jenkins on OS X using Homebrew

[Phu Ha](http://blog.asg-service.net/post/continuous-integration-part-1-setting-up-vms-docker-and-jenkins/)
Continuous Integration: Part 1 - Setting Up VMs, Docker, and Jenkins
[Phu Ha](http://blog.asg-service.net/post/continuous-integration-part-2-setup-a-jenkins-slave-docker-registry-jenkinsfile/)
Continuous Integration: Part 2 - Setup a Jenkins Slave, Docker Registry, and Jenkinsfile (Pipeline)

## microservices

[Sumit Maingi](https://cloudncode.blog/2016/07/22/msa-getting-started/)
(2016) Building Microservices? Here is what you should know

## microservices vs monolith

[Microservices vs Monoliths: Benefits, Tradeoffs, and How to Choose Your App's Architecture](https://www.freecodecamp.org/news/microservices-vs-monoliths-explained/)

## network segmentation

[GitHub - sergiomarotco/Network-segmentation-cheat-sheet: Best practices for segmentation of the corporate network of any company](https://github.com/sergiomarotco/Network-segmentation-cheat-sheet)

## NGINX

[Cody Parker](https://codyparker.com/force-entire-site-ssl-nginx-behind-aws-load-balancer/)
(2017) How To Force HTTPS in NGINX behind a classic AWS Load Balancer

[Avoiding the top Nginx configuration mistakes | Hacker News](https://news.ycombinator.com/item?id=30435282)
[Avoiding the Top 10 NGINX Configuration Mistakes - NGINX](https://www.nginx.com/blog/avoiding-top-10-nginx-configuration-mistakes/)

[The NGINX Handbook - Learn NGINX for Beginners](https://www.freecodecamp.org/news/the-nginx-handbook)

## observability and monitoring

[Charity Majors aka mipsytipsy](https://honeycomb.io/blog/2017/11/best-practices-for-observability/)
(2017) Best Practices for Observability

[Matt Watson](https://stackify.com/cloud-monitoring-vs-server-monitoring/)
(2017) 6 Reasons Cloud Monitoring Is Different Than Server Monitoring

## Openshift

[OpenShift](https://www.openshift.com/container-platform/resources.html)
Learning Resources (webinars, datasheets, whitepapers, infographic, tools, videos...)

[OpenShift](https://blog.openshift.com/openshift-v3-deep-dive-docker-kubernetes/)
OpenShift V3 Deep Dive Tutorial
The Next Generation of PaaS

[Laurent Broudoux](https://blog.openshift.com/multiple-deployment-methods-openshift/)
Multiple Deployment Methods for OpenShift

[oscp/awesome-openshift3](https://github.com/oscp/awesome-openshift3)
Awesome Openshift 3 resources

[OpenShift Interactive Learning Portal](https://learn.openshift.com/)
Interactive learning scenarios. Can be used for experimentation

[OpenShift](https://www.openshift.com/devops-with-openshift/)
[Book] DevOps with OpenShift
[OpenShift](https://www.openshift.com/promotions/devops-with-openshift.html)
[Book] DevOps with OpenShift

## postmortems

[What is the difference between RPO, RTO, and MTD? - Tandem](https://tandem.app/blog/what-is-the-difference-between-rpo-rto-mtd)

[Gregg Caines](http://caines.ca/blog/2015/03/08/reclaiming-value-from-bugs-and-outages/)
(2015) Reclaiming Value From Bugs and Outages: Thoughts on Post-Mortems

## premortems

[Gary Klein](https://hbr.org/2007/09/performing-a-project-premortem)
(2007) Performing a Project Premortem

## profiling

[poor man's profiler](http://poormansprofiler.org/)
like dtrace's don't really provide methods to see what programs are blocking on.

## Prometheus - go

[Alex Dzyoba](https://alex.dzyoba.com/blog/go-prometheus-service/)
(2018) Instrumenting a Go service for Prometheus

## relay server

[NoSuchCon - Press](https://www.nosuchcon.org/stream.html)

## RTOS

[Real-time operating system - Wikipedia](https://en.wikipedia.org/wiki/Real-time_operating_system)

## search engine - Amazon_Elasticsearch

[Guide to running Elasticsearch in production | Hacker News](https://news.ycombinator.com/item?id=22396918)
[In depth guide to running Elasticsearch in production - TechNotes](https://web.archive.org/web/20200225115308/https://facinating.tech/2020/02/22/in-depth-guide-to-running-elasticsearch-in-production/)

[GitHub - dzharii/awesome-elasticsearch: A curated list of the most important and useful resources about elasticsearch: articles, videos, blogs, tips and tricks, use cases. All about Elasticsearch!](https://github.com/dzharii/awesome-elasticsearch)

## search engine

[Search User Interfaces](https://www.searchuserinterfaces.com/)

[How to create your OWN search engine and find the cool stuff in this sub ? : opendirectories](https://old.reddit.com/r/opendirectories/comments/d3w2fu/how_to_create_your_own_search_engine_and_find_the/)

## serverless

[GitHub - puresec/awesome-serverless-security: A curated list of awesome serverless security resources such as (e)books, articles, whitepapers, blogs and research papers.](https://github.com/puresec/awesome-serverless-security)

## services engineering

[mmcgrana/services-engineering](https://github.com/mmcgrana/services-engineering)
A reading list for services engineering, with a focus on cloud infrastructure services.

## software architectures - 11

[Software Architecture Patterns: 5 minute read | Hacker News](https://news.ycombinator.com/item?id=29024767)
[Software Architecture Patterns: 4 minute read | by Orkhan Huseynli | Sep, 2021 | Medium | Medium](https://orkhanscience.medium.com/software-architecture-patterns-5-mins-read-e9e3c8eb47d2)

[The Software Architecture Handbook](https://www.freecodecamp.org/news/an-introduction-to-software-architecture-patterns)

[GitHub - mhadidg/software-architecture-books: A comprehensive list of books on Software Architecture.](https://github.com/mhadidg/software-architecture-books)

[FMC - Home of Fundamental Modeling Concepts](http://fmc-modeling.org)

[Software Architecture Guide | Hacker News](https://news.ycombinator.com/item?id=20786448)
[Software Architecture Guide](https://martinfowler.com/architecture/)

[booknotes/architecture/clean-architecture at master · preslavmihaylov/booknotes · GitHub](https://github.com/preslavmihaylov/booknotes/tree/master/architecture/clean-architecture)

[GitHub - tekiegirl/SoftwareArchitectureResources: A collection of resources for supporting and learning about software architecture](https://github.com/tekiegirl/SoftwareArchitectureResources)

[Introduction - Architecture Playbook](https://nocomplexity.com/documents/arplaybook/introduction.html)
[Business Architecture - Architecture Playbook](https://nocomplexity.com/documents/arplaybook/businessarchitecture.html)

[GitHub - mehdihadeli/awesome-software-architecture: A curated list of awesome articles, videos, and other resources to learn and practice software architecture, patterns, and principles.](https://github.com/mehdihadeli/awesome-software-architecture)

[GitHub - simskij/awesome-software-architecture: A curated list of resources on software architecture](https://github.com/simskij/awesome-software-architecture)

[Web Architecture 101](https://engineering.videoblocks.com/web-architecture-101-a3224e126947)
the basic architecture concepts.

## software architectures - diagrams

[Solutions Architect Tips - The 5 Types of Architecture Diagrams | Ready, Set, Cloud!](https://www.readysetcloud.io/blog/allen.helton/the-5-types-of-architecture-diagrams)

[Architecture diagrams should be code | Hacker News](https://news.ycombinator.com/item?id=34322130)
[Architecture diagrams should be code - BAM Weblog](https://brianmckenna.org/blog/architecture_code)

[How to draw software architecture diagrams (2022) | Hacker News](https://news.ycombinator.com/item?id=38035505)
[How to draw beautiful software architecture diagrams](https://terrastruct.com/blog/post/draw-software-architecture-diagrams/)

[The C4 model for visualising software architecture (2017) | Hacker News](https://news.ycombinator.com/item?id=37974021)
[The C4 model for visualising software architecture](https://c4model.com/)
consists of a hierarchical set of software architecture diagrams for context, containers, components, and code.

[How to review a software architecture diagram - DEV Community](https://dev.to/simonbrown/how-to-review-a-software-architecture-diagram-6p0)

## Splunk

[Splunk Docs](http://dev.splunk.com/view/logging-best-practices/SP-CAAAFCK)
Logging best practices.
[Overview of Splunk logging for Java](http://dev.splunk.com/view/splunk-logging-java/SP-CAAAE2K)

## system monitoring

[Justyna Ilczuk](http://tinystruggles.com/2015/03/22/bash-monitoring-tips.html)
(2015) Bash monitoring tips - watch

[Steven Vaughan-Nichols](https://insights.hpe.com/articles/16-linux-server-monitoring-commands-you-really-need-to-know-1703.html)
16 Linux server monitoring commands you really need to know
