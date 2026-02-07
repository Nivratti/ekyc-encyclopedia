# Microservices vs Monolith for eKYC

## Definition

Architectural choice between deploying eKYC as a monolithic application vs decomposed microservices.

---

## Comparison

| Aspect | Monolith | Microservices |
|--------|----------|--------------|
| **Development speed** | Faster initially | Slower initially, faster at scale |
| **Scaling** | Scale everything together | Scale GPU services independently |
| **Deployment** | Single deployment | Independent service deployment |
| **Complexity** | Simple | Distributed systems complexity |
| **Best for** | Startup/MVP, < 10K verifications/day | Scale, > 100K verifications/day |

**Recommendation**: Start monolith, decompose as you scale. Extract GPU-heavy services (face, document) first.

---

## Related Articles

- [eKYC System Architecture](ekyc-system-architecture.md)
