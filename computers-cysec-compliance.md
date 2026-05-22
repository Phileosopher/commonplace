
# Cybersecurity compliance

Managing [cybersecurity](computers-cysec.md) for large organizations is vastly complicated compared with [individually-focused security](safety-security.md).

Individually managing permissions and configurations becomes more difficult across [a group of people](groups-small.md), for several reasons:

- Each group consists of a variety of people, and the weakest computer or least-tech-savvy user is the highest risk for the organization.
- A group draws more attention than an individual, proportionally to its popularity, creating more desire for hackers to infiltrate it.
- Groups are often subject to more [regional government laws](legal-safety.md) than individuals.
- If the organization is spread across multiple regions, completely legal actions in one region could imprison someone for life in another.

The legality and safety of the organization can often sit on the nuanced difference in IP address or choice of [protocol](standards-computers.md).

While every increase in a cybersecurity policy decreases the risk of damage, it comes with multiple secondary risks:

1. Authorized users will be impeded in doing what they need to do.
2. The cybersecurity staff will have to be increased to manage manual overrides for false negatives.
3. If the actions [feel](mind-feelings.md) too punitive, authorized individuals will completely circumvent the system for a more convenient system (e.g., using personal email for workplace reasons).

## Risk Management

NIST created its Risk Management Framework (RMF) to put [risk management](safety-riskmgmt.md) systems in place and test to be sure they work:

1. Prepare - everyone should [be aware](mind-awareness.md) changes will be happening.
2. Categorize - [organize](organization.md) how the system processes, stores, and transmits information and conduct a risk assessment.
3. Select - choose the controls that will protect the system based on the risk assessment.
4. Implement - carry out the controls and document what happens.
5. Assess - examine if the controls are in place, operating as intended, and creating desired results.
6. Authorize - the group leader makes a risk-based decision to authorize the system to operate.
7. Monitor - continuously monitor the implementation, as well as any further risks to the system.

## Background verification

To ensure a trustworthy system, all users must sign Acceptable Use Policies (AUPs) as a prerequisite to accessing anything.

- The more public presence an organization has, the more that users, groups, and even entire websites or IP address ranges must be routinely blocked.
- Most of these verifications arise through robust background checks, which usually require trusting another organization entirely for their validation of someone's background.

## Threat modeling

With enough skill and education, a skilled cybersecurity professional can stop most [PenTesting](computers-cysec-pentest.md) efforts.

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
