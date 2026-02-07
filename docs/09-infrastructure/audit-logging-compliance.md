# Audit Logging & Compliance

## Definition

Immutable, comprehensive logging of all eKYC operations — required for regulatory audit, fraud investigation, and compliance demonstration.

---

## What Must Be Logged

| Event | Details Logged |
|-------|---------------|
| **Verification initiated** | Session ID, timestamp, client, user identifier |
| **Document processed** | Document type, OCR results, forensic scores, authenticity decision |
| **Face processed** | Liveness score, match score, decision |
| **Screening performed** | Sanctions/PEP results, data source, timestamp |
| **Decision made** | Auto-approve/reject/review, reason, model versions, scores |
| **Manual review** | Agent ID, decision, reason, duration |
| **Data access** | Who accessed what biometric data, when, why |
| **Data deletion** | What was deleted, when, by whom/automation |

## Log Requirements

| Requirement | Implementation |
|-------------|---------------|
| **Immutability** | Write-once storage (S3 Object Lock, WORM) |
| **Retention** | 5+ years (matching AML record-keeping) |
| **Searchability** | Indexed for quick regulatory query response |
| **Tamper evidence** | Hash chains or blockchain-based integrity verification |
| **Access control** | Only compliance/audit team can query full logs |

---

## Key Takeaways

!!! success "Summary"
    - **Every verification decision** must be logged with full audit trail — regulatory requirement
    - Logs must be **immutable** — prevent tampering after the fact
    - **5-year minimum retention** aligned with AML record-keeping requirements
    - **Data access logging** is critical for GDPR/DPDP compliance — prove who accessed biometric data

---

## Related Articles

- [Building a Compliance Program](../07-regulations-standards/building-compliance-program.md)
- [Security Architecture](security-architecture.md)
