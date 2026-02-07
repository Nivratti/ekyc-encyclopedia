# RBI KYC Master Direction

## Definition

The **RBI Master Direction on KYC** (updated periodically) is India's definitive regulation governing customer identification and verification for all Regulated Entities (REs) — banks, NBFCs, payment banks, and other financial institutions.

---

## Accepted eKYC Methods

| Method | How It Works | Assurance |
|--------|-------------|-----------|
| **Aadhaar OTP eKYC** | Customer enters Aadhaar number + OTP sent to registered mobile | Substantial |
| **Aadhaar biometric eKYC** | Fingerprint/iris matched against UIDAI database | High |
| **Aadhaar offline XML** | Customer downloads signed XML from UIDAI, shares with FI | Substantial |
| **Video-based Customer Identification (V-CIP)** | Live video call with trained RE official | High |
| **DigiLocker** | Pull verified documents from government repository | Substantial |
| **cKYC download** | Download existing KYC from central registry (CERSAI) | Substantial |
| **OVD-based digital** | Officially Valid Document scanned + verified | Varies |

---

## Key Requirements

| Requirement | Details |
|-------------|---------|
| **Risk categorization** | Customers must be categorized as low/medium/high/very high risk |
| **CDD for all** | Customer Due Diligence mandatory for all account types |
| **EDD for high-risk** | Enhanced Due Diligence for PEPs, high-risk countries, complex structures |
| **Beneficial ownership** | UBO identification for non-individual accounts |
| **Record keeping** | 5 years after account closure — all KYC records |
| **Re-KYC frequency** | High risk: 2 years, Medium: 8 years, Low: 10 years |
| **Suspicious transaction reporting** | File STR with FIU-IND within 7 days |
| **cKYC upload** | All REs must upload KYC to CERSAI |

## V-CIP (Video KYC) Specific Requirements

| Requirement | Details |
|-------------|---------|
| **Agent** | Must be RE official (not outsourced) |
| **Recording** | Full video recorded, stored securely |
| **Geo-tagging** | GPS location captured |
| **Aadhaar OTP** | Must be verified during session |
| **Face match** | Customer face matched against OVD photo |
| **Randomized questions** | To verify live interaction (not pre-recorded) |
| **Concurrent sessions** | Agent cannot handle multiple sessions |

---

## Key Takeaways

!!! success "Summary"
    - RBI KYC Master Direction is **the definitive reference** for eKYC in India
    - **7 accepted eKYC methods** — Aadhaar-based methods dominate
    - **V-CIP** has the most detailed requirements — live video, agent, recording, geo-tag, Aadhaar OTP
    - **Risk-based approach** mandated — different CDD levels for different risk categories
    - **cKYC upload mandatory** — all REs must contribute to central registry
    - **5-year record retention** after account closure

---

## Related Articles

- [India DPDP Act](india-dpdp-act.md)
- [India Stack](../04-digital-identity/india-stack.md)
- [Video KYC](../01-identity-verification/vkyc-video-kyc.md)
- [Central KYC (cKYC)](../01-identity-verification/ckyc-central-kyc.md)
