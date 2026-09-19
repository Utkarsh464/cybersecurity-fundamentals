# Module 7: Technical Scanning

## What I Learned

Technical scanning is the active side of reconnaissance. Where Module 6 gathered intelligence from public sources without touching targets, this module is about probing systems directly: finding which hosts are alive, which ports are open, which services run there, and which vulnerabilities they carry. The course steps through a natural progression: ping, traceroute, port scanning, vulnerability scanning, the internet-scale versions of the same idea, and machine learning entering the picture at the end.

For me this was the most familiar module, because scanning is what my own labs and tools do every day. The value here was structure: the course gave names and an order to a workflow I had been running semi-instinctively.

## Ping Test

The ping test uses ICMP to ask "is this host alive?". An Echo Request goes out, an Echo Reply comes back, and the round-trip time gives a rough latency estimate. It is the cheapest possible host-discovery technique.

The important caveats the course makes: ping tells you a host is up and reachable, but nothing about what it runs; and many firewalls and cloud providers block ICMP, so a host that does not answer ping may still be fully alive. Tools like Nmap handle this by combining ICMP with TCP probes to common ports, which is more reliable than ping alone.

## Traceroute

Traceroute maps the network path between your machine and a target. It works by sending packets with increasing TTL values; each router that drops a packet to zero replies with a time-exceeded message, identifying itself as a hop. The result is the sequence of routers packets traverse.

The course's point: traceroute reveals topology. It shows how many networks sit between you and the target, and it can expose infrastructure hostnames. It is useful for diagnostics and for mapping a network you are authorized to test, and the same information helps an attacker understand a target's connectivity.

## Port Scanning

Port scanning asks "which services is this host offering?". Every TCP or UDP port is a potential door, and scanning enumerates which ones are open.

The course explains the mechanics through the TCP three-way handshake: SYN, SYN-ACK, ACK. Different scan types observe different stages of that exchange:

- **TCP connect**: completes the full handshake. Works without privileges and is easy to detect.
- **SYN (half-open)**: sends SYN and aborts on reply. Faster and less logged, and the default for Nmap.
- **UDP**: sends UDP probes; slower and less reliable because many services stay quiet.
- **ACK and FIN variants**: map firewall rules and filtering behavior.

Port states matter: open, closed, or filtered (a firewall drops the probe). Knowing the state tells you what to investigate next. Combined with version detection, port scanning builds the inventory of services that an attacker would match against known exploits and a defender would close or monitor.

This is exactly the territory of the module's practical activity (network reconnaissance with scanning tools), and the skills carry directly into my [pentools](https://github.com/Utkarsh464/pentools) port scanner and my [Nmap-based lab workflows](https://github.com/Utkarsh464/labs).

## Vulnerability Scanning

Vulnerability scanning goes one level deeper: where port scanning says what is running, vulnerability scanning says what is wrong with it. Scanners fingerprint software versions and check them against databases of known vulnerabilities and CVEs, and they also look for common misconfigurations.

Key distinctions the course draws:

- **Unauthenticated scans** look from the outside like an attacker would, catching exposed issues.
- **Credentialed scans** log in and inspect patch levels and configuration directly; they are far more accurate.
- Tools like Nessus and OpenVAS maintain large vulnerability databases and produce prioritized reports.
- Results map to CVEs and CVSS severity scores, which is how teams decide what to fix first.
- False positives exist; scanners flag, humans confirm.

The course is clear that scanning someone else's network without authorization is illegal in most jurisdictions. Vulnerability scanning is an authorized activity on your own systems or with written permission.

## Search Engine for the Internet

"Search engine for the internet" is the course's name for services like Shodan and Censys. These continuously scan the entire public internet and index the banners every reachable device returns: open ports, service versions, default logins, exposed databases, even industrial control systems. Searching them works like a search engine, except the index is of devices instead of web pages.

The dual-use reality matters: the same index that lets defenders find their own exposed assets also lets an attacker find vulnerable targets at scale without touching them directly. In the course's framing, this is OSINT applied to technical assets, and the internet-scale version of local scanning.

## Network Scanning

Network scanning is the umbrella discipline: mapping hosts, subnets, operating systems and topology. It combines host discovery, OS fingerprinting (identifying the operating system from TCP/IP stack behavior), service detection, and mapping which machines sit on which network segments.

The course distinguishes active scanning (sending probes, informative but detectable) from passive scanning (observing existing traffic, quieter). It also emphasizes scope control and scheduling in real environments, because scanning fragile devices can break them.

## AI in Technical Scanning

The course closes the module with how AI and machine learning are changing scanning. The applications described are mostly augmentation rather than replacement:

- Automating analysis and triage of scan output, prioritizing plausible vulnerabilities over raw severity scores.
- Semantic matching of service fingerprints against CVE databases, which improves on exact-string matching.
- Adaptive scanning pipelines that adjust strategy based on intermediate results.
- Generating target-specific wordlists and reasoning about multi-step attack chains.
- AI-generated scan traffic that mimics legitimate patterns, balanced by ML-based detection of scanning behavior.

The takeaway the course frames: AI handles volume and pattern-matching, while humans provide context, judgment, and the authorization.

## What Stood Out to Me

This module formalized a workflow I already run daily in my labs. Seeing ping, traceroute, port and vulnerability scanning presented as one graduated discipline was clarifying: each tool answers one question, and the questions build on each other. I also appreciated the recurring boundary: everything here is only legal and legitimate within authorization, the same line the course drew for threat actors and researchers in Module 1.

## Practical Connection

This is the module with the most direct overlap with my own work:

- My [pentools](https://github.com/Utkarsh464/pentools) port scanner implements what the port-scanning section describes, TCP checks against a target host.
- My [isolated network labs](https://github.com/Utkarsh464/labs) begin with the same progression: Nmap host discovery, then service and version enumeration, before exploitation of what the scan found on Metasploitable 2, DVWA and WebGoat.
- My [dir-brute](https://github.com/Utkarsh464/dir-brute) crawler is the content-discovery companion that follows technical scanning in a real engagement.

The course's structure gave me a vocabulary for the sequence I had been following by habit, and confirmed that my lab workflow mirrors the standard progression in the field.

## Key Takeaways

- Technical scanning is the active side of reconnaissance: probing hosts, ports, services and vulnerabilities directly.
- Ping checks liveness, traceroute maps the path, port scanning enumerates services, vulnerability scanning finds weaknesses.
- Scan types and port states (open, closed, filtered) determine what a scanner can conclude.
- Credentialed scanning is far more accurate than unauthenticated scanning.
- Device-search engines like Shodan and Censys bring the same ideas to internet scale.
- AI augments scanning with automated triage, semantic CVE matching and adaptive pipelines, while humans retain judgment and authorization.

## What I Want to Explore Further

- Nmap's scripting engine (NSE) for automation, since my labs currently use elementary scans.
- Credentialed vulnerability scanning with a local OpenVAS instance against my lab VMs.
- Shodan and Censys search techniques, now that I understand the scanning behind the index.

## Sources

- Nmap, _Reference Guide_: https://nmap.org/book/man.html
- Nmap, _Port Scanning Techniques_: https://nmap.org/book/port-scanning.html
- Tenable, _Nessus_: https://www.tenable.com/nessus
- Greenbone, _OpenVAS Community Edition_: https://www.greenbone.net/en/community-edition/
- CISA, _Cyber Hygiene Services_ (vulnerability scanning): https://www.cisa.gov/cyber-hygiene-services
- Shodan, _Search Query Fundamentals_: https://help.shodan.io/the-basics/search-query-fundamentals
