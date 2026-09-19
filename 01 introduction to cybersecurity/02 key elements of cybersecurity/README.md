# Module 2: Key elements of cybersecurity

## What I Learned

This module drops the pure-definition level and asks a practical question: _what actually has to exist for a security program to work?_ IBM's answer is that a functioning security posture rests on three elements, and the ordering of the module is meaningful — **education, process, and technology** — because each one builds on the one before it.

### Education

Education is the foundation in this framingable. The course's argument is that people are the first line of defense, and that awareness is what turns ordinary employees into that line instead of a liability. This covers formal security training, awareness campaigns, and ongoing education about new and emerging threats so that people understand _why_ a policy exists, not just that it exists.

What matters is that education is treated as an ongoing practice, not an onboarding checkbox. Threats change, and the education element is what keeps organizational behavior tracking the reality of the threat landscape rather than last year's version of it.

### Process

Process is what turns knowledge into repeatable behavior. This is the layer of policies, standards, and procedures that govern how security work actually happens: who is allowed to do what, how incidents get reported, how access gets granted and revoked, how software gets changed and deployed. It includes procedures for authorization, change management, incident response, and the day-to-day governance that makes security auditable and repeatable.

The key insight is that process is where _consistency_ comes from. A single knowledgeable engineer making the right call once is not a security posture; a defined, documented, repeatable procedure is. Process is also where the plan's earlier distinction between administrative and technical controls starts to feel real — the administrative controls (policy, procedure, training) live mostly in this "process" element, while the technical controls live in the element that comes next.

### Technology

Technology is the element people usually assume security is _all about_. This is the tooling layer — firewalls, antivirus, encryption, intrusion detection, access control systems, security information and event management (SIEM). IBM's framing positions technology as the enabler and multiplier of the other two elements rather than as a replacement for them.

The course is explicit that technology alone cannot carry a security program. A firewall sitting behind weak or nonexistent process, with untrained people operating it, is a weak control. This is why the module is ordered education → process → technology and not the reverse: the "stack" only holds if each layer is present.

### The People-Process-Technology Relationship

The module closes by reinforcing that the three elements work as an interlocking system. Weakness in any one element becomes the effective ceiling on the whole program — this is the same "chain is only as strong as its weakest link" idea, but stated structurally. A security program is not the sum of its parts; it is bounded by its weakest element.

## What Stood Out to Me

The ordering of the module is what stood out. In almost every discussion of security in casual settings, technology comes first and everything else is an afterthought ("just install a firewall"). IBM reverses that: **education → process → technology**. It took reading it this way to make it click — a tool is only as effective as the people using it and the process governing it. The firewall metaphor again: the tool enforces the policy, but the policy and the people have to exist first.

This also reframed how I think about my own lab practice. In my labs I have the technology corner well covered (I own the tools). What this module made me realize I should consciously build is the _process_ corner: documenting the procedure from reconnaissance through reporting consistently, so that my work is repeatable and auditable the way a professional engagement would be.

## Key Takeaways

- Education, process, and technology are the three necessary elements of a security program, in that order.
- People are treated as the first line of defense — the education element supports that.
- Process provides consistency, repeatability, and auditability.
- Technology enables and multiplies the other two elements but does not replace them.
- The program is bounded by its weakest element, so all three must be maintained together.

## What I Want to Explore Further

- How specific security frameworks (like NIST CSF) structure these three elements into a concrete implementation sequence.
- The relationship between the "process" element here and the "administrative controls" category from Module 1 — they seem to overlap significantly, and I want to understand the exact boundary.
- What a mature documented process looks like in practice (e.g., a real incident-response playbook), to emulate it in my own lab documentation.

## Sources

- IBM SkillsBuild, _Introduction to Cybersecurity_ course material (module 2, "Key elements of cybersecurity")
- IBM, _What is cybersecurity?_: https://www.ibm.com/think/topics/cybersecurity
- NIST, _Cybersecurity Framework (CSF 2.0)_: https://www.nist.gov/cyberframework
