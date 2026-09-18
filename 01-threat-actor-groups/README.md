# Module 1: Threat Actor Groups

## What I Learned

This module was about the people behind attacks — who the threat actors actually are, what they want, and what they are capable of. What stood out from the start is that the course treats threat actors as a spectrum rather than one faceless "hacker" stereotype. Each category differs in skill level, resources, motivation, and the kind of damage it can realistically cause.

The course also makes a point I had not fully appreciated: the most technically sophisticated attacker is not automatically the most common one. Realistic threat modeling means knowing which actors are actually likely to target you, and defending accordingly. A script kiddie, a criminal gang and a nation-state group do not require the same defensive response.

## Threat Actors

### Script Kiddie

A script kiddie is someone who runs existing tools and exploits without really understanding how they work. They are typically low-skill and opportunistic — they pick up ready-made tools (for example a Loic-style flood tool or a known exploit script) and use them against whatever target is convenient.

The name says it all: they "kidd" around with scripts. Their motivation is usually bragging rights, thrill, or curiosity rather than serious profit. Because they depend on public exploits, they mostly hit known, unpatched vulnerabilities — which is why basics like patching and good password hygiene stop most of them.

### Hacktivist

A hacktivist uses hacking to push a political or social message. The attack itself is part of the protest. Typical activities include website defacement, distributed denial of service, and leaking data to embarrass an organization.

What I found interesting is the communication aspect. A hacktivist wants the attack to be visible and attributable to their cause — the opposite of a stealthy criminal operation. Groups like Anonymous are the usual example, with operations aimed at organizations the group considers to be acting against its beliefs or against public interest.

### Criminal Gang

Criminal gangs are organized groups whose attacks are purely financial. The course frames them as businesses, which matches how they behave: they have developers, operators, negotiators, and money handlers, and they reinvest their profits into better tools.

These groups run the ransomware operations, business email compromise campaigns, and large-scale credential theft you read about in breach reports. The model that stood out to me is ransomware-as-a-service — where a gang develops the ransomware and rents it out to affiliates who do the actual deployments, with the profits split between them. That structure reappears in Module 4, so it was useful to see the actor category first.

### Nation-State Hacker

A nation-state hacker operates on behalf of a government, usually for espionage, sabotage, or strategic advantage. These are the most resourced and patient actors the course discusses — they fund long-running campaigns, develop or buy zero-day exploits, and can afford to wait months inside a network.

The course connects this category to advanced persistent threats: actors who establish a foothold and keep operating quietly over a long period. High-profile supply-chain compromises and destructive malware campaigns have been attributed to nation-state groups. What separates them from the other categories is capability and intent — they are precise, persistent, and backed by significant budgets.

### Malicious Insider

A malicious insider is someone inside the organization who uses their legitimate access to cause harm — stealing data, sabotaging systems, or selling secrets. They already have valid credentials and know where the sensitive data lives, which makes them harder to detect than an external intruder working their way in.

The course highlighted that insiders are not only current employees; ex-employees and contractors with retained access can fall into the same category. Motivations range from financial gain to revenge or ideological disagreement with the organization.

### Offensive Security Researcher

The offensive security researcher is the category that stood out most to me. They probe systems, find vulnerabilities, and use the same techniques as attackers — but with a defensive goal. In the course's framing they sit inside the threat-actor conversation because their skills overlap with criminals; the difference is authorization and intent.

Legitimate offensive researchers operate under permission — through penetration-testing engagements, bug bounty programs, or vulnerability research with responsible disclosure. The course makes the distinction that the same skill set can be used to break in or to harden, and what separates them is the legal and ethical framework around the work.

## What Stood Out to Me

The biggest takeaway for me was the overlap between categories. An individual can move between them — a script kiddie can grow into a criminal gang member, and the technical skill of a nation-state hacker is the same skill a researcher uses to find bugs for a living. Capability is shared; intent and authorization are what differ.

I also liked that the course did not rank threat actors purely by skill. A malicious insider may not be the most technically impressive actor, but they are often one of the most dangerous to a specific organization, precisely because they are already inside.

## Practical Connection

The offensive security researcher category is the lane my own lab practice sits in. My [PortSwigger labs](https://github.com/Utkarsh464/portswigger-academy) and the [isolated network labs against Metasploitable 2, DVWA and WebGoat](https://github.com/Utkarsh464/labs) use the same offensive techniques the course describes — the difference is that everything I attack is an intentionally vulnerable target inside my own setup, where I have full permission.

It was reassuring to see the course formalize this distinction. The label that module gave me for what I have been doing in my labs is "authorized offensive security research," not "hacking."

## Key Takeaways

- Threat actors are a spectrum of motivation and capability, not a single stereotype.
- The same technical skill set appears across categories; intent and authorization separate them.
- Insider threats matter because they bypass the perimeter entirely.
- Criminal gangs operate like businesses, complete with division of labor and profit-sharing models.
- Understanding who is likely to target you should drive how you defend — different actors need different responses.

## What I Want to Explore Further

- How threat intelligence teams track actor groups over time (the MITRE ATT&CK Groups page tracks real groups by their techniques — Module 3 gives me the vocabulary for that).
- The business structure behind ransomware operations, which this module introduced and Module 4 builds on.
- How bug bounty platforms formalize the offensive-security-researcher role in practice.

## Sources

- CISA, _Cyber Threats and Advisories_: https://www.cisa.gov/topics/cyber-threats-and-advisories
- CISA, _Nation-State Cyber Actors_: https://www.cisa.gov/topics/cyber-threats-and-advisories/nation-state-cyber-actors
- MITRE ATT&CK, _Groups_: https://attack.mitre.org/groups/
- Europol, _Internet Organised Crime Threat Assessment (IOCTA)_: https://www.europol.europa.eu/publication-events/main-reports/internet-organised-crime-threat-assessment-iocta-2023
- NIST SP 800-53 Rev. 5 (threat and vulnerability context): https://csrc.nist.gov/publications/detail/sp/800-53/rev-5/final
