# Module 01 — Financial impacts of cyberattacks

> **Course:** Cybersecurity: On the Defense (IBM SkillsBuild)
> **Module:** 1 of 7
> **Status:** 100% COMPLETE

## What I Learned

This module is the bridge between the offense and the defense course. Before you can defend anything, you need to understand what is actually at stake in money terms — because that is the language the business speaks. The module frames cybersecurity not as a technical discipline first, but as a **financial risk management** problem.

The core premise: a data breach is expensive, and it keeps getting more expensive. The module leans on the **IBM Cost of a Data Breach Report 2024** — which is the authoritative annual study, and notably a piece of my own employer's (IBM) research — to put real numbers on the conversation.

Key figures that anchor the module:

- The **global average cost of a data breach in 2024 was $4.88 million**, up 10% from the prior year — the largest single-year jump the report has recorded.
- The average cost per compromised **record** was **$165**.
- **47%** of breach costs are incurred in the **first year** after the breach, with the rest spread over subsequent years — meaning the financial impact extends well beyond the initial disclosure.
- **40%** of data breaches involved data stored **across multiple environments** — and these breaches were significantly more expensive than single-environment ones.
- **Two-thirds** of breaches were either **not detected by the organization's own security team** or were disclosed to authorities anyway (for example, via mandatory breach notification laws).
- **Phishing and stolen/compromised credentials** remained the most common initial attack vectors, and phishing alone carried a higher-than-average breach cost.

The module walks through what actually drives those costs:

1. **Detection and escalation** — the money spent finding out a breach happened and getting it contained.
2. **Notification** — legal and regulatory obligations to tell affected parties.
3. **Post-breach response** — forensics, remediation, and communication.
4. **Lost business** — customer churn, reputation damage, and lost revenue.
5. **Fines and legal judgments** — regulatory penalties and class-action exposure.

The big punchline the module keeps returning to: security is expensive, but **the cost of a breach dwarfs the cost of prevention**. The financial case for defense is not abstract — it is a direct comparison of these two numbers.

## What Stood Out to Me

The **"67% detected by a third party / disclosed by a regulator"** statistic really landed for me. It reframes the whole discipline: the vast majority of the time, an attacker is inside a network and the victim finds out from someone else — a law enforcement agency, a security vendor, or a leaked database — rather than from their own sensors. It connects directly back to the On the Offense course, where we saw that attackers move laterally and exfiltrate on their own schedule; if the defender does not detect it, the attacker controls the narrative completely.

I also found the **"47% in year one"** point striking from a math perspective. It means a breach is a multi-year financial liability, not a one-time spike. When I model this out, it changes how a budget conversation happens: you are not just paying for remediation once, you are carrying a depreciating but real obligation.

## Practical Connection

The "cost of a data breach > cost of prevention" framing is exactly the argument I would take into any budget justification. Instead of asking for security spend as a "cost center," the module gives a concrete, citable number — $4.88M average, $165/record — to compare against the price of the controls that reduce the likelihood.

I also connected this to my own exposure surface. The money isn't uniform: **40% of breaches touched multiple environments**, and multi-environment breaches cost more. That maps directly to the "reduce your attack surface" work in the Prevent Attacks module and to how I think about my own setups across machines, networks, and cloud — every extra environment is another chunk of that $4.88M you're exposing.

## Key Takeaways

- A data breach is a **multi-year, multi-line-item financial event**, not a single expense: detection, notification, response, lost business, and fines add up independently.
- The **2024 global average was $4.88M** (up 10% YoY), ~**$165 per record**, with **47%** of cost hitting in year one.
- **Most breaches are found by someone other than your own team** — detection is the weakest link, and that is where defenders should focus.
- Security is a **financial risk management** discipline: prevention costs less than the breach it avoids.

## What I Want to Explore Further

- The full IBM **Cost of a Data Breach Report 2024** methodology — how the per-record number is derived and whether it is comparable industry by industry.
- How **cyber insurance** prices these risks, since insurers run basically the same math the module walks through.
- The mechanics of **breach notification laws** (GDPR 72-hour, HIPAA, etc.) and what triggers the mandatory-cost bucket.

## Sources

- IBM, **Cost of a Data Breach Report 2024** (data anchoring the module)
- IBM SkillsBuild, *Cybersecurity: On the Defense* — Module 1 (financial impacts of cyberattacks)
