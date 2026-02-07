# Multi-Tenant Architecture

## Definition

Serving multiple eKYC clients from shared infrastructure while maintaining data isolation, per-tenant configuration, and independent scaling.

---

## Tenancy Models

| Model | Isolation | Cost | Complexity |
|-------|-----------|------|-----------|
| **Shared everything** | Logical (same DB, API key separation) | Lowest | Lowest |
| **Shared compute, separate storage** | Data isolated, compute shared | Medium | Medium |
| **Dedicated compute** | Separate GPU/processing per tenant | High | High |
| **Fully dedicated** | Separate infrastructure per tenant | Highest | Highest |

## Per-Tenant Configuration

| Configuration | Why Per-Tenant |
|--------------|---------------|
| **Thresholds** | Different risk appetites (bank vs fintech) |
| **Document types** | Different supported countries |
| **Screening lists** | Additional custom watchlists |
| **Decision rules** | Custom approval/reject logic |
| **Branding** | White-label SDK with client branding |
| **Data retention** | Different regulatory requirements |
| **Webhook endpoints** | Different notification targets |

---

## Key Takeaways

!!! success "Summary"
    - **Shared compute + separate storage** is the sweet spot for most SaaS eKYC platforms
    - **Per-tenant configuration** (thresholds, rules, documents) is essential — one size doesn't fit all
    - **Data isolation** is non-negotiable — one tenant must never see another's biometric data
    - **Enterprise clients** often require dedicated compute — premium tier

---

## Related Articles

- [eKYC System Architecture](ekyc-system-architecture.md)
- [Security Architecture](security-architecture.md)
