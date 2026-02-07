# NIST SP 800-63 (Digital Identity Guidelines)

## Definition

**NIST Special Publication 800-63** provides technical guidelines for digital identity services — defining Identity Assurance Levels (IAL), Authenticator Assurance Levels (AAL), and Federation Assurance Levels (FAL).

---

## The Three Assurance Dimensions

| Dimension | What It Measures | Levels |
|-----------|-----------------|--------|
| **IAL (Identity Assurance)** | Confidence in identity proofing | IAL1 (none), IAL2 (remote/in-person), IAL3 (in-person + biometric) |
| **AAL (Authenticator Assurance)** | Strength of authentication | AAL1 (single factor), AAL2 (multi-factor), AAL3 (hardware crypto) |
| **FAL (Federation Assurance)** | Security of federated identity assertions | FAL1, FAL2, FAL3 |

## IAL Mapping to eKYC

| Level | eKYC Equivalent | Method |
|-------|-----------------|--------|
| **IAL1** | No identity proofing | Self-asserted — not sufficient for financial services |
| **IAL2** | Standard eKYC | Remote: document + selfie + database check |
| **IAL3** | V-KYC or in-person | In-person with biometric verification |

---

## Key Takeaways

!!! success "Summary"
    - NIST 800-63 provides the **US government's identity assurance framework**
    - **IAL2** maps to standard eKYC — remote document + biometric + database verification
    - Widely referenced beyond US — influences global identity standards
    - Revised periodically — 800-63-4 (draft) updates for modern technology

---

## Related Articles

- [Identity Assurance Levels](../04-digital-identity/identity-assurance-levels.md)
- [Digital Identity Overview](../04-digital-identity/digital-identity-overview.md)
