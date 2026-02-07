# ISO 30107 — PAD Testing Standard

## Definition

**ISO/IEC 30107** is the international standard for biometric **Presentation Attack Detection (PAD)**. It defines terminology, attack classification, and testing methodology. Part 3 (ISO 30107-3) specifies how to evaluate PAD mechanisms — the basis for iBeta certification.

---

## Standard Parts

| Part | Title | Content |
|------|-------|---------|
| **30107-1** | Framework | Definitions, attack taxonomy, general principles |
| **30107-2** | Data formats | How to exchange PAD-related data |
| **30107-3** | Testing and reporting | **How to test PAD systems** — methodology, metrics, reporting |
| **30107-4** | Profile for mobile devices | PAD testing specific to mobile biometrics |

---

## ISO 30107-3 Testing Methodology

| Element | Details |
|---------|---------|
| **PAI species** | Each attack type (e.g., "A4 color print", "tablet replay") tested separately |
| **APCER** | Calculated per PAI species — % of attacks that bypass PAD |
| **BPCER** | Overall — % of real users rejected by PAD |
| **Minimum subjects** | 50+ bona fide subjects recommended |
| **Minimum attacks** | Sufficient per PAI species for statistical significance |
| **Reporting** | Must report APCER per PAI species, overall BPCER, testing conditions |

---

## Key Takeaways

!!! success "Summary"
    - ISO 30107 is the **international standard** for PAD testing — basis for iBeta and BixeLab certifications
    - Part 3 defines the **testing methodology** — PAI species, APCER/BPCER metrics, reporting requirements
    - APCER must be reported **per attack type** — the worst-case species determines overall security level
    - Compliance with ISO 30107 is increasingly required by enterprise buyers and regulators

---

## Related Articles

- [iBeta Certification](ibeta-certification.md)
- [Biometric Performance Metrics](biometric-performance-metrics.md)
- [Presentation Attack Types](presentation-attack-types.md)
