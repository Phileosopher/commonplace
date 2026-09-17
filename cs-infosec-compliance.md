
# Large-scale infosec compliance

To keep computers safe across an organization, information security professionals uses a Governance, Risk, and Compliance (GRC) framework to create and manage processes within an organization.

## Risk Management

NIST created its Risk Management Framework (RMF) to put [risk management](safety-riskmgmt.md) systems in place and test to be sure they work:

1. Prepare - everyone should [be aware](mind-awareness.md) changes will be happening.
2. Categorize - [organize](organization.md) how the system processes, stores, and transmits information and conduct a risk assessment.
3. Select - choose the controls that will protect the system based on the risk assessment.
4. Implement - carry out the controls and document what happens.
5. Assess - examine if the controls are in place, operating as intended, and creating desired results.
6. Authorize - the group leader makes a risk-based decision to authorize the system to operate.
7. Monitor - continuously monitor the implementation, as well as any further risks to the system.

Generally, since some of the measures can cost a lot of money and don't affect profitability directly, most companies won't invest in a risk management solution until they learn the hard way.

- However, a well-maintained infosec policy can be more effective at protecting an organization than an [insurance policy](money-insurance.md).

The weakest link in every single cybersecurity system are the employees:

- Unlike computers, [humans](humanity.md) make non-deterministic mistakes all the time.
- When they're performing a [habitual](habits.md) task, they're often [unaware](mind-awareness.md) of what's going on.
- They are the most susceptible to [social engineering](cs-infosec-socialengineering.md).

While it's more affordable and productive to have a "bring your own device" (BYOD) strategy, that policy opens up a wider attack surface from all the varieties of factors that can't be controlled.

- At that point, expert security professionals will retreat to emphasizing network and app security.

## Background verification

To ensure a trustworthy system, all users must sign Acceptable Use Policies (AUPs) as a prerequisite to accessing anything.

- The more public presence an organization has, the more that users, groups, and even entire websites or IP address ranges must be routinely blocked.
- Most of these verifications arise through robust background checks, which usually require trusting another organization entirely for their validation of someone's background.

## Threat modeling

With enough skill and education, a skilled cybersecurity professional can stop most [PenTesting](cs-infosec-pentest.md) efforts.

1. They create "threat models" of how a PenTester will attack.
2. They test that threat model by giving the work off to a "red team" while they play the role of "blue team".
3. Then, they'll constantly improve their efforts to block off the red team.

However, it's impossible to stop everything, *something* will fail, and *someone* will gain access.

- To that end the best threat modeling also assumes the system will inevitably get hacked, and should have a means to mitigate damage:
  - Lead to specific information that's useless but seems legitimate without further inspection.
  - Have a hard limit on data requests (e.g., only 1,000 emails per email address per day).
  - Send information about anything suspicious, even if it may be benign.

Further, there's always the possibility of the blue team being incapacitated, which should have conditions only present if the person or system is dead, disappeared, or was disabled (3D system):

- It could be associated to something constantly updating, such as a heart rate monitor or RSS feed.
- It may be a trigger that only activates if someone isn't routinely validating something (e.g., once a week).
- Either way, that type of system permits other people to later act with more information.

One of the most profound uses of [machine learning](cs-ai-ml.md) comes through more easily training the data on normal behavior within an organization. After the model is trained on typical user access and behaviors, it can *very* easily find odd behaviors that deviate from that norm.

However, things are guaranteed to still slip through, so the best policy is to *assume* compromised systems, then create policies assuming those events will happen.

- The legality and safety of the organization can often sit on the nuanced difference in IP address or choice of [protocol](cs-standards.md).
- In other words, assume the "disaster recovery plan" *will* be used.

All of these security policies must be subject to security audits to be sure they actually work. Further, when an event happens, there's plenty of [bureaucracy](bureaucracy.md) in following up and documenting everything that happened.

## Laws and standards

There is a unique culture within cybersecurity composed of two types of people:

1. Red team [penetration testers](cs-infosec-pentest.md) who have a [crime-adjacent career](https://gainedin.site/crime) and are often borderline [anarchists](politics-systems.md)
2. Blue team policy-making enforcers who are a hybrid of [bureaucrat](bureaucracy.md) and [police officer](legal-crimes.md)

Altogether, it creates a synergy of many, many rules.

- Large organizations have to have *absurd* rules in place to prevent any unauthorized use.
- It is entirely common for a policy to be so severe that someone can't use a company-issued flash drive to move a file from a company computer to another company computer next to it.
- This is necessary, however, to prevent the risks of unauthorized use.

Beyond this, there are many [government rules](people-rules.md) that require region-specific compliance:

- European Union
  - General Data Protection Regulation (GDPR): connected largely with data privacy and [user consent](people-contracts.md)
  - European Union—United States Privacy Shield: US standards for EU data protection requirements
- United States
  - Federal Information Security Modernization Act (FISMA): government-related
  - [Money](money-accounting.md)-related
    - Sarbanes-Oxley (SOX)
    - Bank Secrecy Act of 190
  - Family Educational Rights and Privacy Act (FERPA): [student](education.md)-based
  - Foreign Corrupt Practices Act: foreign activities against the interests of the USA
  - Privacy-related
    - Fair Credit Reporting Act (1970), specifically about [credit-worthiness](money-2_debt.md)
      - Fair and Accurate Credit Transactions Act (2003), an amendment to the FCRA
    - Right to Financial Privacy Act (1978), specifically about the government looking at financial information
    - Gramm-Leach-Bliley Act, specifically about financial information
    - Health Insurance Portability and Accountability Act (HIPAA): [healthcare](body-health.md)-related
      - The American Recovery and Reinvestment Act (2009) added to HIPAA, specifically Title XIII-D
    - Family Educational Rights and Privacy Act (1974), specifically for parents' release of children's educational records
    - Children’s Online Privacy Protection Act (1998), specifically for offering services specifically to minors that collect their personal information
    - Omnibus Crime Control and Safe Streets Act (1968 and amended 1986) Title III, specifically about the government intercepting spoken communications
- [Standardization groups](standards.md)
  - Payment Card Industry Data Security Standard (PCI DSS): financial transaction-related

There are far too many to count, and many of these require certifications, which is why cybersecurity requires an endless pursuit of more certifications than just about every other possible job.

Among these standards, the US National Institute of Standards and Technology (NIST) created a five-section set of standards called the Cybersecurity Framework (CSF):

- Identify: seeing where an attack may happen
- Protect: measures to prevent an attack
- Detect: for when someone is [actively attacking](cs-infosec-pentest.md)
- Respond: for when things fail or are stolen, to act to mitigate the damage
- Recover: for when things fail or are stolen, to bring things back online

## Risks from Rules

Managing [cybersecurity](cs-infosec.md) for large organizations is vastly complicated compared with [individually-focused security](safety-security.md).

Individually managing permissions and configurations becomes more difficult across [a group of people](groups-small.md), for several reasons:

- Each group consists of a variety of people, and the weakest computer or least-tech-savvy user is the highest risk for the organization.
- A group draws more attention than an individual, proportionally to its popularity, creating more desire for hackers to infiltrate it.
- Groups are often subject to more [regional government laws](legal-safety.md) than individuals.
- If the organization is spread across multiple regions, completely legal actions in one region could imprison someone for life in another.

While every increase in a cybersecurity policy decreases the risk of damage, it comes with multiple secondary risks:

1. Authorized users will be impeded in doing what they need to do.
2. The cybersecurity staff will have to be increased to manage manual overrides for false negatives.
3. If the actions [feel](mind-feelings.md) too punitive, authorized individuals will completely circumvent the system for a more convenient system (e.g., using personal email for workplace reasons).
