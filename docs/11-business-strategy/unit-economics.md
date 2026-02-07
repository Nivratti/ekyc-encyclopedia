# Unit Economics of eKYC

## Definition

The cost structure and economics of running an eKYC platform — from the vendor/provider perspective.

---

## Cost Structure per Verification

| Cost Component | Typical Range | % of Total |
|---------------|-------------|-----------|
| **GPU compute** (liveness, recognition, OCR) | $0.01-$0.05 | 10-20% |
| **Third-party data** (screening, database checks) | $0.05-$0.30 | 20-40% |
| **Cloud infrastructure** (storage, network, API) | $0.01-$0.03 | 5-10% |
| **Manual review** (8-15% of cases × $2-10 per review) | $0.15-$1.50 | 20-40% |
| **R&D amortized** (model development, document support) | $0.05-$0.20 | 10-20% |
| **Support & operations** | $0.02-$0.10 | 5-10% |
| **Total COGS** | **$0.30-$2.00** | |

## Margin Structure

| Volume Tier | Revenue/Verification | COGS | Gross Margin |
|-------------|---------------------|------|-------------|
| **Low volume** | $3.00-$5.00 | $1.50-$2.00 | 50-60% |
| **Medium volume** | $1.00-$2.00 | $0.50-$1.00 | 50-60% |
| **High volume** | $0.30-$0.80 | $0.20-$0.40 | 40-55% |

---

## Key Takeaways

!!! success "Summary"
    - **Manual review** and **third-party data** are the two largest cost components
    - Reducing manual review rate (higher STP) is the most impactful cost optimization
    - Gross margins are **40-60%** — typical for B2B SaaS
    - At scale, **GPU compute** becomes a small fraction — data and manual review dominate

---

## Related Articles

- [eKYC Pricing Models](ekyc-pricing-models.md)
- [Fraud Economics & ROI](../06-fraud-risk/fraud-economics-roi.md)
