# Biometric Fairness & Bias

## Definition

**Biometric fairness** refers to the equitable performance of biometric systems across different demographic groups. Bias occurs when a system performs significantly better or worse for certain populations based on age, gender, ethnicity, or skin tone.

---

## Documented Bias in Face Systems

### NIST FATE Findings

| Demographic Factor | Finding |
|-------------------|---------|
| **Skin tone** | Some algorithms show 10-100x higher false positive rates for darker skin |
| **Gender** | Higher false positive rates for women in some algorithms |
| **Age** | Higher error rates for elderly (65+) and very young (< 18) |
| **Country of birth** | Performance varies significantly by nationality/ethnicity |

### Root Causes

| Cause | Details |
|-------|---------|
| **Training data imbalance** | Datasets overrepresent lighter-skinned, younger faces |
| **Lighting bias** | Cameras and imaging optimized for lighter skin tones |
| **Annotation bias** | Subjective labeling in training data |
| **Architecture bias** | Features that work well for majority group may not generalize |
| **Evaluation bias** | Benchmarks not representative of diverse populations |

---

## Fairness Metrics

| Metric | What It Measures |
|--------|-----------------|
| **FMR ratio** | Max FMR / Min FMR across demographic groups (closer to 1 = fairer) |
| **FNMR ratio** | Max FNMR / Min FNMR across groups |
| **Equalized odds** | Equal TPR and FPR across groups |
| **Demographic parity** | Equal positive prediction rates across groups |
| **Gini coefficient** | Overall inequality of error distribution across groups |

---

## Mitigation Strategies

| Strategy | Approach |
|----------|----------|
| **Balanced training data** | Ensure representative data across demographics |
| **Per-group threshold tuning** | Different thresholds per demographic to equalize error rates |
| **Fairness-aware training** | Add fairness constraints to loss function |
| **Data augmentation** | Synthetic generation of underrepresented groups |
| **Regular bias audits** | Periodic evaluation against diverse test sets |
| **Diverse evaluation sets** | Test on demographically balanced datasets (BFW, RFW) |

---

## Key Takeaways

!!! success "Summary"
    - Biometric bias is **real, documented, and measurable** — NIST FATE provides evidence
    - Root causes: **training data imbalance**, lighting bias, evaluation gaps
    - **Per-group threshold tuning** is the most practical immediate mitigation
    - **Balanced training data** is the most impactful long-term solution
    - Regulators (EU AI Act) are beginning to **mandate fairness testing** for biometric systems
    - For eKYC: bias means some demographics are **systematically more likely to be rejected** — a fairness and business problem

---

## Related Articles

- [NIST FRVT](nist-frvt.md)
- [Biometric Performance Metrics](biometric-performance-metrics.md)
- [Face Recognition Architectures](face-recognition-architectures.md)
