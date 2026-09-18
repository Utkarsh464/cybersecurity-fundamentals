# Module 6: Open-Source Intelligence

## What I Learned

This module is about collecting intelligence from information that is already public. Open-source intelligence (OSINT) means gathering and analyzing publicly available data to answer a question: who runs a domain, what an organization exposes, what technology it uses, or what a person has posted online. The course's framing that stayed with me is that "open" refers to the source, not the cost; the information is accessible without special authority, which makes OSINT the only intelligence discipline anyone can practice.

The module also planted the idea that OSINT is the foundation of most other intelligence work, and that the same public data used to target victims is what defenders use to understand their own exposure.

## Open-Source Intelligence Versus Alternatives

Intelligence is divided into disciplines by source type:

- **OSINT**: publicly available data, no authorization needed.
- **HUMINT**: information from people (diplomats, informants, interviews); requires access to people.
- **SIGINT**: intercepted communications and electronic signals; requires interception authority and infrastructure.
- **IMINT/GEOINT**: imagery and geospatial data, often from satellites; requires classified platforms.

The distinction that matters: HUMINT, SIGINT and IMINT require special access and are typically national-intelligence activities with legal boundaries. OSINT is the exception; anyone with a browser can do it. That is also why both sides use it so heavily, defenders and attackers.

## Sources of Open Information

The course organizes sources into categories, and the practical list is long:

- **Search engines**: normal web search plus advanced operators (site:, filetype:, inurl:) that surface specific documents and pages.
- **Domain and network data**: WHOIS registrant records, DNS records, name servers, and subdomains via certificate-transparency logs.
- **Social media and public profiles**: names, roles, relationships, locations, technology choices.
- **Government and public records**: corporate filings, patents, sanctions lists, court records, procurement data.
- **Job postings**: positions reveal an organization's technology stack and security tools.
- **Breach-notification sites**: whether accounts or data have appeared in known breaches.
- **Device-search engines**: Shodan and Censys index internet-connected devices, open ports and service banners.
- **Web archives**: the Wayback Machine preserves historical versions of sites, including deleted content.
- **Document metadata**: author names, software versions and creation dates embedded in public files.

What impressed me is how much of this is just careful, systematic use of things that are already public: WHOIS, DNS, search operators, job ads. No hacking involved.

## Guidelines for Gathering Open Information

The course is explicit that OSINT has a legal and ethical boundary, and it is the same line drawn elsewhere in this course:

- Only collect from sources that are genuinely public; if there is a login screen, a paywall or an access control, stop.
- Do not use stolen credentials, do not bypass authentication, and do not exploit vulnerabilities to reach data.
- Respect privacy laws and a platform's terms of service, even when data is technically visible.
- Collect only what the intelligence question needs; minimize personal data.
- Record where each piece of information came from and when, because web content changes and disappears.
- Cross-check against multiple sources before concluding, because public channels can be used to plant disinformation.

## Why Is Open-Source Intelligence an Area of Interest for Everyone

The course argues that OSINT matters beyond espionage:

- **For defenders**: threat intelligence, red-team reconnaissance, and checking your own exposure before an attacker does.
- **For individuals**: anything you post publicly can be assembled into a profile of you, and spear phishers use exactly that profile to make lures convincing.
- **For organizations**: job postings, employee social profiles and public documents leak their technology stack and structure.

That is the point that connected the module for me: the same OSINT techniques that find a target are what make spear phishing (Modules 2 and 5) effective, so knowing OSINT is also knowing how to defend against a personalized attack.

## What Stood Out to Me

I had known pieces of this before (WHOIS, search operators), but the module gave them a framework and a discipline. OSINT is the intelligence counterpart to Module 1's threat actors and their targets: before any technical step, attackers build a picture from public data, and the kill chain's first phase (reconnaissance, from Module 3) is largely OSINT.

The other thing that stuck is the boundary. OSINT stops where access control starts. Everything in Module 7 (technical scanning) probes systems directly; OSINT stays on the surface of what is already public. Keeping those two apart is what keeps the practice legal.

## Practical Connection

OSINT is a genuine overlap with my [TryHackMe notes](https://github.com/Utkarsh464/tryhackme-writeups). The network-reconnaissance section of the Jr Penetration Tester path covers passive recon in detail: WHOIS, DNS lookups and OSINT collection, which is exactly the ground this module covers.

The practical lesson for my own work: when I set up a lab target, I can walk the OSINT checklist over it first, and every step I document is a step an attacker would take against a real target.

## Key Takeaways

- OSINT is intelligence from publicly available sources; "open" refers to access, not cost.
- Unlike HUMINT, SIGINT and IMINT, OSINT requires no special authority, which is why everyone uses it.
- Sources range from search operators and WHOIS/DNS records to social media, job postings, breach sites, device-search engines and web archives.
- The legal line is simple: public data only; if access control exists, it is out of scope.
- OSINT is the foundation of reconnaissance (Module 3's kill chain), spear phishing (Module 2) and social engineering (Module 5).

## What I Want to Explore Further

- Certificate-transparency logs for subdomain discovery, since that extends WHOIS/DNS data.
- Shodan and Censys, which this module introduces and Module 7 builds on for active scanning.
- How analysts verify OSINT findings against disinformation, which the course flagged as a real risk.

## Sources

- Wikipedia, _Open-Source Intelligence_ (definitions and categories): https://en.wikipedia.org/wiki/Open-source_intelligence
- MITRE ATT&CK, _Reconnaissance (TA0043)_: https://attack.mitre.org/tactics/TA0043/
- Wikipedia, _Intelligence cycle_: https://en.wikipedia.org/wiki/Intelligence_cycle
- Wikipedia, _Human intelligence (intelligence gathering)_: https://en.wikipedia.org/wiki/Human_intelligence_(intelligence_gathering)
- NIST, _Cybersecurity Framework_: https://www.nist.gov/cyberframework
