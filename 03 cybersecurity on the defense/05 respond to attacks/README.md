# Module 05 — Respond to attacks

> **Course:** Cybersecurity: On the Defense (IBM SkillsBuild)
> **Module:** 5 of 7
> **Status:** 100% COMPLETE

## What I Learned

Detection tells you something is wrong; **response is what you do about it.** This module is about how organizations take an incident from "we detected a problem" to "we are contained, recovered, and learned." It is built around the **incident response lifecycle** and the planning that keeps the business alive through an emergency.

Core ideas:

- **The incident response (IR) lifecycle** (nested in the NIST IR framework):
  1. **Preparation** — building the IR plan, the team, the tools, and the training _before_ anything happens. This is the phase you do when the sun is shining, and it is the phase that decides how well you handle the storm.
  2. **Detection and analysis** — recognizing that something is an incident, figuring out _what_ is happeningable (scope, impact, indicators), and determining the response priority. Detection is only useful if it is attached to _analysis_.
  3. **Containment, eradication, and recovery** — the sequence of limiting the damage (containment isolates systems so the attacker cannot spread), removing the threat (eradication), and restoring normal operation (recovery).
  4. **Post-incident activity** — the "lessons learned" phase where the team reviews what happened, documents it, and improves the plan so the next incident is handled better and faster.

- **Response teams.** IR is not a solo act — it is a **team function** with defined roles: the **incident response team** (technical responders) working alongside a **broader response team** that includes legal, PR/communications, HR, and executive stakeholders. The module emphasizes that deciding _who_ gets called, _when_, and _who makes the call to escalate_ is part of the plan — not something improvised in the moment.

- **Business continuity (BC)** — keeping the **business** running when systems fail. BC planning asks: what are the _critical_ functions, and how do we keep delivering them even if our normal tools are down? It is about alternate processes, workarounds, and keeping revenue and service alive.

- **Disaster recovery (DR)** — getting the **systems** back. DR planning answers: what needs to be restored, how fast, and from what? Its backbone is the **recovery time objective (RTO)** — how long the business can tolerate being down — and the **recovery point objective (RPO)** — how much data loss in time the business can tolerate. RTO and RPO drive every backup and recovery decision: the more you can tolerate, the cheaper the plan.

- **BCDR (business continuity + disaster recovery).** The module pairs these deliberately: BC keeps the _business_ alive while DR restores the _infrastructure_, and organizational resilience needs both timed to the RTO/RPO targets.

The hands-on piece is a **personal incident response plan** — scaling the whole lifecycle down to a single person's small world, which is exactly the right size to practice the thinking.

## What Stood Out to Me

The thing that stuck is how **response is the phase where the defense course finally becomes a discipline rather than a set of tools.** Prevention and detection are technical; response is _organizational_ — it is about roles, decisions, and process under pressure. The module insists that the plan exists _before_ the incident, because nobody thinks clearly in the middle of a breach. That idea — "you don't rise to the occasion, you sink to the level of your training/preparation" — is the spine of the whole module.

I also liked the RTO/RPO framing because it makes **money the driver of recovery design**. You do not buy the most expensive backup/DR solution; you buy the solution whose RTO/RPO matches what the business can actually tolerate. That is the same "security as financial risk management" thread from Module 1, applied to recovery.

## Practical Connection

The **personal incident response plan activity** is my favorite hands-on in the course so far, because it is honest about scale. I mapped it onto my own small-world reality:

- **Preparation:** keep consistent writeup discipline and repo hygiene (the conventions I already follow — doing writeups, verifying links, committing at the agreed window) as my "plan."
- **Detection/analysis:** know my baseline — what logs/signals I normally generate vs. what is abnormal.
- **Contain/eradicate/recover:** isolate the affected system, remove the foothold, restore from a known-good state — territory I've already practiced in labs.
- **Post-incident:** write the writeup, note what to do differently. The whole repo is, in a sense, one running "lessons learned" document.

This gives me a transferable template: the same lifecycle that runs a Fortune 500 SOC scales down to a single machine and a single learner — the _shape_ is identical.

## Key Takeaways

- **IR is a lifecycle (prepare → detect/analyze → contain/eradicate/recover → post-incident), not a single action.**
- **Response is a team sport** with pre-defined roles and an escalation decision tree.
- **BC keeps the business running; DR restores the systems** — and BCDR means doing both against RTO/RPO targets.
- **RTO and RPO convert business tolerance into concrete recovery numbers** — the financial driver of resilience.
- **The plan is written before the incident** — that's what separates a coordinated response from a fire drill.

## What I Want to Explore Further

- Reading **NIST SP 800-61** (Computer Security Incident Handling Guide) in full — the module is built on it and the real framework has much more depth.
- Building a sample **BCDR plan** for a small business as an exercise, complete with RTO/RPO targets and a restoration script.
- Practicing a hands-on **containment/eradication drill** in a lab — quarantining a compromised VMache and restoring it cleanly, on a timer.

## Sources

- IBM SkillsBuild, _Cybersecurity: On the Defense_ — Module 5 (respond to attacks)
- Activity: design a personal incident response plan (IBM SkillsBuild)
- NIST SP 800-61, _Computer Security Incident Handling Guide_ (framework behind the module)
