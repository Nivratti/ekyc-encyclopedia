# Model Drift & Retraining

## Definition

**Model drift** occurs when a production model's performance degrades over time due to changes in input data distribution, new attack types, or evolving user demographics.

---

## Types of Drift

| Type | Cause | Example in eKYC |
|------|-------|-----------------|
| **Data drift** | Input distribution changes | New phone models with different cameras |
| **Concept drift** | Relationship between input and label changes | New attack type not in training data |
| **Label drift** | Class distribution changes | Spoof ratio increases due to new tool availability |
| **Upstream drift** | Changes in preprocessing | SDK update changes image quality/format |

## Detection Methods

| Method | How It Works |
|--------|-------------|
| **Score distribution monitoring** | Track model output distribution — shift indicates drift |
| **Performance monitoring** | Track accuracy metrics (requires delayed ground truth) |
| **Population Stability Index (PSI)** | Compare current vs baseline feature distributions |
| **Statistical tests** | KS test, chi-squared test on feature/score distributions |

## Retraining Strategies

| Strategy | When to Use |
|----------|-------------|
| **Scheduled** | Retrain monthly/quarterly regardless | Stable environments |
| **Trigger-based** | Retrain when drift metric exceeds threshold | Dynamic environments |
| **Continuous** | Ongoing training on new data | Highest accuracy, highest cost |
| **Incremental** | Fine-tune on new data only | Balance freshness and stability |

---

## Key Takeaways

!!! success "Summary"
    - Model drift is **inevitable** in eKYC — new phones, new attacks, new demographics
    - **Score distribution monitoring** is the fastest drift indicator (no labels needed)
    - **Trigger-based retraining** balances freshness with cost
    - Always validate retrained model on **held-out test sets** before deployment

---

## Related Articles

- [MLOps for eKYC](mlops-ekyc.md)
- [eKYC Monitoring & Observability](../05-onboarding-workflow/ekyc-monitoring-observability.md)
