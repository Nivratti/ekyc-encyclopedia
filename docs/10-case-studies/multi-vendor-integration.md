# Multi-Vendor eKYC Integration

## Overview

Integrating multiple eKYC vendors for best-of-breed capabilities, redundancy, and cost optimization — the orchestration approach.

---

## Common Multi-Vendor Patterns

| Pattern | Setup |
|---------|-------|
| **Primary + fallback** | Vendor A for all; Vendor B on failure |
| **Best-of-breed** | Vendor A for liveness, Vendor B for documents, Vendor C for screening |
| **Geographic routing** | Vendor A for India/APAC, Vendor B for EU/US |
| **A/B testing** | Split traffic to evaluate vendor performance |

## Integration Challenges

| Challenge | Solution |
|-----------|---------|
| **Data format differences** | Normalized data model across vendors |
| **Score calibration** | Different vendors return different score scales |
| **Latency variation** | Timeouts and fallback logic |
| **Cost tracking** | Per-vendor, per-verification cost attribution |

---

## Key Takeaways

!!! success "Summary"
    - Multi-vendor provides **redundancy, optimization, and vendor leverage**
    - **Orchestration platforms** (Alloy, Persona) simplify multi-vendor management
    - **Score normalization** is critical — different vendors use different scales
    - **Geographic routing** optimizes for document coverage and latency

---

## Related Articles

- [Vendor Orchestration](../05-onboarding-workflow/vendor-orchestration.md)
- [Document Verification Vendors](../03-document-verification/document-verification-vendors.md)
