# India: Aadhaar-Based eKYC at Scale

## Overview

India's Aadhaar-based eKYC is the world's largest digital identity verification system — 100M+ monthly verifications across banking, telecom, and government services.

---

## Scale Metrics

| Metric | Value |
|--------|-------|
| **Total Aadhaar issued** | 1.4 billion |
| **Monthly authentications** | 200M+ (eKYC + authentication combined) |
| **eKYC methods** | OTP, biometric, offline XML, face |
| **Cost per verification** | ₹3-20 ($0.04-0.25) |
| **Response time** | < 3 seconds |
| **Regulated entities using** | All banks, NBFCs, telecom, insurance |

## Lessons Learned

| Lesson | Details |
|--------|---------|
| **Biometric exclusion** | Elderly/manual laborers fail fingerprint → need alternatives (OTP, face) |
| **Privacy concerns** | Supreme Court limited Aadhaar scope (2018 judgment) |
| **Offline mode** | Aadhaar offline XML enables verification without UIDAI API call |
| **Fraud evolution** | Biometric cloning attempts → led to liveness addition |

---

## Key Takeaways

!!! success "Summary"
    - Aadhaar eKYC demonstrates **population-scale** digital verification is achievable
    - **Multiple methods** (OTP, biometric, offline, face) are essential for universal coverage
    - **Privacy safeguards** (Supreme Court limits, data minimization) are critical for public trust
    - The model is being **replicated globally** — India Stack as reference architecture

---

## Related Articles

- [India Stack](../04-digital-identity/india-stack.md)
- [RBI KYC Master Direction](../07-regulations-standards/rbi-kyc-master-direction.md)
