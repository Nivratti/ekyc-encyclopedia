# Data Encryption Strategy

## Definition

Comprehensive encryption approach for eKYC — covering data at rest, in transit, in processing, and key management.

---

## Encryption Requirements

| State | Standard | Implementation |
|-------|----------|---------------|
| **At rest** | AES-256 | S3 SSE-KMS, RDS encryption, encrypted EBS |
| **In transit** | TLS 1.3 | All API calls, SDK-server communication |
| **In processing** | Optional — secure enclaves | AWS Nitro, Azure Confidential Computing |
| **Key management** | HSM-backed | AWS KMS, GCP Cloud KMS, Azure Key Vault |
| **Client-side** | SDK encryption | Encrypt images before upload |

## Key Management

| Approach | Security | Operational Complexity |
|----------|---------|----------------------|
| **Provider-managed keys** | Standard | Low |
| **Customer-managed keys (CMK)** | Higher — customer controls key | Medium |
| **Bring Your Own Key (BYOK)** | Highest — HSM-generated keys | High |

---

## Key Takeaways

!!! success "Summary"
    - **AES-256 at rest + TLS 1.3 in transit** is the minimum baseline
    - **Enterprise clients** typically require **customer-managed keys (CMK)**
    - **Key rotation** must be automated — annual rotation at minimum
    - Consider **field-level encryption** for biometric data — additional protection beyond full-disk encryption

---

## Related Articles

- [Security Architecture](security-architecture.md)
- [Biometric Data Protection](../07-regulations-standards/biometric-data-protection.md)
