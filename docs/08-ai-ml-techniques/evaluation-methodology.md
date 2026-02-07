# Evaluation Methodology

## Definition

How to properly evaluate eKYC ML models — test set design, cross-validation, statistical significance, and avoiding common pitfalls that lead to overestimated performance.

---

## Evaluation Principles

| Principle | Why It Matters |
|-----------|---------------|
| **Held-out test set** | Never test on data seen during training |
| **Cross-dataset evaluation** | Same-dataset results overestimate real-world performance |
| **Demographic stratification** | Report performance per demographic group |
| **Statistical significance** | Ensure differences between models are real (not random) |
| **Production-representative** | Test data should match production conditions |

## Liveness Evaluation Protocols

| Protocol | Method |
|----------|--------|
| **Intra-dataset** | Train/test split within same dataset — baseline only |
| **Cross-dataset (leave-one-out)** | Train on 3 datasets, test on 4th — measures generalization |
| **Cross-attack** | Train on known attacks, test on unseen attack types |
| **Cross-device** | Train on some devices, test on new devices |

## Common Pitfalls

| Pitfall | Consequence |
|---------|------------|
| **Data leakage** | Same person in train and test → inflated accuracy |
| **Evaluation on same domain** | Model memorizes dataset, fails in production |
| **Ignoring demographics** | 99% overall accuracy hiding 80% accuracy for some groups |
| **Cherry-picking metrics** | Reporting best metric while hiding poor ones |
| **Small test set** | Results not statistically significant |

---

## Key Takeaways

!!! success "Summary"
    - **Cross-dataset evaluation** is the only reliable measure of eKYC model quality
    - **Per-demographic reporting** is essential for fairness — and increasingly required by regulation
    - **Data leakage** (same person in train/test) is the most common evaluation mistake
    - Report **confidence intervals** — point estimates without uncertainty are misleading

---

## Related Articles

- [Biometric Performance Metrics](../02-biometrics-face/biometric-performance-metrics.md)
- [Error Analysis](error-analysis-ekyc.md)
- [Biometric Fairness & Bias](../02-biometrics-face/biometric-fairness-bias.md)
