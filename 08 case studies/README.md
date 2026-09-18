# Module 8: Case Studies

## What I Learned

The final content module is a set of real incidents that put the whole course to work: threat actors (Module 1), attack types (Module 2), structure (Module 3) and the ecosystem (Module 4) all show up in the cases the course selected: Stuxnet, the Los Angeles Unified School District, the National Security Agency, Cash App and SolarWinds. The point the course makes is that these are not exotic: each one is a recognizable instance of things already covered, and each one is chosen to teach a different lesson.

## Stuxnet

Stuxnet is the first known cyberweapon that caused physical destruction. It targeted Iranian nuclear-enrichment centrifuges at Natanz by taking over the Siemens PLCs that controlled rotor speed, spinning the machines into self-destruction while showing operators normal readings. Roughly a thousand of six thousand centrifuges were destroyed, and the program is historically attributed to the US and Israel, though neither government has officially confirmed it.

What stands out technically: the worm used four zero-day Windows exploits and a stolen digital certificate, and it crossed the air gap on infected USB drives. The lesson the course draws is about attack surface: even an air-gapped, protected network is reachable through removable media and the people around it, and nation-state actors will invest years and rare exploits for a strategic target.

## Los Angeles Unified School District

The LAUSD case is a mainstream ransomware story with an unusual ending. Over Labor Day weekend in 2022, Vice Society, a Russian-speaking criminal gang, hit the second-largest school district in the US, disabling IT systems, encrypting infrastructure, and stealing about 500 GB of data including student records and staff information. The district refused to pay, and the gang leaked the stolen data anyway.

The course uses this case to make the double-extortion point from Module 4 concrete: encryption is only half the leverage; the threat of leaking stolen data is the rest. It also shows a criminal gang as a business (Module 1) and education as a soft, high-data target. The defensive lessons are the standard ones: patching internet-facing systems, MFA, backups, and incident-response planning before the incident.

## National Security Agency

The NSA case is the moment an intelligence agency's own offensive capability became everyone's problem. The Shadow Brokers, an unconfirmed group, leaked NSA hacking tools in 2016 and 2017, including EternalBlue, an exploit for a Windows SMB vulnerability. Microsoft had already patched it, but unpatched systems across the world were hit within weeks by WannaCry, a self-spreading ransomware that disrupted hospitals in the UK and organizations in 150 countries, and later by NotPetya, which caused billions in damage.

The course's lesson here is layered: the value of patching (a patch existed a month before the outbreak), the danger of hoarding zero-days, and the way leaked tools cascade into mass attacks. It is also a case where a nation-state actor (Module 1) generated a capability that criminal and state groups then weaponized.

## Cash App

Cash App is the smallest and least technical case, which is exactly its point. In December 2021, a former employee of Block, the company behind Cash App, downloaded internal reports containing data on about 8.2 million US customers. The access should have been revoked the day the employee left; it was not.

The course frames this as a clean example of the malicious-insider category from Module 1 and of a kill chain that is almost empty: no reconnaissance, no exploit, no malware, valid credentials the whole way. The defense is offboarding discipline: revoke access at termination, enforce least privilege, and audit who can reach what.

## SolarWinds

SolarWinds is the supply-chain case. In 2020, attackers broke into the build process of SolarWinds Orion, an IT-monitoring product used by tens of thousands of organizations, and injected a backdoor into a legitimate software update, digitally signed with SolarWinds' own certificate. About 18,000 customers installed it. The attackers, attributed to the Russian SVR, then moved against a small number of high-value victims, including US government agencies, using stolen credentials and existing tools rather than more malware.

MITRE ATT&CK documents the operation as a campaign (C0024) mapped to dozens of techniques, and the course connects it to the kill chain from Module 3: the chain began at the vendor, not the victim. The lesson is trust: software that is legitimately signed by a trusted vendor still has to be verified, and zero-trust thinking applies at every layer.

## What Stood Out to Me

Looking at the five cases together, the pattern the course wanted me to see is that the frameworks actually work. Stuxnet and SolarWinds trace cleanly through the kill chain; LAUSD is the ecosystem and criminal-gang model in action; Cash App is the insider threat with an almost empty kill chain; the NSA leak is what happens when capabilities escape into the wild. None of these needed new theory; they needed the vocabulary this course built across the previous modules.

The second pattern is that the biggest failures were not exotic either. Unpatched systems, unrevoked access, misplaced trust in signed software: the breaches happened because basics were missed, which is a humbling and useful lesson.

## Activity: Summarizing Alerts and Advisories

The module's activity is to read a real security alert or advisory and summarize it: what the threat is, who is affected, and what to do. This is the practical skill of translating documents like CISA advisories, which use alert codes such as AA22-249A and structure findings around recommended actions, into a short brief. The skill matters because advisories are how defenders learn about active threats and required mitigations, and the course ends the module with this to point the notes toward the everyday work of a security professional.

## Practical Connection

The case studies do not map to my labs directly; no lab target of mine is remotely comparable to Natanz, a school district or a software supply chain. What they do is exercise the analytical frameworks I use in my own notes: I traced each case through the Cyber Kill Chain and considered which threat-actor category (Module 1) and which attack types (Module 2) it exemplifies, exactly the way I map my own lab attacks in my [lab writeups](https://github.com/Utkarsh464/labs).

The activity also formalizes something I already do: reading and summarizing security publications. Applying it to a real CISA advisory, per the exercise, turns that habit into a structured skill.

## Key Takeaways

- Stuxnet shows nation-state capability, air-gap bypass via USB, and the first physical destruction by malware.
- LAUSD shows ransomware double extortion and why education is a soft, high-data target; refusing to pay is a policy choice with consequences.
- The NSA case shows the cascade from leaked tools to WannaCry and NotPetya, and the value of patching before an exploit goes public.
- Cash App is a minimal-kill-chain insider threat: access that was never revoked.
- SolarWinds is supply-chain compromise at scale, with signed updates carrying a backdoor.
- Real advisories are readable, structured documents; summarizing them is a core professional skill.

## What I Want to Explore Further

- MITRE ATT&CK campaign pages, starting with the SolarWinds campaign (C0024), since the course references the framework this way.
- Reading current CISA advisories as they are published, using the summarizing skill from this module's activity.
- More historical cases (NotPetya in depth, Colonial Pipeline) through the same kill-chain lens.

## Sources

- CISA, _Primary Stuxnet Advisory (ICSA-10-272-01)_: https://www.cisa.gov/news-events/ics-advisories/icsa-10-272-01
- CISA, _#StopRansomware: Vice Society (AA22-249A)_: https://www.cisa.gov/news-events/alerts/2022/09/06/stopransomware-vice-society
- CISA, _Indicators Associated with WannaCry Ransomware (TA17-132A)_: https://www.cisa.gov/news-events/alerts/2017/05/12/indicators-associated-wannacry-ransomware
- CISA, _SolarWinds advisory (AA20-352A)_: https://www.cisa.gov/news-events/cybersecurity-advisories/aa20-352a
- MITRE ATT&CK, _Campaign C0024 (SolarWinds Compromise)_: https://attack.mitre.org/campaigns/C0024/
- Block Inc., _SEC Form 8-K disclosure (Cash App breach)_: https://www.sec.gov/Archives/edgar/data/1512673/000119312522095215/d343042d8k.htm
