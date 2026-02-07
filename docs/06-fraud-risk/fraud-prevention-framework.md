# Fraud Prevention Framework

## Definition

A **layered defense framework** that combines multiple fraud prevention signals at different stages — pre-verification, during verification, and post-verification — for comprehensive protection.

---

## The Three-Layer Defense

```mermaid
graph TD
    subgraph "Layer 1: Pre-Verification"
        A1[Device fingerprinting]
        A2[IP/geo risk assessment]
        A3[Email/phone intelligence]
        A4[Velocity checks]
    end

    subgraph "Layer 2: During Verification"
        B1[Face liveness / PAD]
        B2[Document forensics & liveness]
        B3[Face matching]
        B4[Sanctions/PEP screening]
        B5[1:N face deduplication]
        B6[Database verification]
    end

    subgraph "Layer 3: Post-Verification"
        C1[Transaction monitoring]
        C2[Behavioral biometrics]
        C3[Re-authentication triggers]
        C4[Network analysis]
        C5[Periodic re-KYC]
    end

    A1 & A2 & A3 & A4 --> D[Pre-score]
    D --> B1 & B2 & B3 & B4 & B5 & B6
    B1 & B2 & B3 & B4 & B5 & B6 --> E[Verification score]
    E --> C1 & C2 & C3 & C4 & C5
    C1 & C2 & C3 & C4 & C5 --> F[Ongoing risk score]

    style D fill:#F57F17,color:#000
    style E fill:#4051B5,color:#fff
    style F fill:#2E7D32,color:#fff
```

## Defense by Attack Type

| Attack | Layer 1 | Layer 2 | Layer 3 |
|--------|---------|---------|---------|
| **Stolen document + photo** | Device risk | Liveness detection | — |
| **Deepfake + injection** | Emulator/root detection | Injection prevention | — |
| **Synthetic identity** | Velocity, device reuse | Database verification, dedup | Network analysis |
| **Fraud ring** | Shared device/IP detection | Document similarity | Cross-institution linking |
| **Money mule** | — | Normal eKYC passes | Transaction monitoring |
| **Account takeover** | — | — | Behavioral change detection |

---

## Key Takeaways

!!! success "Summary"
    - **No single layer catches all fraud** — layered defense is essential
    - **Pre-verification** (device, IP) is the cheapest gate — reject obvious fraud before expensive processing
    - **During verification** (liveness, forensics, screening) is the core eKYC defense
    - **Post-verification** (monitoring, behavioral) catches fraud that passes initial checks
    - Each fraud type requires **different layers** — synthetic identity needs post-verification network analysis

---

## Related Articles

- [Identity Fraud Overview](identity-fraud-overview.md)
- [Risk Scoring Engines](risk-scoring-engines.md)
- [Decision Engine Architecture](../05-onboarding-workflow/decision-engine-architecture.md)
