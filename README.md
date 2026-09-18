# Cybersecurity: On the Offense

Personal learning notes from the **IBM Cybersecurity: On the Offense** course.

Each module in this repository is written from my own understanding of the course material. Where the course touched a topic briefly, I researched the same topic through primary sources — IBM, CISA, NIST, MITRE, OWASP, Lockheed Martin, Europol and others — to check the facts and get the context right.

This is a learning log, not a textbook. If a section feels light, it is because the course itself covered it lightly, and I kept the scope to what the course actually taught.

## Course Progress

- [x] Module 1 - Threat Actor Groups
- [x] Module 2 - Types of Cyberattacks
- [x] Module 3 - Structure of a Cyberattack
- [x] Module 4 - Cybercrime Ecosystem
- [ ] Module 5 - Social Engineering
- [ ] Module 6 - Open-Source Intelligence
- [ ] Module 7 - Technical Scanning
- [ ] Module 8 - Case Studies
- [ ] Final Assessment

Modules 5-8 and the final assessment are still ahead of me, so nothing there is documented yet.

## What This Repository Contains

| Directory                                                                | What is in it                                                                                                                                                            |
| ------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| [01-threat-actor-groups](01-threat-actor-groups/README.md)               | The threat-actor categories the course covers: script kiddies, hacktivists, criminal gangs, nation-state hackers, malicious insiders and offensive security researchers. |
| [02-types-of-cyberattacks](02-types-of-cyberattacks/README.md)           | Denial of service, distributed denial of service, phishing, spear phishing, malware, man-in-the-middle, DNS attacks, SQL injection and AI in cyberattacks.               |
| [03-structure-of-a-cyberattack](03-structure-of-a-cyberattack/README.md) | How attacks are structured, the Lockheed Martin Cyber Kill Chain, MITRE ATT&CK, and why understanding the structure matters for defense.                                 |
| [04-cybercrime-ecosystem](04-cybercrime-ecosystem/README.md)             | How the underground cybercrime economy works: the ecosystem, the underground marketplaces, the initial cash injection and the role of cryptocurrency.                    |
| [references](references/README.md)                                       | The sources I used while researching each module.                                                                                                                        |

## Learning Approach

My process for every module looked like this:

```
IBM Course -> Research -> Understand -> Document -> Connect With Practice
```

The course defines the boundaries. I read the module, noted the exact concepts it teaches, researched those same concepts in reputable sources to verify details, wrote my understanding in my own words, and only then looked for connections to things I have actually practiced.

The IBM course decides what belongs in a module. My research and lab experience only add depth to topics the course already covers.

## Practical Connections

Purely practical labs are not part of this course. However, when a course topic overlaps with something I have already tried in my own lab work — PortSwigger labs, Metasploitable 2, DVWA/WebGoat, or tools I built myself — I link the relevant repository so the notes connect back to hands-on practice.

Those projects are my own work and are separate from the IBM course. Where I link them, they are examples of practice, not claims of professional experience.

## Related Repositories

The repositories referenced inside the module notes:

- [portswigger-academy](https://github.com/Utkarsh464/portswigger-academy) — Web Security Academy lab writeups, including SQL injection
- [labs](https://github.com/Utkarsh464/labs) — isolated-network labs against Metasploitable 2, DVWA and WebGoat
- [pentools](https://github.com/Utkarsh464/pentools) — small Python security utilities, including a blind SQLi extractor
- [http-proxy-lab](https://github.com/Utkarsh464/http-proxy-lab) — an HTTP forward proxy built from scratch

These are only included where a course topic genuinely overlaps with what the repository demonstrates.

## Disclaimer

Everything here is for educational purposes. The techniques and concepts described are studied to understand how attacks work so they can be defended against. Practical security testing should only ever be performed on systems you own or have explicit written authorization to test.
