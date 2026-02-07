# Cost Optimization

## Definition

Optimizing the cost per eKYC verification — GPU compute, storage, API calls, and operational overhead.

---

## Cost Breakdown (Typical)

| Component | % of Cost | Optimization |
|-----------|-----------|-------------|
| **GPU compute** | 40-60% | INT8 quantization, spot instances, right-sizing |
| **Third-party APIs** | 15-25% | Screening API, database verification |
| **Storage** | 10-15% | Lifecycle policies, embedding vs raw images |
| **Manual review** | 5-15% | Improve STP rate, AI-assisted review |
| **Infrastructure** | 5-10% | Reserved instances, auto-scaling |

## Cost per Verification Benchmarks

| Scale | Cost/Verification | Notes |
|-------|------------------|-------|
| **1K/day** | $2-5 | Low volume, high fixed costs |
| **10K/day** | $0.50-2 | Moderate economies of scale |
| **100K/day** | $0.10-0.50 | Good GPU utilization |
| **1M/day** | $0.05-0.20 | Maximum economies of scale |

---

## Key Takeaways

!!! success "Summary"
    - **GPU compute** is the largest cost — INT8 quantization + spot instances can reduce by 60-80%
    - **Increasing STP rate** reduces manual review cost — the most expensive per-unit component
    - **Storage lifecycle** (hot → cold → delete) prevents cost from growing linearly with history
    - At scale (1M+/day), cost per verification drops to **$0.05-0.20** — massive economies of scale

---

## Related Articles

- [GPU Infrastructure](gpu-infrastructure.md)
- [Fraud Economics & ROI](../06-fraud-risk/fraud-economics-roi.md)
