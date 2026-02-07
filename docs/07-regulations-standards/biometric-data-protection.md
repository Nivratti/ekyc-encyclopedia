# Biometric Data Protection

## Definition

Specific requirements for protecting biometric data collected during eKYC — face images, embeddings, fingerprints, and iris templates — across different regulatory frameworks.

---

## What Counts as Biometric Data

| Data Type | Biometric? | Notes |
|-----------|-----------|-------|
| **Face photograph** | Yes (when used for identification) | GDPR: biometric only if processed to identify |
| **Face embedding (512-d vector)** | Yes | Derived from biometric, still biometric |
| **Fingerprint template** | Yes | Minutiae-based representation |
| **Iris code** | Yes | Mathematical representation of iris |
| **Voice recording** | Yes (when used for identification) | Context-dependent |
| **Document photo** | No (usually) | Photo of document, not biometric identification |
| **Liveness score** | No | Derived score, not biometric data itself |

---

## Protection Requirements

| Requirement | Implementation |
|-------------|---------------|
| **Encryption at rest** | AES-256 for stored biometric templates |
| **Encryption in transit** | TLS 1.3 for all biometric data transfers |
| **Access control** | Role-based access, principle of least privilege |
| **Audit logging** | Log all access to biometric data |
| **Retention limits** | Delete when purpose fulfilled (subject to AML retention) |
| **Template protection** | Cancelable biometrics, encrypted templates |
| **Breach notification** | Immediate notification per applicable law |
| **Data minimization** | Store embeddings instead of raw images where possible |

---

## Key Takeaways

!!! success "Summary"
    - Biometric data is the **most sensitive data** in eKYC — highest protection level across all jurisdictions
    - **Face embeddings are biometric data** — same protection as raw images
    - **Encryption (AES-256 at rest, TLS 1.3 in transit)** is the minimum baseline
    - **Template protection** (cancelable biometrics) provides defense against database breaches
    - **Data minimization**: prefer storing embeddings over raw face images

---

## Related Articles

- [GDPR & eKYC](gdpr-ekyc.md)
- [Template Protection](../02-biometrics-face/template-protection.md)
- [Global Privacy Laws](global-privacy-laws-ekyc.md)
