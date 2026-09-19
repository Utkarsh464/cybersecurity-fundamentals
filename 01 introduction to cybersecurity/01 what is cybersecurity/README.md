# Module 1: What is Cybersecurity?

## What I Learned

This module establishes the definition that the whole course — and by extension the whole learning plan — builds on. IBM defines cybersecurity as **the practice of protecting people, systems and data from cyberattacks by using various technologies, processes and policies**. The most important part of that definition for me is that IBM deliberately frames it as protecting _people, systems and data_ — not just "devices" or "networks" — and that it is about protection achieved through a mix of technology, process, and policy rather than technology alone.

The course also makes the point that cybersecurity is a **business enabler**, not just a technical function. That framing came up repeatedly and is worth holding onto for the courses that follow: security decisions are business decisions, and understanding the value of what you are protecting is part of the job.

### The CIA Triad

The core model for evaluating data security is the CIA triad:

- **Confidentiality** — information is accessible only to authorized individuals
- **Integrity** — data is kept accurate and complete, and is not altered without authorization
- **Availability** — data and systems are accessible when needed

The course frames the triad as the standard model for thinking about what security is actually protecting. Each control you apply, and each risk you think about, maps back to one of these three properties. I used this same triad extensively when working through the colleges module later in this course, so it became the vocabulary for evaluating everything.

### Controls

The course groups security safeguards into three categories:

1. **Administrative controls** — also called management controls. These are the policies, procedures, awareness training, and personnel rules that govern how people behave. Example: a password policy, security awareness training.
2. **Technical controls** — also called logical controls. These are the technical mechanisms that protect systems. Example: firewalls, encryption, access controls, antivirus, intrusion detection.
3. **Physical controls** — the physical barriers and mechanisms guarding the hardware and environment. Example: locks, security cameras, biometric scanners.

What stood out is that all three categories are needed and they reinforce each other. A strong technical control (like encryption) is undermined if an administrative control (like a clean-desk or credential policy) is missing, and both are undermined if the physical control (like a locked server room) fails.

### Core Vocabulary

The module also establishes the foundational threat vocabulary used everywhere in the plan:

- **Threat** — any potential danger to an organization's systems and data
- **Vulnerability** — a weakness that can be exploited by a threat
- **Risk** — the likelihood of a threat exploiting a vulnerability and causing harm
- **Attack vector** — the method or path an attacker uses to gain unauthorized access

These four terms are the shared risk vocabulary. Distinguishing threat from vulnerability from risk sounds pedantic until you realize that each one is addressed by a _different_ control — and the risk-management module later in the course depends on keeping them separate.

## What Stood Out to Me

What stood out most was how _framing_ cybersecurity as protecting people, systems and data (rather than just "devices") immediately changes how you think about the job. If security is only about devices, then the defense is purely technical. If security is about people, systems and data, then the procurement of policies, training and process becomes just as important as the firewall — which is exactly the argument this module's controls section makes.

I also found the CIA triad to be a genuinely useful simplification. Every time a later module talked about a control, an attack, or a risk, I found myself checking: _which corner of the triad is this protecting?_ That check turned the abstract model into a working tool.

## Practical Connection

Module 1 of the accompanying "Offense" course (threat actor groups) is where the vocabulary from this module earns its keep. The offense course's explanation of why a malicious insider is dangerous works precisely because of the term _attack vector_: an insider is already on the inside, so the attack vector is their legitimate credentials. Treating "threat," "vulnerability" and "attack vector" as separate concepts is what makes it possible to say something precise like that.

## Key Takeaways

- Cybersecurity protects people, systems and data, not just devices — via technology, process and policy.
- The CIA triad (confidentiality, integrity, availability) is the model used to evaluate what security protects.
- Controls come in three reinforcing categories: administrative, technical, and physical.
- Threat, vulnerability, risk, and attack vector are distinct concepts addressed by different kinds of defenses.

## What I Want to Explore Further

- How the CIA triad maps onto specific controls (which control protects which corner of the triad) — this is the bridge from this module to the "key elements" module.
- The difference between _risk appetite_ and general risk concepts, which this module only touches and the risk module covers in depth.
- IBM's "defense in depth" framing and how many layers of the three control categories are actually typical in a real enterprise.

## Sources

- IBM, _What is Cybersecurity?_ (Think): https://www.ibm.com/think/topics/cybersecurity
- IBM SkillsBuild, _Introduction to Cybersecurity_ course material (module 1, "What is Cybersecurity?")
- BSI, _The 3 Pillars of Information Security: understanding the CIA triad_: https://www.bsigroup.com/en-GB/insights-and-media/insights/blogs/the-3-pillars-of-information-security-understanding-the-cia-triad/
