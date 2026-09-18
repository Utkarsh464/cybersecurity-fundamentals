# Module 3: Structure of a Cyberattack

## What I Learned

This module is about how attacks are structured, rather than what the attacker ultimately wants. The core idea is that almost every serious attack is a sequence of steps, not a single action: the attacker has to find a target, build or obtain a way in, deliver it, exploit a weakness, keep access, and only then do the damage.

The course presents two complementary ways of looking at that sequence (the Lockheed Martin Cyber Kill Chain and MITRE ATT&CK), and the useful part for a beginner is that both exist to give defenders a shared map. If you know which stage an attack is in, you know what to look for and where to stop it.

## Cyber Kill Chain

### What It Is

The Cyber Kill Chain is a framework developed by Lockheed Martin that describes the stages an attacker must complete to achieve a goal in a network intrusion. It originated from Lockheed Martin's Intelligence Driven Defense model and breaks an intrusion into seven phases:

1. **Reconnaissance**: researching and selecting the target: gathering email addresses, mapping the network, identifying what is exposed.
2. **Weaponization**: coupling an exploit with a deliverable payload, for example embedding malware into a document.
3. **Delivery**: transmitting the weaponized payload to the target, commonly via phishing email, a malicious website, or removable media.
4. **Exploitation**: triggering the payload so it takes advantage of a vulnerability on the target system.
5. **Installation**: installing malware or a backdoor so the attacker keeps a foothold on the system.
6. **Command and Control (C2)**: establishing a channel the attacker can use to remotely control the compromised system.
7. **Actions on Objectives**: the attacker carries out the actual goal: stealing data, destroying systems, or moving further into the network.

### How the Course Explains It

The course presents the model as a linear chain of phases and emphasizes its defensive value: if defenders can break the chain at any single link, the attack fails. Detect the phishing email, and delivery fails. Block the C2 traffic, and the attacker can no longer control the system. The metaphor of a chain is the point: one intact link is all it takes.

### My Understanding

What helped me was mapping the sequence to attacks I had studied in my labs. The reconnaissance phase is what Nmap and enumeration do in a workflow; the delivery and exploitation phases are where a Metasploit exploit run happens; installation and C2 describe the persistence and shell-access stages that come after. The kill chain gave me names for stages I had been doing semi-instinctively.

I also noted that the model has a real-world bias: it describes intrusions that start from the outside and move in. Not every attack fits perfectly (insider threats skip the outer phases entirely), but as a map for how network intrusions typically unfold, it is clear and practical.

## MITRE ATT&CK

### What It Is

MITRE ATT&CK is a knowledge base of real-world adversary behavior, organized as tactics, techniques, and procedures (TTPs). It is built from observed attacks and is publicly accessible at attack.mitre.org.

The vocabulary matters here. Tactics are the strategic goals of the attacker: the stages, such as Initial Access, Persistence, or Exfiltration. Techniques are the specific methods used to achieve a tactic, each with its own identifier (for example, Phishing is T1566). Procedures are the concrete implementations: how a particular group actually carried out a technique. ATT&CK organizes these into matrices for enterprise systems, mobile devices, and industrial control systems.

### My Understanding

If the kill chain is a timeline, ATT&CK is a catalog. Instead of one linear sequence, it lists the behaviors attackers exhibit across many campaigns, which lets you compare groups against each other and check whether your defenses cover the techniques that matter. When I first looked at the enterprise matrix, the volume of techniques was overwhelming, but the structure (tactic → technique → procedure) makes it navigable, and every technique links to detection and mitigation advice.

## Cyber Kill Chain vs MITRE ATT&CK

The two frameworks are designed for different jobs and work well together.

The **Cyber Kill Chain** is a linear model of the phases of an intrusion, from reconnaissance to final objective. It is simple to explain and good for understanding the overall progression of an attack and where it can be interrupted.

**MITRE ATT&CK** is a non-linear knowledge base of observed adversary behaviors. It does not assume a fixed order, and it covers behaviors the kill chain's seven phases map awkwardly onto, like lateral movement and defense evasion, by giving them dedicated tactics.

My short version after this module: the kill chain tells you the shape of an attack; ATT&CK tells you the content of one. Defensive teams commonly use both, mapping the chain to understand progression and ATT&CK to reason about specific techniques.

## What Stood Out to Me

The concept that stayed with me is that structure is what makes defense possible. An attacker operating as an unstructured blur would be impossible to defend against, but because attacks follow recognizable stages, each stage becomes a place to detect, delay, or stop the adversary.

I also found it telling that both frameworks were created with defense in mind: the kill chain by a defense contractor for their own incident-response team, and ATT&CK from years of real observed intrusions. They are maps drawn from what attackers actually do, which is why studying them is worth more than memorizing attack definitions.

## Practical Connection

The stages in this module map onto my [isolated-network penetration-testing labs](https://github.com/Utkarsh464/labs) against Metasploitable 2, DVWA and WebGoat. Those workflows start with reconnaissance (Nmap scans, service discovery, version enumeration), move through exploitation (Metasploit modules against known vulnerabilities), and end in post-exploitation access, which is the kill chain's shape in miniature, running against a deliberately vulnerable target.

The course gave me the vocabulary for a process my labs had been teaching me by repetition: I now know which phase of the chain each lab step occupies, and where an equivalent real-world attack would try to persist and establish command and control.

## Key Takeaways

- Serious attacks are structured sequences, and each stage is a potential defensive control point.
- The Cyber Kill Chain's seven phases (reconnaissance, weaponization, delivery, exploitation, installation, command and control, actions on objectives) describe the progression of a network intrusion.
- Breaking the chain at any single link stops the attack.
- MITRE ATT&CK catalogs adversary behavior as tactics (why), techniques (how), and procedures (actual implementation).
- The kill chain describes the shape of an attack; ATT&CK describes its content.

## What I Want to Explore Further

- The MITRE ATT&CK enterprise matrix in depth, starting with the tactics this module mentioned (Initial Access, Persistence, Command and Control, Exfiltration).
- Detection and mitigation mappings: parts of the ATT&CK pages that show which defensive controls address each technique.
- How incident responders use these frameworks during a real investigation (later modules in this course touch this).

## Sources

- Lockheed Martin, _Cyber Kill Chain_: https://www.lockheedmartin.com/en-us/capabilities/cyber/cyber-kill-chain.html
- Lockheed Martin, _Gaining the Advantage: Applying Cyber Kill Chain Methodology_: https://www.lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/Gaining_the_Advantage_Cyber_Kill_Chain.pdf
- Lockheed Martin, _Intelligence-Driven Computer Network Defense_ (original research paper): https://www.lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf
- MITRE ATT&CK: https://attack.mitre.org/
- MITRE ATT&CK, _Enterprise Matrix_: https://attack.mitre.org/matrices/enterprise/
