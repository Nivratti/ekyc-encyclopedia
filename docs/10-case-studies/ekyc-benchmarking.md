# eKYC Performance Benchmarking

## Overview

How to evaluate eKYC vendors and measure system performance — POC design, metrics, and comparison methodology.

---

## POC Evaluation Framework

| Dimension | Metrics | Weight |
|-----------|---------|--------|
| **Accuracy** | STP rate, false acceptance rate, false rejection rate | 30% |
| **Document coverage** | Countries and document types supported | 15% |
| **Speed** | End-to-end latency (P50, P95) | 15% |
| **Security** | Liveness detection, injection prevention, certifications | 15% |
| **Integration** | SDK quality, API design, documentation | 10% |
| **Cost** | Per-verification price at volume | 10% |
| **Support** | SLA, response time, dedicated support | 5% |

## Testing Methodology

| Test | What It Measures |
|------|-----------------|
| **Golden set** | 500+ known-good and known-bad samples → measure accuracy |
| **Demographic coverage** | Test across age, ethnicity, gender → check for bias |
| **Attack testing** | Print, screen, mask, deepfake samples → measure security |
| **Document diversity** | All expected document types → check coverage |
| **Load testing** | Peak traffic simulation → measure latency under load |

---

## Key Takeaways

!!! success "Summary"
    - **Always test with your own data** — vendor benchmarks use ideal conditions
    - **Golden set** of known-good/known-bad samples is essential for accuracy measurement
    - **Demographic testing** reveals bias invisible in aggregate metrics
    - Weight accuracy and security highest — cost matters but shouldn't drive the decision

---

## Related Articles

- [Biometric Performance Metrics](../02-biometrics-face/biometric-performance-metrics.md)
- [A/B Testing for eKYC](../05-onboarding-workflow/ab-testing-ekyc.md)
