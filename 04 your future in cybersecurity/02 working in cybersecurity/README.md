# Module 02 — Working in cybersecurity

> **Course:** Your Future in Cybersecurity (IBM SkillsBuild)
> **Module:** 2 of 4
> **Status:** 100% COMPLETE

## What I Learned

If Module 1 proves the market exists, Module 2 is where the market's _panic_ becomes a _career question_: what does it actually mean to _be in_ cybersecurity — and which of the dozens of possible versions of that do I want? The module's answer to "what do cybersecurity people actually do?" is grounded in the **NIST NICE Framework** (SP 800-181 Rev. 1), which organizes the field into **five work role categories** spanning **52 distinct work roles**:

1. **Oversight and Governance (OG)** — strategy, policy, leadership, risk management, compliance. The business-facing spine of security. Example roles: CISO, GRC analyst, security manager.
2. **Design and Development (DD)** — building and testing secure systems. Example roles: security architect, secure software developer.
3. **Implementation and Operation (IO)** — configuring, running, and maintaining security systems. SOC tools, identity infrastructure, firewalls. Example roles: systems security administrator, network security specialist.
4. **Protection and Defense (PD)** — actively defending against attacks. Example roles: **SOC analyst**, incident responder, threat hunter.
5. **Investigation (IN)** — forensics and breach investigation. Example roles: digital forensics analyst, cybercrime investigator.

The module walks through the most common entry paths and the reality of each:

- **SOC Analyst (Tier 1)** — the classic entry role: monitoring alerts, triaging, escalating. High volume, high learning velocity, and often the fastest on-ramp.
- **Incident Responder** — the actual hands-on response when something happens: containment, eradication, recovery. Ties directly to my defense course (module 05, respond to attacks).
- **Threat Intelligence Analyst** — research-heavy, produces the context other defenders consume. Directly the capstone skill I documented in the defense course (module 07).
- **Security Engineer** — builds and maintains the tooling (SIEM, EDR, firewalls, IAM) that the SOC operates.
- **Penetration Tester** — offense, for hire: authorized attacks to find weaknesses before criminals do. This is the role the entire On the Offense course built toward.
- **GRC Analyst** — Governance, Risk, and Compliance: policies, audits, vendor risk, regulatory alignment. The marriage of security with business and law.

What the module stresses is that these are **not silos** — they feed each other. A SOC analyst's detections become a threat intelligence analyst's raw material; an engineer's deployment decisions shape what a responder can actually do; a pen tester's findings are the vulnerability a defense team patches. Knowing the whole landscape — not just one role — is what makes you valuable both as a specialist and as a collaborator.

## What Stood Out to Me

The **NICE Framework** clicked harder than I expected. Having already toured offense and defense, I realized my entire 4-course arc maps onto these categories almost exactly: Introduction taught the concepts (OG-adjacent), On the Offense built offense skill (PD + IN flavor), On the Defense built defense skill (PD + IO), and now the final course is teaching me _which category to aim at_. The framework is the label that connects the work I have already done to the roles that pay for it. And because employers literally write job postings in NICE language, I can now read a posting and immediately know which category and which of my existing skills it's testing.

## Practical Connection

The most direct move: **map my existing writeups to NICE categories** in the repo — tag each module writeup with the NICE category/categories it most directly serves. That turns a "learning log" into a "skills map" that I (and a hiring manager) can read at a glanceторое. It is the same repo, one labeling layer richer, and it directly demoes the NICE-fluency employers look for.

## Key Takeaways

- There are **5 NICE categories / 52 roles**, not "one cybersecurity job."
- **SOC Tier 1 is the classic entry on-ramp** — high velocity, high learning rate.
- Roles are **interdependent, not siloed** — the field rewards breadth of understanding.
- **Pen testing (offense)** and **threat intelligence / response (defense)** directly reuse the skills I've already documented.
- Employers write postings in **NICE language** — knowing the framework means speaking the market's vocabulary.

## What I Want to Explore Further

- Filling out a **NICE work-role map** for my repo: which of the 52 roles my lab writeups + this repo best evidence, and what's missing.
- Researching the **entry-role breakdown** most common for self-taught candidates (SOC Tier 1 vs. GRC vs. threat intel) to pick my lane.
- The **NICE Framework interactive/reference tools** to browse roles interactively.

## Sources

- NIST, _NICE Framework — Work Roles_ (SP 800-181 Rev. 1): https://www.nist.gov/itl/applied-cybersecurity/nice
- IBM SkillsBuild, _Your Future in Cybersecurity_ — Module 2 (working in cybersecurity)
- Cross-ref: defense course modules 05 (respond) + 07 (threat intelligence); offense course (pen testing role)
