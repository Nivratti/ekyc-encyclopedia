# Decentralized Identifiers (DIDs)

## Definition

**DIDs (Decentralized Identifiers)** are a W3C standard for globally unique identifiers that are created, owned, and controlled by the individual — not by any central authority. DIDs are the identifier layer that complements Verifiable Credentials.

---

## DID Structure

```
did:method:method-specific-identifier
```

| Example | DID Method | Where It Resolves |
|---------|-----------|-------------------|
| `did:web:example.com` | Web | DNS / HTTPS |
| `did:key:z6MkhaXg...` | Key | Self-contained (public key in DID) |
| `did:ion:EiAnK...` | ION | Bitcoin blockchain (Layer 2) |
| `did:ethr:0xb9c5...` | Ethereum | Ethereum blockchain |
| `did:sov:WRfXPg...` | Sovrin | Sovrin blockchain |

## DID Document

A DID resolves to a **DID Document** containing:

| Field | Purpose |
|-------|---------|
| **Public keys** | For verifying signatures on VCs |
| **Authentication methods** | How the DID owner proves control |
| **Service endpoints** | Where to send messages to DID owner |

---

## Key Takeaways

!!! success "Summary"
    - DIDs are **self-owned identifiers** — no central authority can revoke or control them
    - Multiple DID methods exist — from blockchain-based to simple web-hosted
    - DIDs pair with **Verifiable Credentials** to create complete decentralized identity
    - **did:web** is the most pragmatic for enterprise eKYC (no blockchain needed)
    - EUDI Wallet will likely use DIDs as the underlying identifier mechanism

---

## Related Articles

- [W3C Verifiable Credentials](w3c-verifiable-credentials.md)
- [Self-Sovereign Identity](self-sovereign-identity.md)
