# Module 4: Common Misconceptions about Cybersecurity

## What I Learned

This module is the course's reality-check. Where the earlier modules built the vocabulary and the machinery, this one debugs the _beliefs_ people carry into the topic — and the course's framing is that these beliefs are not neutral. A misconception is not just a wrong fact; it is a wrong fact that causes you to **drop your guard in exactly the wrong place**. Each myth below is paired with the reality the course teaches, and I've also noted the specific lab/workload connection where one exists.

### Myth 1: "Antivirus is enough"

**The reality:** Antivirus is necessary but nowhere near sufficient. Modern attacks routinely bypass signature-based detection entirely: fileless malware (memory-only execution), stealing valid credentials and using them normally, and browser-based exploits never drop a "known malicious file" for antivirus to catch. IBM's position is that security has to be multi-layered — antivirus is one layer, not the whole stack. This connects directly to the _defense in depth_ idea that runs through the course.

### Myth 2: "We're too small / too uninteresting to be targeted"

**The reality:** Small businesses are _especially_ attractive targets. The Hiscox Cyber Readiness Report found that nearly half (41%) of small businesses suffered a cyberattack within the past year BasketBasket. IBM's formulation is memorable: cybercriminals "look for the easiest opportunity, not the biggest company." Small organizations are often easier _because_ they are assumed to have weaker defenses — the attacker isn't choosing fame, they're choosing convenience.

### Myth 3: "Strong passwords are all I need"

**The reality:** A strong password is a necessary baseline but it does not survive phishing, keyloggers, credential-stuffing on reused passwords, or credentials bought off the dark web after a data breach elsewhere. The course's answer to this category of weakness is **multi-factor authentication (MFA)** — adding a second factor so that a stolen password alone is not sufficient.

### Myth 4: "We know the main risks already"

**The reality:** The threat landscape does not hold still. New vulnerabilities are reported continuously (thousands per year), and the module's point is that what matters is not "did we know about _the_ big risks" but "are we tracking the _current_ risk landscape." New attack vectors come from emerging technology (AI, new deployment models) and from changes in human behavior and process — which loops back to Module 2's "education and process enable technology" idea.

### Myth 5: "Some industries are off the hook"

**The reality:** No industry is exempt, and the _wrong_ belief here is especially dangerous because it creates a false sense of safety. The course specifically notes that high-profile ransomware has hit healthcare, local government, and nonprofits — the sectors people most often _assume_ attackers would leave alone on moral grounds. Attackers follow valuable data and weak defenses, not sentiment.

## What Stood Out to Me

The thing that shifted my thinking most was the reframing of the "too small to be targeted" myth. My instinct — like most people's — is that attackers would rather chase big, impressive targets. The data says the opposite: attackers optimize for _ease_, and small organizations are a large pool of relatively easy targets. That inversion (fame vs. convenience) is the single most useful idea in this module, because it tells you who needs to take security seriously: everyone, including solo practitioners and learners.

I also appreciated that the module refrains from giving each myth a purely technical fix. The rebuttal to "we already know the risks" isn't a firewall — it's a _practice_ of continuously monitoring the threat landscapecheny. That's a Module 2 lesson (process over technology) showing up again, which is the pattern this course keeps rewarding: each module reuses the vocabulary and frameworks of the ones before it.

## Practical Connection

The "antivirus is enough" myth is the one that most clearly shows up in my own lab practice. My lab intentionally runs _known-vulnerable_ applications (DVWA, WebGoat, Metasploitable) — literally the kind of thing a signature-based scanner would flag. If I had believed antivirus "was enough," the entire premise of my offensive-security lab would be contradictory. The course's multi-layer answer is what makes the lab coherent: the lab environment is itself a deliberate _acceptance_ (from Module 3) of a known risk, kept safe by _physical isolation_ (from Module 1's physical controls), which is the layered-control framing working as designed.

## Key Takeaways

- Antivirus is one layer, not the whole defense; modern attacks signatularly bypass signature detection.
- Attackers optimize for ease, not fame — small organizations are a large pool of easy targets.
- MFA is the standard answer to the password alone being insufficient.
- The risk landscape is continuously shifting; awareness is a practice, not a one-time fact.
- No industry is exempt — attackers follow value and weakness.

## What I Want to Explore Further

- Real-world statistics that quantify how often fileless / credential-based attacks bypass traditional antivirus (to firm up my own mental model of "how much").
- MFA implementation patterns and the difference between possession-based factors (hardware tokens) and knowledge-based factors, plus phishing-resistant MFA.
- How the "ease, not fame" targeting model is reflected in honeypot and attacker-provenance research.

## Sources

- IBM, _What is cybersecurity?_ misconceptions section: https://www.ibm.com/think/topics/cybersecurity
- Verizon, _The truth behind 5 small-business cybersecurity misconceptions_: https://www.verizon.com/business/resources/articles/s/truth-behind-5-small-business-cybersecurity-misconceptions
- Palo Alto Networks, _Is antivirus enough for small businesses?_: https://www.paloaltonetworks.com/cyberpedia/is-antivirus-enough-for-small-businesses
- PCMag, _Stop believing these 5 antivirus misconceptions_: https://www.pcmag.com/explainers/stop-these-5-antivirus-misconceptions-could-leave-you-unprotected
