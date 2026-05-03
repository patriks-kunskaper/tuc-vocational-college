# TLS 1.3 and ECDHE Key Exchange

**Network Security module — Cybersecurity program, April 2026**

---

## What this is

A technical deep dive into how TLS 1.3 establishes a secure connection — from TCP handshake to encrypted traffic — with a focus on the ECDHE key exchange mechanism and symmetric key derivation.

The assignment asked for an explanation of classical Diffie-Hellman. Classical DH is not what runs in production: TLS 1.3 replaced it with ECDHE in 2018, and understanding the protocol as it actually operates meant covering the full handshake. This document is the result of following that thread.

Written as a course assignment during the Network Security module of a professional cybersecurity program in Sweden.

---

## Why it matters

Every HTTPS connection you make relies on this process running silently in the background. Understanding it is foundational for anyone working in network security, security hardening, or cryptographic protocol analysis.

The two documents here approach the same material at different levels of detail — one for depth, one for clarity.

---

## Documents

### `TLS-handskakning-ECDHE.pdf` — Main assignment (Swedish)
A phase-by-phase technical walkthrough covering:

- TCP 3-way handshake and ClientHello
- ServerHello, certificate authentication, and ECDHE parameter exchange
- ECDHE key exchange and shared secret derivation
- HKDF-based symmetric key derivation (client\_write\_key / server\_write\_key)
- AES-256-GCM encryption of session traffic
- Post-quantum threat context: Shor's algorithm, harvest-now-decrypt-later, NIST PQC standards (Kyber, Dilithium)

### `TLS-presentation.pdf` — Summary slides (Swedish)
A compressed three-step overview designed for communication rather than examination. Demonstrates the same material stripped to its essential logic — intended to show how complex cryptographic processes can be made accessible without losing accuracy.

---

## Key concepts covered

- Discrete logarithm problem as the security foundation of Diffie-Hellman
- Why ECDHE replaced classical DH in TLS 1.3: smaller keys, faster computation, forward secrecy by design
- How ephemeral private values (a, b) ensure forward secrecy
- HKDF as a one-way key derivation function using shared secret + nonce salting
- Certificate chain verification via CA signature and SHA-256 hash comparison
- The quantum threat to ECDHE and the post-quantum cryptography transition

---

## The key exchange in notation

Public parameters (pre-installed in all browsers):

```
p  = 256-bit prime
G  = fixed base point on the curve (x, y)
n  = upper bound for private values
```

Browser generates locally:
```
a  = random integer, 1 ≤ a ≤ n-1  (private, never transmitted)
A  = G × a (mod p)                 (public, sent to server)
```

Server generates locally:
```
b  = random integer, 1 ≤ b ≤ n-1  (private, never transmitted)
B  = G × b (mod p)                 (public, sent to browser in ServerHello)
```

Shared secret derivation:
```
Browser computes:  S = B × a (mod p)
Server computes:   S = A × b (mod p)
Both arrive at:    S = same point on the curve (x, y)
Shared secret:     Sx = x-coordinate of S
```

Key derivation (HKDF):
```
Salt               = client_random + server_random
PRK                = HMAC-SHA256(Salt, Sx)
client_write_key   = HMAC-SHA256(PRK, "client key")
server_write_key   = HMAC-SHA256(PRK, "server key")
```

Traffic is then encrypted and decrypted using AES-256-GCM with the respective write keys.

---

## One thing worth noting

The security of ECDHE rests on the discrete logarithm problem being computationally infeasible to reverse. A sufficiently powerful quantum computer running Shor's algorithm would break this assumption. NIST finalized its first post-quantum cryptography standards in 2024. This assignment covers that transition in its closing section.

---

## Context

Part of an ongoing portfolio documenting applied cryptography, network security, and threat-informed security design. Program trajectory leads toward security hardening, IAM, and LIA internship placements in the Stockholm area.
