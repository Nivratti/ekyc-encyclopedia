# Consortium Data & Fraud Sharing

## Definition

**Consortium data sharing** enables multiple financial institutions to share fraud signals and verified identity data — dramatically improving detection by revealing patterns invisible to any single institution.

---

## What's Shared

| Data Type | Purpose | Privacy Approach |
|-----------|---------|-----------------|
| **Known fraud indicators** | Alert other institutions to confirmed fraud | Anonymized/hashed identifiers |
| **Device fingerprints** | Link fraud attempts across institutions | Device hash only |
| **Face embeddings** | Cross-institutional 1:N dedup | Template-protected embeddings |
| **Velocity data** | Detect rapid multi-institution applications | Aggregated counts |
| **Confirmed mule accounts** | Block known mule accounts | Account hashes |

## Consortium Models

| Model | Example | How It Works |
|-------|---------|-------------|
| **Industry utility** | UK CIFAS, US Early Warning Services | Central database, all members contribute and query |
| **Platform-mediated** | Alloy, LexisNexis, Socure | Platform aggregates data from all clients |
| **Bilateral** | Bank-to-bank agreements | Direct data sharing between specific institutions |
| **Blockchain-based** | Emerging approaches | Decentralized sharing with privacy-preserving computation |

---

## Key Takeaways

!!! success "Summary"
    - Cross-institutional data sharing **multiplies fraud detection power** — catches fraud rings, mules, velocity attacks
    - **Privacy-preserving techniques** (hashing, differential privacy) enable sharing without exposing raw PII
    - **CIFAS (UK)** and **Early Warning Services (US)** are the largest operational consortiums
    - Platform-mediated sharing (via eKYC vendors like Alloy, Socure) is growing fastest

---

## Related Articles

- [Network Analysis for Fraud](network-analysis-fraud.md)
- [Fraud Rings](fraud-rings-organized.md)
