# Module 06 — Introducing cryptography

> **Course:** Cybersecurity: On the Defense (IBM SkillsBuild)
> **Module:** 6 of 7
> **Status:** 100% COMPLETE

## What I Learned

Cryptography is the mathematical engine underneath almost everything else in security. This module backs the camera out and asks the conceptual questions: what is cryptography, why does it matter, and how does it relate to the CIA triad? It stays conceptual (it's an _introduction_), but the framing it builds is the foundation for everything that follows.

Core ideas:

- **What cryptography is.** The practice of **secure communication in the presence of adversaries** — protecting data by transforming it so that only the intended parties can read it. The module grounds it in the **CIA triad** (which I first met in the Intro course): **confidentiality** (secrecy), **integrity** (unchanged/correct), and **availability** (accessible when needed). Cryptography is the set of techniques that protects those three properties of data.

- **Encryption.** The core mechanism: transforming **plaintext** into **ciphertext** using an **encryption key**, and back again with the right key. The two families:
  - **Symmetric encryption** — the _same_ key encrypts and decrypts. Fast and simple, but the hard problem is **key distribution**: how do two parties share a secret key without someone intercepting it?
  - **Asymmetric (public-key) cryptography** — uses a **key pair**: a **public key** (shared freely) and a **private key** (kept secret). Encrypt with the public key, decrypt only with the private key. This solves the key-distribution problem symmetric crypto has, at the cost of being slower.
  - The module's activity walks through the **order of steps in an asymmetric encryption exchange** — a nice test of actually understanding _who_ does _what_ with _which key_.

- **Hashing.** A **one-way** function that turns data of any size into a fixed-length **digest**. You can't reverse it, and any change in the input produces a completely different digest. Hashing is how you verify **integrity** (did the file change?) without revealing the data — used for password storage, file verification, and digital signatures.

- **Digital signatures.** The integrity + authenticity cousin of encryption: a **hash of the data encrypted with the sender's private key**. Anyone with the sender's public key can verify it — proving the data is unchanged and genuinely from the sender. This is how email signing, software signing, and document authentication work.

- **Quantum encryption (a taste of the future).** The module looks ahead: quantum computers threaten to break current public-key algorithms (like RSA and ECC) because they can factor/be solved far faster than classical computers. **Quantum/post-quantum cryptography** is the response — new algorithms that resist quantum attacks. This is the hook that connects forward to the "Your Future" course.

- **Cryptography in the real world** is everywhere: HTTPS/TLS, Wi-Fi encryption (WPA), disk encryption, password hashing, secure messaging. It protects data **at rest** and **in transit** — the two places data lives.

## What Stood Out to Me

The **asymmetric encryption activity** is where it clicked for me. Ordering the steps made the _conceptual_ idea concrete: the sender grabs the recipient's **public** key, encrypts the message with it, sends the ciphertext — and only the recipient's **private** key decrypts it, so interception en route is useless. That single ordering is the entire basis of HTTPS and secure email, and actually working through the sequence (rather than just being told "public key encrypts") made the attack model obvious: the weakness isn't the cipher, it's whether the public key you grabbed is really the recipient's (the MITM problem, which ties back to trust/identity and forward to threat intelligence).

I also liked the **hash-vs-encrypt distinction**, because conflating them is a classic newbie trap (and exactly the kind of conceptual clarity I want in my own notes): encryption gives you _secrecy_ (reversible with a key), hashing gives you _integrity_ (irreversible, tamper-evident). Same triangle, different corner.

## Practical Connection

This module's concepts are things I actually use constantly without having named them:

- **SSH** (which I use in every lab) is asymmetric crypto in action — my keypair, the server's public key, the handshake. Now I can trace _what_ each key does in the exchange.
- **HTTPS/TLS** — the padlock in the browser is the asymmetric exchange from the activity, running invisibly.
- **Password hashing** — systems store a digest, not the password; this is why a password _file_ leak is measured in how hard the hashes are to crack (a direct hook to the offense course's hash-cracking material).
- **Git** itself uses SHA-1/SHA-256 hashes to guarantee object integrity — the "content-addressed" property that my whole repo structure leans on.

So this module retroactively explains mechanisms I've been using all session.

## Key Takeaways

- **Cryptography protects all three corners of the CIA triad** — confidentiality (encryption), integrity (hashing/signatures), availability (access control layers).
- **Symmetric = one shared key, fast, key-distribution is the hard problem.**
- **Asymmetric = public/private keypair that solves key distribution** at the cost of speed — the basis of HTTPS, SSH, email.
- **Hash = one-way, fixed-length, tamper-evident** — integrity and password storage.
- **Digital signature = hash encrypted with the sender's private key** — authenticity + integrity.
- **Quantum computers threaten current public-key crypto**; post-quantum cryptography is the emerging answer.

## What I Want to Explore Further

- **Ordering the asymmetric exchange** was the module activity — I want to push it further: actually generate an SSH/RSA keypair and encrypt/decrypt a file with `openssl` to walk the steps hands-on.
- Learning the **actual math behind RSA/ECC** at an intuitive level (why multiplying is easy but factoring is hard — the asymmetry the whole field rests on).
- Understanding **quantum/post-quantum algorithms** (like lattice-based or NIST's standardized ones) deeply enough to say why the threat is real and not just a headline.

## Sources

- IBM SkillsBuild, _Cybersecurity: On the Defense_ — Module 6 (introducing cryptography)
- Activity: order the steps of an asymmetric encryption exchange (IBM SkillsBuild)
- Cross-references: Intro course (CIA triad), offense course (hash cracking, HTTPS/TLS, SSH in labs)
