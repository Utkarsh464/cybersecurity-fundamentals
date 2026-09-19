# Module 3: Risk Management

## What I Learned

This module moves from _what security protects_ (the CIA triad) and _what it's built from_ (education, process, technology) to the machinery that connects the two: risk. The core move of the module is that risk isn't a feel-good label applied after the fact — it's a **valuated, quantified thing that you make deliberate decisions about**. The course walks through risk valuation, risk response, and risk appetite, and each of those is a distinct decision point.

### Risk Valuation

Risk valuation is the step where you actually take stock. It involves:

- **Risk identification** — naming the threats and vulnerabilities that exist
- **Risk analysis** — determining how likely each threat is to occur and how big the impact would be
- **Risk evaluation** — prioritizing risks so you know which ones to treat first

The point of doing this as a _process_ rather than a gut check is that it forces you to separate likelihood from impact. A risk that is extremely unlikely but catastrophic is handled differently from one that is likely but minor. IBM's framing — that risk management is about identifying, assessing and addressing financial, legal, strategic and security risks — makes clear that the same valuation machinery applies to non-technical risk as to technical risk.

### Risk Response (Risk Treatment)

Once a risk is valued, you choose how to respond. The course lists five standard responses:

1. **Risk avoidance** — not engaging in the activity that creates the risk
2. **Risk reduction** — putting controls in place to lower the likelihood or impact (this is where most security work lands)
3. **Risk sharing** — distributing the risk across partners (e.g., through a joint venture or shared responsibility model)
4. **Risk transfer** — shifting the risk to a third party (e.g., via cyber insurance)
5. **Risk acceptance** — acknowledging the residual risk and preparing for it rather than fighting it

The module emphasizes that these are choices, not defaults. A common beginner mistake is to assume "mitigate everything," but the five responses make explicit that _not_ mitigating is occasionally the correct business decision — which is only defensible, though, when it's a decision and not a default.

### Risk Appetite

Risk appetite is the final distinction: how much risk an organization is willing to pursue or retain in order to meet its goals. IBM is careful to separate two closely-related terms:

- **Risk appetite** — the amount and type of risk an organization is willing to accept in pursuit of its objectives
- **Risk tolerance** — the acceptable variation in outcomes around a given level of risk

The course positions risk appetite as a strategic statement that should align with business goals, and it ties directly into the earlier "security is a business enabler" framing. An organization that depends on rapid innovation has a different risk appetite than one whose whole value is stability, and their security programs should look different as a result.

## What Stood Out to Me

The five risk responses were the piece that changed how I think. Before this, "risk management" read to me as a synonym for "do something about the risk." Seeing _acceptance_ listed as a legitimate, named response reframed it: managing risk means being _intentional_ about what you do with it, and sometimes the intended action is to consciously hold it.

That landing points backwards at Module 1's vocabulary — the difference between _threat_ and _vulnerability_ and _risk_ isn't academic. An attacker exploiting a specific vulnerability is a _threat_; whether you're exposed depends on whether the combination of likelihood and impact crosses your _appetite_; and which response you pick depends entirely on valuation. The whole risk decision chain is only possible because those earlier terms were kept distinct.

## Practical Connection

Risk response maps cleanly onto the reasons my own lab environment is built the way it is. Running intentionally vulnerable tools (Metasploitable, DVWA, WebGoat) against isolated targets is a deliberate _risk acceptance_ + _risk reduction_ decision: I accept the residual risk of the lab itself because it's isolated from anything I care about, and I reduce it further by keeping the lab segmented on my own network. The value of calling it by name is that it makes the _why_ of the isolation explicit — it's not cosmetic, it's the response to a specific, valuated risk.

## Key Takeaways

- Risk has three verbs before you ever act: identify, analyze, evaluate.
- There are five legitimate risk responses, and acceptance is one of them.
- Risk appetite and risk tolerance are distinct concepts, not synonyms.
- Risk posture should be a deliberate strategic choice aligned with business goals.

## What I Want to Explore Further

- How NIST's risk management framework sequences these steps in practice (identification → assessment → response → monitoring is the classic loop).
- What a real risk register looks like — the document that records identified risks, their valuation, and their chosen response.
- How risk appetite gets _codified_ — the difference between "we're risk-averse" and an actual written risk appetite statement.

## Sources

- IBM, _What is Risk Management?_: https://www.ibm.com/think/topics/risk-management
- IBM Consulting, _Risk Management services_: https://www.ibm.com/consulting/risk-management
- ISACA Journal, _The Modeling of Risk Evaluation, Risk Appetite, and Risk Tolerance_: https://www.isaca.org/resources/isaca-journal/issues/2024/volume-6/the-modeling-of-risk-evaluation-risk-appetite-and-risk-tolerance
- NIST, _Cybersecurity Framework (CSF)_: https://www.nist.gov/cyberframework
