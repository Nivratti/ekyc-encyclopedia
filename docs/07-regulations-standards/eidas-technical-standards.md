# eIDAS Technical Standards

## Definition

Technical standards underpinning the **eIDAS regulation** — trust services, qualified electronic signatures, and the assurance level framework for electronic identification.

---

## Key Standards

| Standard | What It Covers |
|----------|---------------|
| **ETSI EN 319 411** | Trust Service Provider policy requirements |
| **ETSI EN 319 421** | Time-stamping authority requirements |
| **ETSI TS 119 431** | Trust Service Provider practices |
| **ISO 29115** | Entity authentication assurance framework (basis for eIDAS LoA) |
| **ETSI TS 119 461** | Electronic identity proofing — **directly covers eKYC methods** |

## ETSI TS 119 461 (Identity Proofing)

Directly relevant to eKYC — defines acceptable methods for remote identity proofing:

| Method | Assurance Level |
|--------|----------------|
| **Document + live photo + face comparison** | Substantial |
| **NFC chip reading + face comparison** | High |
| **Video identification (V-KYC)** | Substantial-High |
| **Qualified electronic signature** | High |

---

## Key Takeaways

!!! success "Summary"
    - **ETSI TS 119 461** is the most relevant eIDAS technical standard for eKYC
    - Maps eKYC methods to eIDAS assurance levels (Low/Substantial/High)
    - **NFC chip + biometric** achieves "High" assurance — the gold standard
    - These standards will govern **EUDI Wallet** credential issuance requirements

---

## Related Articles

- [eIDAS & EU Digital Identity](../04-digital-identity/eidas-eu-digital-identity.md)
- [Identity Assurance Levels](../04-digital-identity/identity-assurance-levels.md)
