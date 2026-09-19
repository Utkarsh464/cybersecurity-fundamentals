# Module 03 — Prevent attacks

> **Course:** Cybersecurity: On the Defense (IBM SkillsBuild)
> **Module:** 3 of 7
> **Status:** 100% COMPLETE

## What I Learned

This is the first hands-on "mechanism" module of the defense course: how do you actually *stop* attacks before they happen? It is the defensive mirror of the On the Offense modules that showed how attackers get in — now we see the architectural controls that deny them the door.

Core concepts:

- **The goal of prevention is to make attacks fail at the earliest possible stage.** Think of it as shifting every attack as far left (early) as you can. An attack that never gets in costs nothing; an attack that reaches your crown jewels costs $4.88M.

- **Reduce the attack surface.** The attack surface is the sum of all the ways an attacker can interact with your systems — every open port, every exposed service, every internet-facing device, every running service, every credential. Each element of the surface is a potential way in laser. The most fundamental prevention is simply **removing surface**: close unused ports, disable unneeded services, expose only what must be exposed.

- **The DMZ (demilitarized zone).** A network-level control that places internet-facing services (web servers, mail) in a segmented zone between the untrusted internet and the trusted internal network. Even if an internet-facing service is compromised, the attacker is still stranded in the DMZ and cannot automatically reach the internal LAN. It is compartmentalization expressed as network architecture.

- **Least privilege.** Grant users, applications, and services only the permissions they need to do their job — nothing more. It is the single most effective way to contain the blast radius of a single compromised account, because a compromised account can only do what it is allowed to do.

- **Vulnerability management.** The continuous loop of identifying weaknesses (scans, assessments), prioritizing them by risk, and remediating (patching, configuring) before attackers exploit them. Because you cannot patch everything instantly, you prioritize by exposure and exploitability. This is a *process*, not a tool.

- **Defense in depth.** The capstone idea: never rely on a single control. Layer controls so that if one fails, the next one catches the attacker — network zones + host hardening + least privilege + application controls + monitoring. Redundancy of protection is the point. Defense in depth is the architectural expression of "don't put all your eggs in one basket."

The module ties these together as a layered model: shrink the surface → segment the network → least-privilege the identities → close the known weaknesses → and never rely on just one of these.

## What Stood Out to Me

**Least privilege** is the one that keeps coming back to me, precisely because the Offense course showed me why it matters. When we studied privilege escalation and lateral movement, every single technique worked because a compromised account had *too much* privilege. Least privilege is the defense that directly neutralizes that. The offense course taught me the attack; this module taught me the exact control that stops it, and the two finally connect in my head.

I also like **defense in depth** as the organizing principle. It reframes "security" from a single product or a single fix to a *system* with redundancy — which is a much more mature and less fragile way to think about it.

## Practical Connection

These are controls I can actually set up and verify in my own lab:

- **Reduce attack surface / DMZ:** in my network labs, I can segment services into zones and verify that a compromised DMZ host cannot reach the internal network — the exact isolation the module describes.
- **Least privilege:** apply it to my own services and accounts — run services as unprivileged users, scope API keys, don't share credentials.
- **Vulnerability management:** the patching/prioritization loop maps to keeping my own environments current and logging which fixes matter.

The offense → defense link is the whole theme: I spent the offense course learning the techniques; this module gives me the architectural controls that make those techniques fail.

## Key Takeaways

- Prevention's goal is to **make attacks fail early** — shift them as far left as possible.
- **Reduce the attack surface** (close ports, disable services) is the most fundamental prevention.
- **DMZ** segments internet-facing services away from the internal network.
- **Least privilege** caps the blast radius of any single compromised account.
- **Vulnerability management** is a continuous prioritize-and-remediate process, not a tool.
- **Defense in depth** layers controls so no single failure is fatal.

## What I Want to Explore Further

- Building a real **DMZ/segmentation** in a lab and testing the isolation.
- The practical workflow of **vulnerability scanning → prioritization (CVSS + exposure) → remediation**.
- How **least privilege** is enforced at scale with identity and access management tools.

## Sources

- IBM SkillsBuild, *Cybersecurity: On the Defense* — Module 3 (prevent attacks)
- Concepts cross-referenced with the On the Offense course (privilege escalation, lateral movement, attack surface)
