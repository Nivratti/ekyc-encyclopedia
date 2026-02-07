# Identity Assurance Levels

## Definition

**Identity Assurance Levels (IALs)** define the degree of confidence that a claimed identity is the person's true identity. Different activities require different assurance levels — opening a basic prepaid wallet needs less assurance than opening a private banking account.

---

## NIST SP 800-63 (USA Standard)

| Level | Description | Verification Required | eKYC Equivalent |
|-------|------------|----------------------|-----------------|
| **IAL1** | No identity proofing | Self-assertion only | — |
| **IAL2** | Remote or in-person identity proofing | Document + selfie + database check | Standard eKYC |
| **IAL3** | In-person identity proofing | Physical presence + biometric | V-KYC or in-person |

## eIDAS Assurance Levels (EU)

| Level | Description | Example |
|-------|------------|---------|
| **Low** | Minimal assurance | Username + password registration |
| **Substantial** | Moderate assurance | eKYC with document + biometric |
| **High** | Highest assurance | eID with NFC chip + biometric + government PKI |

## Mapping to eKYC Methods

| Assurance | eKYC Methods | Use Cases |
|-----------|-------------|-----------|
| **Low** | Database check only, basic OTP | Prepaid cards < €150, basic accounts |
| **Substantial** | Document + selfie + liveness + DB verification | Standard bank accounts, lending |
| **High** | NFC chip + biometric + V-KYC or in-person | Private banking, large loans, PEPs |

---

## Key Takeaways

!!! success "Summary"
    - Assurance levels create a **framework for proportionate verification** — higher risk = higher assurance required
    - **NIST IAL1/2/3** and **eIDAS Low/Substantial/High** are the two dominant frameworks
    - Most standard eKYC corresponds to **IAL2 / Substantial** — document + biometric + database
    - **NFC chip reading** pushes assurance to **High** — cryptographically signed government data

---

## Related Articles

- [Digital Identity Overview](digital-identity-overview.md)
- [eIDAS & EU Digital Identity](eidas-eu-digital-identity.md)
- [Risk-Based Approach](../01-identity-verification/kyc-know-your-customer.md)
