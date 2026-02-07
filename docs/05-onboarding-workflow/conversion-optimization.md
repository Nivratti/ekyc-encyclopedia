# Conversion Optimization

## Definition

**Conversion optimization** in eKYC focuses on maximizing the percentage of users who start the verification process and successfully complete it — balancing security requirements with user experience.

---

## Key Metrics

| Metric | Definition | Good Target |
|--------|-----------|-------------|
| **Completion rate** | % who finish the full flow | > 85% |
| **First-attempt success** | % passing on first try | > 75% |
| **STP rate** | Straight-Through Processing (auto-approved) | > 80% |
| **Average time to complete** | Time from start to submission | < 60 seconds |
| **Drop-off per step** | % abandoning at each step | < 10% per step |
| **Retry rate** | % needing to retry a step | < 20% |

---

## Drop-Off Analysis

| Drop-Off Point | Common Cause | Fix |
|---------------|-------------|-----|
| **Permission request** | Camera permission denied/scary | Clear pre-permission explanation |
| **Document capture** | Can't get quality capture | Better guidance, lower quality threshold |
| **Selfie capture** | Liveness fails, confusing instructions | Passive liveness, simpler UI |
| **Processing wait** | Too slow, user navigates away | Show progress, async with notification |
| **Rejection** | Too strict thresholds | Tune thresholds, add retry path |

---

## Optimization Levers

| Lever | Impact | Risk |
|-------|--------|------|
| **Lower quality thresholds** | More users pass capture | Worse downstream accuracy |
| **Fewer verification steps** | Faster completion | Lower security assurance |
| **Lower match thresholds** | Fewer false rejections | More false acceptances |
| **Passive over active liveness** | Less drop-off | Slightly lower spoof detection |
| **Auto-retry with guidance** | Recover failed attempts | Longer total time |
| **Progressive disclosure** | Simpler initial flow | May need follow-up for EDD |

---

## Key Takeaways

!!! success "Summary"
    - **Completion rate** is the single most important business metric for eKYC
    - Every step in the flow loses 5-15% of users — **minimize steps**
    - **Threshold tuning** is the most powerful lever — balance FAR/FRR against conversion
    - **A/B test everything** — small UX changes can have large conversion impacts
    - Conversion optimization must be balanced with security — regulators audit acceptance quality

---

## Related Articles

- [eKYC UX Best Practices](ekyc-ux-best-practices.md)
- [A/B Testing for eKYC](ab-testing-ekyc.md)
- [Face Matching & Thresholds](../02-biometrics-face/face-matching-thresholds.md)
