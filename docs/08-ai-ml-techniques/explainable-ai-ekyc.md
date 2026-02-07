# Explainable AI for eKYC

## Definition

**Explainable AI (XAI)** makes eKYC model decisions interpretable — showing WHY a face was flagged as spoof, WHY a document was rejected, or WHY a face match failed. Required by GDPR Article 22 and EU AI Act.

---

## XAI Techniques for eKYC

| Technique | What It Shows | Application |
|-----------|-------------|-------------|
| **GradCAM** | Heatmap of important image regions | "Model focused on forehead area for liveness decision" |
| **SHAP** | Feature importance for each prediction | "Face match score was low primarily due to age difference" |
| **Attention visualization** | Where ViT model attends | "Document model focused on tampered region" |
| **Counterfactual** | What would change the decision | "If face were 5% better lit, match would pass" |
| **Concept activation** | Which learned concepts drive decision | "Model detected 'screen moiré' pattern" |
| **Prototype explanation** | Show similar training examples | "This face is similar to known spoof cases" |

## Explainability Requirements

| Regulation | Requirement |
|-----------|------------|
| **GDPR Art. 22** | Right to explanation of automated decisions with legal effects |
| **EU AI Act** | Transparency and documentation for high-risk AI systems |
| **FCRA (USA)** | Adverse action notice with specific reasons for rejection |
| **FCA (UK)** | Firms must be able to explain automated decisions |

---

## Key Takeaways

!!! success "Summary"
    - XAI is **legally required** (GDPR, EU AI Act) — not optional for eKYC
    - **GradCAM** is the most practical technique — visual explanation of model focus
    - **SHAP** provides feature-level importance — useful for risk scoring explanations
    - Explanations must be **user-understandable** — "Face too dark" not "Embedding distance 0.43"
    - Build explainability into the pipeline from the start — retrofitting is harder

---

## Related Articles

- [Algorithmic Accountability](../07-regulations-standards/algorithmic-accountability.md)
- [EU AI Act & Biometrics](../07-regulations-standards/eu-ai-act-biometrics.md)
- [Decision Engine Architecture](../05-onboarding-workflow/decision-engine-architecture.md)
