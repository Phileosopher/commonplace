
# Risk management for information security

The more complexity in the system, the more risks inherent to the system, since it creates more [attack vectors](cs-infosec-pentest.md). To manage this, [CIA security systems](cs-infosec.md) use layers:

1. [Organization](cs-infosec-compliance.md): security strategy, disaster recovery, security auditing, risk assessment, security policies, legal compliance
2. [Network](cs-networks.md): [authentication methods](cs-infosec-authentication.md), routers, proxy/VPN servers, IDS, firewalls, [encryption](encryption.md) of transmitted information
3. Application: more authentication, [user roles and accounts](cs-infosec-permissions.md), data encryption
4. End user: security education, more authentication methods, antivirus software, more data encryption

Since it's absolutely impossible to track every risk, there's a simple-enough structure to assess if that risk is worth the work:

1. Examine all possible vulnerabilities, which are things with some asset value that could be easily exploited.
2. Examine all threats, internal and external, that could use those vulnerabilities. This includes malicious and accidental, with some indication of the threat actor or threat vector.
3. The risk is the likelihood of the exploit, multiplied by the impact it would have on all affected systems.

## Principles

NIST created its Risk Management Framework (RMF) to put [risk management](safety-riskmgmt.md) systems in place and test to be sure they work:

1. Prepare - everyone should [be aware](mind-awareness.md) changes will be happening.
2. Categorize - [organize](organization.md) how the system processes, stores, and transmits information and conduct a risk assessment.
3. Select - choose the controls that will protect the system based on the risk assessment.
4. Implement - carry out the controls and document what happens.
5. Assess - examine if the controls are in place, operating as intended, and creating desired results.
6. Authorize - the group leader makes a risk-based decision to authorize the system to operate.
7. Monitor - continuously monitor the implementation, as well as any further risks to the system.

Broadly, the collective system that protects the computers is called Unified Threat Management (UTM), and it will use eight major principles:

- Least privilege: limit access to only what's necessary to do something.
- Fail-safe defaults: deny access to things by default.
- Economy of mechanism: keep things simple to reduce errors.
- Complete mediation: use the same information access rules every single time something is accessed.
- Open design: keep the design open to allow accountability by good faith actors.
- Separation of privilege: restrict all unilateral access.
- Least common mechanism: whenever possible, don't share resources.
- Psychological acceptability: people need to accept the system or they'll circumvent it.

Altogether, this constitutes a zero-trust model:

- [Authenticate](cs-infosec-authentication.md) before processing
- [Encrypt](encryption.md) before transmitting
- Use end-to-end security
- Deprecate weak authentication and encryption
- Keep the computers updated
- Never share accounts, use generic accounts like "admin", or give anonymous access

In practice, it represents a few things as a full-time job:

1. Get baselines for how everything is running normally.
2. Make sure everything is installed, updated, or deactivated correctly.
3. Educate everyone in the organization to be sure they're educated.
4. Conduct constant security audits.

## Frequent attack vectors

The weakest link in every single cybersecurity system are the employees:

- Unlike computers, [humans](humanity.md) make non-deterministic mistakes all the time.
- When they're performing a [habitual](habits.md) task, they're often [unaware](mind-awareness.md) of what's going on.
- They are the most susceptible to [social engineering](cs-infosec-socialengineering.md).

In practice, the ubiquity of people on their smartphones means mobile device management in many organizations becomes the largest attack surface.

- The policies can range from Bring Your Own Device (BYOD) to Corporate Owned Business Only (COBO), and can include Corporate Owned Personally Enabled (COPE) and Choose Your Own Device (CYOD).
- To keep track of everything, organizations usually use Mobile Device Management (MDM) software over a network.

While it's more affordable and productive to have a "bring your own device" (BYOD) strategy, that policy opens up a wider attack surface from all the varieties of factors that can't be controlled.

- At that point, expert security professionals will retreat to emphasizing network and app security.

## Preventing access

Most computer systems employ some form of countermeasure through Intrusion Detection Systems and Intrusion Prevention Systems (IDS/IPS).

- In practice, it's basically a packet sniffer with carefully crafted rules about what to do next.
  - The artistry of good cybersecurity is often in IDS/IPS configs.
- The reason IDS is still used is because many security systems can yield false-positives and make life difficult if someone is locked out entirely from access.
- The IDS can be host-based or network-based, depending on security needs.

More information means more risk, so it's wisest to destroy legitimately useless information whenever possible.

- Formatting and destroying unused disks is critical.
  - When formatting, clear the MBR as well (which can often be done through the "fdisk /MBR" command).
  - If you're not outright destroying the data, zero out all the data by clearing it with multiple passes. Traditionally, 7 passes was the standard, but that was when [storage](cs-memory.md) was magnetic hard drives, so it may not need that many.

## Practical realities

Generally, since some of the measures can cost a lot of money and don't affect profitability directly, most companies won't invest in a risk management solution until they learn the hard way.

- However, a well-maintained infosec policy can be more effective at protecting an organization than an [insurance policy](money-insurance.md).
