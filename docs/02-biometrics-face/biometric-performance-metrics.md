# Biometric Performance Metrics

## Definition

Standardized metrics for measuring the accuracy of biometric systems. These metrics are essential for comparing models, setting thresholds, and meeting certification requirements.

---

## Face Recognition Metrics

| Metric | Full Name | What It Measures | Ideal |
|--------|-----------|-----------------|-------|
| **FAR / FMR** | False Accept / Match Rate | % of impostors incorrectly accepted | Lower is better |
| **FRR / FNMR** | False Reject / Non-Match Rate | % of genuine users incorrectly rejected | Lower is better |
| **EER** | Equal Error Rate | Point where FAR = FRR | Lower is better |
| **TAR@FAR** | True Accept Rate at fixed FAR | Acceptance rate at security operating point | Higher is better |
| **d'** | Decidability | Separation between genuine and impostor score distributions | Higher is better |

### ROC and DET Curves

- **ROC (Receiver Operating Characteristic)**: Plots TAR vs FAR — area under curve (AUC) measures overall performance
- **DET (Detection Error Tradeoff)**: Plots FRR vs FAR on normal deviate scale — standard in biometrics (ISO 19795)

---

## Liveness / PAD Metrics (ISO 30107-3)

| Metric | Full Name | What It Measures | Ideal |
|--------|-----------|-----------------|-------|
| **APCER** | Attack Presentation Classification Error Rate | % of attacks that fool the system | Lower is better |
| **BPCER** | Bona Fide Presentation Classification Error Rate | % of real users incorrectly rejected as spoof | Lower is better |
| **ACER** | Average Classification Error Rate | (APCER + BPCER) / 2 | Lower is better |

### APCER Calculation

APCER is calculated **per PAI species** (per attack type):

```
APCER_PAI = (Number of attack presentations classified as bona fide) / (Total attack presentations of that PAI species)
```

The overall APCER is typically the **maximum APCER** across all PAI species (worst-case attack type).

---

## End-to-End eKYC Metrics

| Metric | What It Measures | Typical Target |
|--------|-----------------|----------------|
| **STP Rate** | Straight-Through Processing — % auto-approved | > 80% |
| **First-attempt success** | Users passing on first try | > 75% |
| **Completion rate** | Users who finish the full flow | > 85% |
| **Average verification time** | End-to-end duration | < 60 seconds |
| **Manual review rate** | % requiring human review | < 15% |

---

## Key Takeaways

!!! success "Summary"
    - **FAR and FRR** are the fundamental recognition metrics — always in tension (threshold tradeoff)
    - **EER** is the single-number model quality summary — lower is better
    - **APCER, BPCER, ACER** are the ISO 30107-3 standard for liveness/PAD evaluation
    - APCER should be reported **per PAI species** — overall APCER uses the worst-case species
    - **End-to-end metrics** (STP rate, completion rate) matter as much as model accuracy in production

---

## Related Articles

- [Face Matching & Thresholds](face-matching-thresholds.md)
- [NIST FRVT](nist-frvt.md)
- [ISO 30107 — PAD Testing](iso-30107-pad-testing.md)
- [Biometric Fairness & Bias](biometric-fairness-bias.md)
