# A/B Testing for eKYC

## Definition

**A/B testing** in eKYC compares two variants of a flow, threshold, or UI element to determine which performs better on key metrics (completion rate, accuracy, user satisfaction).

---

## What to A/B Test

| Element | Variant A | Variant B | Metric |
|---------|-----------|-----------|--------|
| **Liveness type** | Passive only | Passive + active fallback | Completion rate, spoof catch rate |
| **Face match threshold** | 0.60 | 0.65 | FAR, FRR, manual review rate |
| **Document capture UI** | Manual button | Auto-capture | First-attempt success |
| **Error messages** | Generic "Try again" | Specific "Face too dark" | Retry success rate |
| **Flow order** | Document first | Selfie first | Drop-off rate |
| **Quality threshold** | Strict (blur < 50) | Relaxed (blur < 100) | Completion vs OCR accuracy |

## Important Considerations

| Consideration | Details |
|--------------|---------|
| **Statistical significance** | Need sufficient volume per variant (thousands) |
| **Regulatory consistency** | Both variants must meet minimum compliance requirements |
| **Equal distribution** | Random assignment, no selection bias |
| **Monitor for harm** | Stop test if one variant has significantly worse fraud rate |

---

## Key Takeaways

!!! success "Summary"
    - A/B testing is **essential** for optimizing eKYC — small changes have large impact
    - **Threshold A/B tests** directly impact the FAR/FRR/STP balance
    - Both variants must meet **minimum regulatory requirements** — can't A/B test compliance away
    - Need **thousands of sessions** per variant for statistical significance

---

## Related Articles

- [Conversion Optimization](conversion-optimization.md)
- [Face Matching & Thresholds](../02-biometrics-face/face-matching-thresholds.md)
