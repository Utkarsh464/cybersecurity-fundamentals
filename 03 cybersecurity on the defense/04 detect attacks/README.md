# Module 04 — Detect attacks

> **Course:** Cybersecurity: On the Defense (IBM SkillsBuild)
> **Module:** 4 of 7
> **Status:** 100% COMPLETE

## What I Learned

Prevention is the dream, but when we were on the offense we saw that prevention is not enough — attackers get in. So detection is where the defense actually earns its keep: **you cannot respond to what you cannot see**. This module is about visibility — how an organization finds out that it is being attacked (or already has been), and the layered toolkit it uses to do it.

Core ideas:

- **Antimalware.** The classic host-level detection. Modern antimalware layers multiple techniques: **signature-based detection** for known malware, **behavioral/heuristic detection** for new and unknown variants, and **real-time protection** that blocks malicious behavior as it happens. The module is careful to frame antimalware as **one layer among many** — a safety net, not the whole answer————because the module acknowledges that antimalware does not catch everything (new zero-days, fileless attacks that never touch disk).

- **Logging.** The _raw material_ of detection. If you do not capture events — who logged on, what ran, what connected where — you have nothing to search later. Logs from endpoints, servers, firewalls, and identity systems are the substrate every other detection tool consumes. A system that does not log is a system that is invisible and un-auditable.

- **Network monitoring.** Looking at traffic as it flows rather than files as they sit. Because most attacks move over the network at some point (command-and-control, lateral movement, exfiltration — all the stages I studied in the offense course), traffic is one of the most reliable places to spot malicious behavior. Tools like **Wireshark** and **Zeek** inspect packets; the module ties this back to the offense side, which is exactly where I learned to _watch_ traffic from the attacker's perspective.

- **SIEM (Security Information and Event Management).** The aggregation + correlation layer. A SIEM (such as IBM **QRadar**) pulls logs from across the environment into one place, normalizes them into a common format, and applies **correlation rules** that surface suspicious combinations of events that no single log would reveal on its own. A good SIEM turns a firehose of individual events into a handful of actionable alerts.

- **SOC (Security Operations Center).** The human + process layer. The people who sit in front of the SIEM, triage alerts, investigate, and coordinate the response. A SIEM without a **SOC** is just an expensive alarm — the SOC is what converts signals into decisionsrable.

- **AI in detection.** The frontier. AI/ML is increasingly used for what does not scale by hand: **behavioral baseline anomaly detection**, triage prioritization, and spotting attack patterns in millions of events that a human analyst would never see. The module frames AI as **amplifying the analyst**, not replacing them.

The hands-on activity is a **log-analysis exercise** — examining a set of logs and identifying the suspicious activity — which is precisely the skill I practice in every lab writeup, now given a formal name.

## What Stood Out to Me

The statistic that landed hardest (carried forward from Module 1): **most breaches are detected not by the organization itself but by a third party** — law enforcement, a security vendor, or a leaked database. Almost every compromise I studied from the defensive side was _visible_ in the victim's own logs in retrospect; nobody was looking at them in the moment. That is the whole point of detection: **it converts retrospective visibility into real-time action.**

I also like how directly this module mirrors the offense course. Where the offense course taught me to use network monitoring to _hunt and attack_, this module teaches the same tools to _watch and defend_. Same protocols, same packets, opposite intent — and knowing both sides is what makes each side make sense.

## Practical Connection

This is the module that maps most directly onto my existing hands-on practice:

- The **log-analysis activity** is exactly the kind of exercise I keep doing in my labs — reconstructing an incident from log entries. Now I have the formal vocabulary (SIEM, correlation, SOC) to describe why that skill matters beyond the lab.
- **Network monitoring with Wireshark/Zeek** is something I have already used while studying how attacks travel; this module tells me those same skills are a _detection control_, not just a learning tool.
- The **on-demand antimalware scan** (run a scan with Malwarebytes) is a simple, repeatable practice I can actually run on my own systems locally — verification that a machine is clean by a tool I'm not relying on 24/7.

## Key Takeaways

- **Detection is the layer that turns "noise" into "incident"** — you can't respond to what you can't see.
- **Logging is the substrate** of every detection tool; without logs there is nothing to correlate.
- **Antimalware is one layer, not the answer** — signatures miss new and fileless attacks.
- **SIEM correlates, SOC decides** — tools surface; humans make the call.
- **Network monitoring** is where offense and defense finally meet in the same packet stream.
- **AI amplifies the analyst** — triage and anomaly detection at a scale humans can't manage by hand.

## What I Want to Explore Further

- Standing up a real **SIEM workflow (QRadar or an open-source alternative)** and feeding it synthetic logs to watch correlation rules actually fire.
- Getting hands-on with **AI-driven anomaly detection** — what a "baseline" really is and how drift from it gets flagged.
- PraƯctising **log forensics** on a real-ish dataset: reconstructing an attack timeline from logs alone, like the module's activity but end-to-end.

## Sources

- IBM SkillsBuild, _Cybersecurity: On the Defense_ — Module 4 (detect attacks)
- Activity: log analysis + on-demand antimalware scan (IBM SkillsBuild)
- Cross-reference: offense-course network monitoring and traffic-analysis modules
