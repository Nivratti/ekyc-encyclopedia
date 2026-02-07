# Algorithmic Accountability

## Definition

**Algorithmic accountability** requires that AI-based decisions (like eKYC auto-approve/reject) are explainable, fair, auditable, and subject to human oversight — driven by regulations like the EU AI Act, GDPR Article 22, and emerging global standards.

---

## Key Requirements

| Requirement | What It Means |
|-------------|-------------|
| **Explainability** | Can explain WHY a verification was approved or rejected |
| **Fairness** | Equitable performance across demographic groups |
| **Auditability** | Complete trail of model decisions for regulatory review |
| **Human oversight** | Human can review and override automated decisions |
| **Contestability** | Individuals can challenge decisions that affect them |
| **Documentation** | Model cards, data sheets, performance reports |

## Implementing Explainability in eKYC

| Decision | Explanation Example |
|----------|-------------------|
| **Rejected — liveness fail** | "The system detected the presented face was not a live person" |
| **Rejected — face mismatch** | "The selfie did not sufficiently match the document photo" |
| **Rejected — document forensics** | "The document showed signs of digital alteration" |
| **Manual review — low confidence** | "Multiple checks had borderline scores requiring human review" |
| **Rejected — sanctions** | "The applicant matched a name on a sanctions list" |

---

## Key Takeaways

!!! success "Summary"
    - **GDPR Article 22** gives individuals the right to contest automated decisions
    - **EU AI Act** mandates transparency, bias testing, and human oversight for high-risk AI
    - eKYC systems must provide **specific, understandable reasons** for rejections
    - **Model documentation** (model cards, bias reports) is becoming a regulatory requirement
    - **Demographic fairness testing** is no longer optional — it's legally mandated in the EU

---

## Related Articles

- [EU AI Act & Biometrics](eu-ai-act-biometrics.md)
- [Biometric Fairness & Bias](../02-biometrics-face/biometric-fairness-bias.md)
