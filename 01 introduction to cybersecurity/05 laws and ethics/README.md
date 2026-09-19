# Module 5: Laws and Ethics

## What I Learned

This module is where the course draws the legal and ethical line around everything taught so far. Up to now the plan built vocabulary (Module 1), the three pillars (Module 2), and the risk machinery (Module 3). This module answers the question the others deliberately deferred: **what separates the skilled-but-authorized researcher from the skilled-but-criminal attacker?**

The answer has two layers. The first is _law_ — the codified, written line that criminalizes certain acts regardless of intent or skill. The second is _ethics_ — the grayer discussion about what makes using your skills acceptable even where the law, by itself, is silent. The course is explicit that these are not the same thing, and that treating them as identical is itself a misconception.

### Common Types of Computer Misuse Laws

The course walks through the major computer-misuse statutes, and the throughline is that they share a common shape: they criminalize **unauthorized access** to, and **unauthorized modification** of, computer material. The UK Computer Misuse Act is the lead example:

**UK — Computer Misuse Act 1990 (CMA)**

- **Section 1**: Unauthorised access to computer material
- **Section 2**: Unauthorised access with intent to commit or facilitate further offences
- **Section 3**: Unauthorised modification of computer material (including deletion and data corruption)
- **Section 3A**: Unauthorised acts causing, or with intent to cause, serious damage — added by the Police and Justice Act 2006, with impact thresholds tied to the UK economy or human welfare

The course's framing of the CMA's weak spot is what stood out: the law predates the web and the cloud, and has had to be stretched by amendments and case law to cover activity its drafters could not have imagined. That "law moves slower than technology" gap is a theme that returns in the ethics discussion.

**US — Computer Fraud and Abuse Act (CFAA), 18 U.S.C. § 1030**

The US federal counter part. First enacted in 1984 and amended several times (most recently in 2008), the CFAA criminalizes:

- Obtaining national-security information through unauthorized access
- Unauthorized access to a government computer
- Accessing a "protected computer" without authorization (or in excess of authorization) and obtaining information — a "protected computer" includes any computer used in or affecting interstate or foreign commerce, which covers most networked machines
- Trafficking in passwords or similar access credentials
- Causing damage through unauthorized access, with thresholds for loss and damage
- Extortion involving threats to damage a protected computer

The CFAA is the law that has generated the most controversy in the security-community context, because of its breadth and because it has been used in cases involving both malicious actors and (controversially) researchers and journalists. That controversy is exactly where the module's ethics discussion lives.

**EU — Directive (EU) 2013/40 on attacks against information systems**

This directive replaces the earlier Framework Decision and establishes a common threshold across EU member states: it requires criminalizing **illegal access to information systems**, **illegal system interference**, **illegal data interference**, and **illegal interception**, plus aggravated penalties where the offense is committed within the framework of a criminal organization, causes serious damage, or affects critical infrastructure.

**Budapest Convention on Cybercrime (Council of Europe, 2001)**

The first international treaty on cybercrime. It requires signatories to criminalize offenses against the confidentiality, integrity and availability of computer data and systems, and — critically — establishes a framework for **mutual legal assistance** between countries, because cybercrime does not respect borders)Skip on top of defining crimes, the convention is the mechanism that lets one country's investigators ask another country for evidence.

### Other Notable Cybercrime Laws

The course also walks through statutory landscape beyond computer-misuse acts:

- **USA PATRIOT Act (US, 2001)** — expanded surveillance and information-sharing powers for law enforcement and intelligence, and extended the definition of offenses related to computer fraud.
- **GDPR (EU, 2018)** — the General Data Protection Regulation. Not a "computer misuse" law, but the most consequential law for _data handling_: it imposes duties on anyone processing personal data, grants rights to data subjects, and caps penalties (up to 4% of annual worldwide turnover or €20M, whichever is greater). The course pairs GDPR with HIPAA as examples of how security failures now have regulatory, not just criminal, consequences.
- **HIPAA (US, 1996)** — the Health Insurance Portability and Accountability Act, which sets security and privacy rules for protected health information.
- **PCI DSS** — the Payment Card Industry Data Security Standard. The course is careful to note PCI DSS is _not_ a law; it is a contractual standard imposed by the payment-card brands on merchants who process cardholder data. This distinction (contractual vs. statutory) matters because the enforcement mechanism is totally different.

### The Ethics Discussion

The module's ethics framing hinged on one question: **"why is it acceptable to use your skills some ways and not others, and who gets to decide?"** The course argues that intent and authorization — not technical capability — are what separate the authorized researcher from the criminal. The same exploit, the same tool, the same skill: one use is a legally-protected research activity, the other is a crime. The difference is _who authorized it_ and _why_.

## What Stood Out to Me

Two things landed hard. First, the course's deliberate widening from "computer misuse law" to the surrounding regulatory landscape: it is not enough to know the anti-hacking statute; a modern professional also operates under GDPR-style data rules rectangles, HIPAA if in healthcare, and contractual standards like PCI DSS. The legal surface is much broader than "the computer crime law."

Second, the _contractual vs. statutory_ distinction with PCI DSS. It is easy to think "if it's mandated, it's a law." It is a useful professional reflex to check the enforcement mechanism — a real statute is enforced by the state; a contractual standard is enforced by the party you signed an agreement with. The course's treatment of this is a small example of the "check your assumptions" theme that runs through the whole plan.

And the ethics question is the one that matters most for this plan specifically. The **"On the Offense"** course — the next course in the fundamentals plan — is entirely about skills that overlap with what criminals do. The reason that course is legitimate, and not just glorified crime, traces directly back to this module's authorization-and-intent argument.

## Practical Connection

This is the module where my own boundary-setting becomes explicit rather than assumed. My lab is built on attacking systems I own or that are explicitly designed for it (DVWA, WebGoat, Metasploitable, my attack VMs). This module gave me the vocabulary to justify that boundary in the course's own terms: the attacks are _authorized_ (my infrastructure, or deliberate practice targets), the _intent_ is defensive learning, and the _authorization_ is unambiguous — which is precisely the line the CFAA/CMA framework uses to separate authorized research from crime.

The activity in this module asks for a description of your own country's computer-misuse law. That is the one activity in this course I will do as written, from a primary source, because it makes the abstract legal framework concrete for my own jurisdiction.

## Key Takeaways

- Computer-misuse law has a common shape across jurisdictions: criminalize unauthorized access and unauthorized modification/interference.
- The UK CMA, the US CFAA, the EU Directive, and the Budapest Convention all rest on that shared shape.
- Laws move slower than technology; amendments and case law stretch statutes written before the web.
- Beyond misuse laws, data-protection law (GDPR), sector rules (HIPAA), and contractual standards (PCI DSS) create a wider compliance surface.
- Authorization + intent, not technical skill, is what separates an authorized researcher from a criminal.
- Legality and ethics are different: an act can be legal and still wrong, or ethical and still illegal.

## What I Want to Explore Further

- The specific text of my own country's computer-misuse law and how it maps onto the CMA/CFAA shape (this is the module activity).
- How the UK's National Cyber Security Centre (part of GCHQ) operates under the Computer Misuse Act — the authorized state-actor case.
- The real-world tension between the CFAA's breadth and legitimate security research, including notable researcher cases.
- How GDPR's breach-notification duty (72 hours) actually changes incident response planning.

## Sources

- UK Government, _Computer Misuse Act 1990_: https://www.legislation.gov.uk/ukpga/1990/18/contents — VERIFIED
- US Department of Justice, _Computer Fraud and Abuse Act (18 U.S.C. § 1030) materials_: https://www.justice.gov/archives/opa/press-release/file/1507126/dl — VERIFIED
- Congressional Research Service, _Cybercrime: An Overview of the Federal Computer Fraud and Abuse Statute_ (R46536): https://www.congress.gov/crs_external_products/R/PDF/R46536/R46536.pdf — VERIFIED
- Council of Europe, _Budapest Convention on Cybercrime_: https://www.coe.int/en/web/cybercrime/the-budapest-convention — VERIFIED
- European Commission, _Directive 2013/40/EU on attacks against information systems_: https://eur-lex.europa.eu/legal-content/EN/TXT/?uri=CELEX%3A32013L0040 — VERIFIED
- NIST, _Cybersecurity Framework_: https://www.nist.gov/cyberframework — VERIFIED
