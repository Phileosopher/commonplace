
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

[The CI/CD Handbook: Learn Continuous Integration and Delivery with GitHub Actions, Docker, and Google Cloud Run](https://www.freecodecamp.org/news/learn-continuous-integration-delivery-and-deployment/)
[How to Build a Weather App with R Shiny](https://www.freecodecamp.org/news/how-to-build-a-weather-app-with-r-shiny/)

[The Microservices Book – Learn How to Build and Manage Services in the Cloud](https://www.freecodecamp.org/news/the-microservices-book-build-and-manage-services-in-the-cloud/)

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
