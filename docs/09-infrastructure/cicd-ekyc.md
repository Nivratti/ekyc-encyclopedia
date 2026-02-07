# CI/CD for eKYC

## Definition

Continuous Integration and Deployment pipelines for eKYC — deploying code changes, model updates, and configuration changes safely.

---

## Deployment Strategies

| Strategy | How It Works | Risk Level |
|----------|-------------|-----------|
| **Blue-green** | Deploy to identical environment, switch traffic | Low |
| **Canary** | Route 5-10% traffic to new version, monitor | Low |
| **Rolling** | Gradually replace instances | Medium |
| **Shadow** | New version processes real traffic but doesn't serve results | Lowest |

## What Gets Deployed

| Component | Frequency | Strategy |
|-----------|-----------|---------|
| **API code** | Weekly-monthly | Blue-green or canary |
| **ML models** | Monthly-quarterly | Shadow → canary → full rollout |
| **SDK** | Monthly | Version-gated, backward compatible |
| **Rules/thresholds** | Weekly | Feature flags, instant rollback |
| **Screening lists** | Daily | Automated, no deployment needed |

---

## Key Takeaways

!!! success "Summary"
    - **ML model deployments** require shadow testing before serving — a bad model update is catastrophic
    - **Canary deployments** for API changes — monitor error rates before full rollout
    - **Feature flags** for threshold/rule changes — enable instant rollback without deployment
    - **Automated rollback** on error rate spike is essential

---

## Related Articles

- [MLOps for eKYC](../08-ai-ml-techniques/mlops-ekyc.md)
- [eKYC Monitoring & Observability](../05-onboarding-workflow/ekyc-monitoring-observability.md)
