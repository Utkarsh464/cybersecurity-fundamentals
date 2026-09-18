# Module 2: Types of Cyberattacks

## What I Learned

This module walks through the common ways attacks actually happen. The list is broad — network-level floods, human-targeted deception, malicious software, and application-level injection — and the point of putting them side by side is to see how different the attacker's job is depending on the vector.

Two things stood out. First, several of these attacks are not exclusive: a phishing email is a common way malware gets delivered, and SQL injection often leads to data theft rather than being an end in itself. Second, the course includes AI in cyberattacks, which tells you something about where the threat landscape is headed — the tools used to attack are getting smarter.

## Attacks Covered

### Denial of Service

A denial of service (DoS) attack aims to make a service unavailable to its legitimate users. The attacker floods the target — a server, service, or network — with more requests or traffic than it can handle, exhausting bandwidth, memory, or connection slots until legitimate traffic can no longer get through.

The course frames DoS as an availability attack: it does not necessarily steal anything, it breaks a business. Even relatively simple floods can take a small service down, which is why rate limiting and traffic filtering exist.

### Distributed Denial of Service

The distributed version, DDoS, does the same thing but from many sources at once. Because the attacker controls a botnet — a network of compromised machines — the flood comes from thousands of different IPs, which makes it much harder to block than a single-source attack (blocking one IP does nothing when the traffic comes from everywhere).

The scale difference matters. A DDoS can generate enormous volumes of traffic, and the course notes that even major internet infrastructure and popular services have been disrupted by botnet-driven floods. The amplification techniques used to multiply traffic are part of why these attacks can be so large.

### Phishing

Phishing is a social engineering attack that uses deceptive messages — usually email — to trick people into revealing sensitive information or taking a harmful action like clicking a malicious link or opening an infected attachment. The attacker impersonates a trusted sender: a bank, a service provider, a colleague.

The course's framing clicked for me here: phishing attacks the human, not the machine. Because it relies on the victim's trust and the sense of urgency the message creates, technical security controls alone cannot fully stop it. That is why recognizing phishing is taught as a user skill.

### Spear Phishing

Spear phishing is phishing with reconnaissance. Instead of a mass campaign sent to anyone, the attacker targets a specific person or organization and personalizes the message using information gathered about them — real names, job roles, even current projects.

The personalization makes spear phishing significantly more convincing than generic phishing. The course also mentions whaling as the extreme end: targeting senior executives specifically, because their accounts have the most access and value. What makes this attack dangerous is that the message looks indistinguishable from normal work communication.

### Malware

Malware is the umbrella term for software written with malicious intent — it covers viruses, worms, trojans, ransomware, spyware and rootkits. The course treats malware mostly as a delivery mechanism problem: some piece of malicious code gets onto a system, often through phishing attachments, drive-by downloads, or infected removable media, and then does the attacker's work.

The distinction between malware families is worth keeping straight because they behave differently: viruses need a host file and user action to spread, worms propagate across networks on their own, trojans disguise themselves as legitimate software, and ransomware locks data behind encryption. Common to all of them is that they are code doing something on a system the owner never approved.

### Man-in-the-Middle

A man-in-the-middle (MitM) attack places the attacker between two parties who believe they are talking directly to each other. The attacker intercepts the communication and can read it, modify it, or inject new content without either side knowing.

The course frames the attacker's position as the key concept: they sit in the middle of the communication path. On a local network this can happen through techniques like ARP spoofing or a rogue Wi-Fi access point; at the application layer, interception of unencrypted traffic achieves the same result. Encryption is the standard defense because it makes the intercepted traffic unreadable.

### DNS Attacks

DNS is the phone book of the internet — it translates domain names like `example.com` into IP addresses. DNS attacks target that resolution process. The course groups a few variants under this heading: poisoning the DNS cache so users are redirected to a malicious site, hijacking DNS configuration to control where traffic goes, and using DNS itself as a channel to smuggle data out.

What connects these is the trust problem: users type a domain name and expect to reach the real site. If the resolution step is corrupted, they land on a convincing fake — and often never realize they were redirected at all.

### SQL Injection

SQL injection exploits web applications that build database queries by inserting user input directly into the SQL statement. If the input is not validated or parameterized, an attacker can inject their own SQL, bypass login checks, or read, modify and delete data from the database.

This was the first attack type in the module that I had already practiced, so it clicked immediately. Injection works because untrusted input is trusted as code. The fix the course emphasizes is treating user input as data, never as something to execute — parameterized queries and input validation.

### AI in Cyberattacks

The course closes the module with AI in cyberattacks, and this was the part that felt most current. Artificial intelligence is lowering the barrier to attacking: it can generate convincing phishing messages at scale, automate the work of finding vulnerable systems, create realistic deepfake audio or video for impersonation, and help malware evade detection by adapting to defensive patterns.

The takeaway from the course is that AI does not create brand-new attack categories so much as it supercharges the existing ones — more volume, more personalization, more automation. Defenders are turning to AI too, which is the arms-race angle the course leaves you with.

## What Stood Out to Me

The pattern across all these attacks is that they exploit some form of trust — trust in an email sender, in a domain name, in an application's input handling, in the network you are connected to. Once I started seeing the attacks that way, the defensive logic of encryption, validation, and awareness training made more sense as a set.

I also appreciated that the course put social engineering and technical attacks in the same module. They are usually taught separately, but in practice phishing is the delivery step for a lot of malware, and the targets are often chosen via DNS or network observation.

## Key Takeaways

- DoS and DDoS are availability attacks; DDoS multiplies the flood using a botnet and amplification.
- Phishing targets human trust; spear phishing adds reconnaissance and personalization, so it is far more convincing.
- Malware is a delivery-and-execution problem, with families (viruses, worms, trojans, ransomware) behaving differently.
- MitM is fundamentally about position — the attacker sits in the middle of the communication path.
- DNS attacks corrupt the trust in domain-name resolution, sending users to the wrong place.
- SQL injection treats untrusted input as executable code; parameterization fixes it.
- AI amplifies existing attack types: more volume, more personalization, more automation.

## What I Want to Explore Further

- Detection-side tooling for the attacks in this module (how defenders spot DDoS traffic, C2 traffic, DNS tunneling in practice).
- Parameterized queries and prepared statements as the concrete fix for SQL injection.
- Keeping up with AI-driven attacks — this is the topic in the module most likely to change quickly.

## Sources

- CISA, _Malware, Phishing, and Ransomware_: https://www.cisa.gov/topics/cyber-threats-and-advisories/malware-phishing-and-ransomware
- MITRE ATT&CK, _Techniques_: https://attack.mitre.org/techniques/
- OWASP, _SQL Injection_: https://owasp.org/www-community/attacks/SQL_Injection
- OWASP Top 10 (2021), _A03:2021 Injection_: https://owasp.org/Top10/A03_2021-Injection/
- NIST, _Artificial Intelligence Risk Management Framework_: https://www.nist.gov/artificial-intelligence
- Anti-Phishing Working Group (APWG): https://apwg.org
