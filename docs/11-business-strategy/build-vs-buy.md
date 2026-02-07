# Build vs Buy eKYC

## Definition

The strategic decision of whether to build eKYC capabilities in-house or purchase from a vendor — weighing cost, time-to-market, accuracy, control, and ongoing maintenance.

---

## Decision Framework

| Factor | Build In-House | Buy from Vendor |
|--------|---------------|----------------|
| **Time to market** | 6-18 months | 2-8 weeks |
| **Upfront cost** | $500K-$5M+ (team + infra) | $0-50K setup |
| **Ongoing cost** | $200K-$1M/year (team + compute) | $0.50-5 per verification |
| **Accuracy** | Depends on team expertise | Proven, benchmarked |
| **Document coverage** | Build incrementally | 2,500-14,000+ types available |
| **Control** | Full | Limited to vendor capabilities |
| **Regulatory updates** | Your responsibility | Vendor handles |
| **Differentiation** | Potential competitive moat | Same as competitors using same vendor |

## When to Build

| Signal | Why Build |
|--------|----------|
| eKYC is **core to your product** (you ARE an eKYC vendor) | It's your competitive advantage |
| **>10M verifications/month** | Economies of scale favor in-house |
| **Unique requirements** not met by vendors | Specialized documents, workflows |
| **Data sovereignty** | Must not share data with third parties |
| **Deep ML team** available | Can achieve and maintain high accuracy |

## When to Buy

| Signal | Why Buy |
|--------|---------|
| eKYC is **table stakes** (bank, fintech) not core differentiator | Focus on your actual product |
| **<1M verifications/month** | Vendor economics are better |
| Need **fast time to market** | Weeks vs months |
| **Limited ML expertise** | Can't match vendor accuracy |
| **Multi-country** from day one | Need 100+ countries immediately |

---

## Key Takeaways

!!! success "Summary"
    - **Most companies should buy** — eKYC is a means to an end, not the core product
    - **Build only if** eKYC is your core product OR you have massive scale + deep ML team
    - **Hybrid approach**: buy vendor SDK for document + liveness, build custom decision engine + orchestration
    - Total cost of ownership (build) is often **3-5x higher** than expected due to ongoing maintenance

---

## Related Articles

- [Competitive Landscape](competitive-landscape.md)
- [Vendor Orchestration](../05-onboarding-workflow/vendor-orchestration.md)
