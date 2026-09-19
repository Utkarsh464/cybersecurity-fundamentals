# Module 07 — Introducing threat intelligence

> **Course:** Cybersecurity: On the Defense (IBM SkillsBuild)
> **Module:** 7 of 7
> **Status:** 100% COMPLETE

## What I Learned

The final module of the defense course steps back from the _tools_ and into the _knowledge_ that makes a defender effective: **threat intelligence (TI)** — knowing who is attacking, how they operate, and what they want, so you can defend against what's coming rather than just what happened. This is the bridge between "On the Defense" and "Your Future in Cybersecurity," and it's the module that most changes _how_ you think about the field.

Core ideas:

- **What threat intelligence is.** **Evidence-based knowledge about cyber threats** — adversaries, their capabilities, their motivations, and their tactics/techniques/procedures (TTPs) — that you act on to **inform your security decisions**. It's the difference between reacting to attacks and _anticipating_ them. TI is not just a feed of indicators; it's the analysis that tells you what those indicators _mean_ for _your_ organization.

- **Types/categories of threat intelligence** — TI comes in layers, each useful for different decisions:
  - **Strategic** — big-picture: adversary motivations, geopolitical context, long-term trends (for executives/decision-makers).
  - **Tactical** — **TTPs**: _how_ attackers operate (MITRE ATT&CK is the vocabulary here — and I already know it from the offense course, which made this module an "aha").
  - **Operational** — specific incidents, campaigns, and imminent threats (for analysts deciding what to look for now).
  - **Technical** — **indicators of compromise (IoCs)**: hashes, IPs, domains, malware samples (the raw, machine-usable stuff that tools and signatures consume).

- **What TI is used for.** Informing risk management, prioritizing **vulnerability** and **patch** decisions (you fix the weaknesses being actively exploited first), tuning **detection** (what to watch for), guiding the **response** (who's attacking and how they move), and briefing decision-makers. It makes defensive effort _targeted_ instead of generic.

- **Sources of threat intelligence.** Open-source (OSINT), commercial feeds, industry-sharing communities (ISACs/ISAOs), government advisories (CISA, CERTs), and internal threat data from your own sensors and incidents. The module emphasizes: **your own network is the best starting source** — you already generate telemetry about what's actually hitting you.

- **The TI lifecycle** — a continuous cycle, typically: **direction** (what do we need to know?) → **collection** → **processing** → **analysis** → **dissemination** → **feedback**. TI is a _process_, not a product you buy once.
- **AI and threat intelligence** — AI/LLMs increasingly help process the mountains of TI (NLP on reports, triage, summarization, spotting patterns). The module flags both the promise and the caution: AI accelerates _analysis_, but it can't replace _judgment_ about what matters to your org.

The hands-on piece is a **threat intelligence research activity** — investigating a known threat (adversary group, malware family, or campaign) using the categories and sources above — which is exactly the "research a topic and write it up" pattern I've been practicing in this entire repo.

## What Stood Out to Me

Two connections made this module land hard:

1. **MITRE ATT&CK was already in my head.** The offense course taught me attack techniques organized by tactic — and that framework _is_ the "tactical threat intelligence" layer. So the moment the module mentioned TTPs and ATT&CK, I recognized the whole vocabulary from the other side. This is the clearest moment in the entire 4-course plan where **offense and defense turn out to be the same map, viewed from different directions.** The defender reads the attacker's playbook; the attacker is essentially threat intelligence with intent.

2. **The IoC awareness from offense.** Studying malware and attacks on the offense side, I learned that indicators (hashes, IPs, domains) are _stale by the time you have them_ — attackers rotate. This module formalizes why: technical IoCs are the _fastest-churning, least_ durable layer of TI, while _TTPs_ persist much longer. That reframed "indicators" for me — they're the tail of the intelligence chain, not the head.

## Practical Connection

The **threat intelligence research activity** is built for exactly the working style I already have in this repo: pick a threat, research it across authoritative sources, and write up what you learned with sources verified. So I can practice this module _by doing this repo's own job_ — and in fact, every writeup in this plan is, at a small scale, a piece of "intelligence analysis" (collect → process → analyze → write up → share).

Concretely, this connects forward to what I want in the "Future" course: **threat intelligence analyst** is one of the clearest job roles that the four-course credential points at, and it's one where my research-and-writeup habit is directly the job skill.

## Key Takeaways

- **Threat intelligence is evidence-based knowledge you _act on_** — it turns security from reactive to anticipatory.
- **Four layers:** strategic, tactical (TTPs), operational (incidents/campaigns), technical (IoCs) — each serves a different decision.
- **ATT&CK is the shared map** between offense and defense — same framework I learned attacking.
- **Your own telemetry/incidents are a first-class TI source** — you log more intelligence than you think.
- **TI is a lifecycle/process**, not a feed you subscribe to once.
- **IoCs churn fast; TTPs endure** — prioritize the durable knowledge over the fresh hashes.
- **AI accelerates TI analysis but can't replace judgment** about what matters to your organization.

## What I Want to Explore Further

- Doing the **TI research activity end-to-end**: pick a real adversary group or campaignfake and write a full strategic→technical threat-intel profile, using ATT&CK for the tactical layer.
- Standing up a tiny **TI pipeline**: collect IoCs from free/OSINT sources, normalize them, and see how they'd feed detection rules.
- Learning the **threat intelligence analyst role** in depth as a career angle — it directly follows from this module and bridges to course 04.

## Sources

- IBM SkillsBuild, _Cybersecurity: On the Defense_ — Module 7 (introducing threat intelligence)
- Activity: threat intelligence research (IBM SkillsBuild)
- Cross-references: offense course (MITRE ATT&CK, TTPs, IoCs), CISA/MITRE ATT&CK framework
