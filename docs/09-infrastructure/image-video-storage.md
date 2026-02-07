# Image & Video Storage

## Definition

Storage strategy for eKYC images (document photos, selfies, liveness videos) — balancing access speed, cost, encryption, and regulatory retention requirements.

---

## Storage Requirements

| Data Type | Size | Access Pattern | Encryption |
|-----------|------|---------------|-----------|
| **Document image** | 1-5 MB | Frequent during processing, rare after | AES-256 at rest |
| **Selfie image** | 0.5-2 MB | Frequent during processing, rare after | AES-256 at rest |
| **Liveness video** | 5-20 MB | Processing only, then archive | AES-256 at rest |
| **Face embedding** | 2 KB | Frequent (dedup queries) | Encrypted, template-protected |
| **OCR results** | < 10 KB | Frequent | Encrypted |

## Estimated Storage (1M verifications/month)

| Component | Per Verification | Monthly Total |
|-----------|-----------------|---------------|
| **Images** | ~10 MB | ~10 TB |
| **Videos** | ~15 MB (if captured) | ~15 TB |
| **Metadata + results** | ~50 KB | ~50 GB |
| **5-year retention** | ~25 MB | ~1.5 PB cumulative |

---

## Key Takeaways

!!! success "Summary"
    - At scale, image/video storage grows **10-25 TB/month** — cost management is essential
    - **Lifecycle policies** (hot → cold) reduce storage costs by 60-80%
    - All images must be **encrypted at rest** (AES-256) with **customer-managed keys** for enterprise
    - Consider storing **embeddings instead of raw images** where regulations allow — 1000x smaller

---

## Related Articles

- [Data Pipeline Architecture](data-pipeline-architecture.md)
- [Biometric Data Protection](../07-regulations-standards/biometric-data-protection.md)
