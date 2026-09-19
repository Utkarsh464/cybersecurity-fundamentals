# Cybersecurity Fundamentals & On the Offense

Personal learning notes from the **IBM SkillsBuild Cybersecurity Fundamentals** learning plan, written course by course.

This repository currently holds the **Introduction to Cybersecurity** — the first course in the plan — and the **On the Offense** course I have already completed. The remaining courses in the plan (On the Defense, then Your Future in Cybersecurity) come next.

Each course in this repository is written from my own understanding of the course material. Where the course touched a topic briefly, I researched the same topic through primary sources (IBM, CISA, NIST, MITRE, OWASP, Lockheed Martin, Europol and others) to check the facts and get the context right. That research is where pretty much all of the links in the module notes come from.

This is a learning log, not a textbook. If a section feels light, it is because the course itself covered it lightly, and I kept the scope to what the course actually taught.

## Course Progress (Cybersecurity Fundamentals plan)

- [x] **Course 1 — Introduction to Cybersecurity** — 100% complete
- [x] **Course 2 — On the Offense** — 100% complete
- [ ] **Course 3 — On the Defense** — planned
- [ ] **Course 4 — Your Future in Cybersecurity** — planned

The **IBM Cybersecurity Fundamentals** credential requires completing all four courses and passing each final assessment)Skip.

## Course 1 — Introduction to Cybersecurity

The foundational course that builds the shared vocabulary the rest of the plan uses: the CIA triad, controls, risk, misconceptions, and the legal/ethical boundary that separates authorized security work from crime.

| Module                                                                                                                  | What is in it                                                                                                                     |
| ----------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------- |
| [01 — What is cybersecurity?](<01 introduction to cybersecurity/01 what is cybersecurity/README.md>)                    | Definition, the CIA triad, the three control categories (administrative, technical, physical), and the threat vocabulary.         |
| [02 — Key elements of cybersecurity](<01 introduction to cybersecurity/02 key elements of cybersecurity/README.md>)     | Education, process and technology as the three pillars of a security program.                                                     |
| [03 — Risk management](<01 introduction to cybersecurity/03 risk management/README.md>)                                 | Risk valuation, the five risk responses, and risk appetite vs. risk tolerance.                                                    |
| [04 — Common misconceptions](<01 introduction to cybersecurity/04 common misconceptions about cybersecurity/README.md>) | The myths that make people and businesses drop their guard, and the reality behind each.                                          |
| [05 — Laws and ethics](<01 introduction to cybersecurity/05 laws and ethics/README.md>)                                 | Computer-misuse laws (UK CMA, US CFAA, EU directive, Budapest Convention), other notable laws, and the ethics of authorized work. |

## Course 2 — On the Offense

The complete threat-actor and attack-structure course, in eight modules. See the course README for the overview and the credential path.

| Directory                                                                    | What is in it                                                                                                                                       |
| ---------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------------------------------------------------- |
| [01 — Threat actor groups](<01 threat actor groups/README.md>)               | The threat-actor categories: script kiddies, hacktivists, criminal gangs, nation-state hackers, malicious insiders, offensive security researchers. |
| [02 — Types of cyberattacks](<02 types of cyberattacks/README.md>)           | DoS, DDoS, phishing, spear phishing, malware, man-in-the-middle, DNS attacks, SQL injection and AI in cyberattacks.                                 |
| [03 — Structure of a cyberattack](<03 structure of a cyberattack/README.md>) | The Lockheed Martin Cyber Kill Chain, MITRE ATT&CK, and why understanding structure matters for defense.                                            |
| [04 — Cybercrime ecosystem](<04 cybercrime ecosystem/README.md>)             | The underground economy: ecosystem, marketplaces, initial cash injection, and cryptocurrency.                                                       |
| [05 — Social engineering](<05 social engineering/README.md>)                 | How attackers manipulate people instead of software: psychology, delivery methods, and how to defend.                                               |
| [06 — Open-source intelligence](<06 open source intelligence/README.md>)     | Collecting intelligence from public sources: what OSINT is, its sources, the legal boundaries.                                                      |
| [07 — Technical scanning](<07 technical scanning/README.md>)                 | Active reconnaissance: ping, traceroute, port scanning, vulnerability scanning, device search engines.                                              |
| [08 — Case studies](<08 case studies/README.md>)                             | Real incidents read through the frameworks built in Modules 1-4.                                                                                    |

## Related Repositories

Purely practical lab work is not part of the IBM courses, but where a course topic overlaps with something I have actually built or tried in my own lab environment, I link the relevant repository so the notes connect back to hands-on practice. Those projects are my own work and are separate from the IBM course — they are examples of practice, not claims of professional experience.

- [portswigger-academy](https://github.com/Utkarsh464/portswigger-academy): Web Security Academy lab writeups, including SQL injection
- [labs](https://github.com/Utkarsh464/labs): isolated-network labs against Metasploitable 2, DVWA and WebGoat
- [pentools](https://github.com/Utkarsh464/pentools): small Python security utilities, including a blind SQLi extractor
- [http-proxy-lab](https://github.com/Utkarsh464/http-proxy-lab): an HTTP forward proxy built from scratch
- [tryhackme-writeups](https://github.com/Utkarsh464/tryhackme-writeups): TryHackMe room writeups, including network reconnaissance and incident response
- [dir-brute](https://github.com/Utkarsh464/dir-brute): a concurrent directory brute-forcer and web crawler

## Disclaimer

Everything here is for educational purposes. The techniques and concepts described are studied to understand how attacks work so they can be defended against. Practical security testing should only ever be performed on systems you own or have explicit written authorization to test.
