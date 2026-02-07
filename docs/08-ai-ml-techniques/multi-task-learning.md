# Multi-Task Learning

## Definition

**Multi-task learning (MTL)** trains a single model on multiple related tasks simultaneously — sharing representations across tasks for better generalization and efficiency.

---

## MTL in eKYC

```mermaid
graph TD
    A[Shared Backbone<br/>ResNet-18 / ViT-S] --> B[Liveness Head<br/>Real vs Spoof]
    A --> C[Depth Head<br/>Face depth map]
    A --> D[Domain Head<br/>Which dataset/domain]
    A --> E[Quality Head<br/>Face quality score]

    style A fill:#4051B5,color:#fff
```

| Task Combination | Benefit |
|-----------------|---------|
| **Liveness + depth estimation** | Depth provides geometric reasoning about 3D vs 2D |
| **Liveness + domain classification** | Adversarial domain head forces domain-invariant features |
| **Recognition + quality estimation** | Quality awareness improves matching on low-quality inputs |
| **OCR detection + recognition** | Shared features improve both stages |
| **Document classification + field extraction** | Document type informs field locations |

---

## Key Takeaways

!!! success "Summary"
    - MTL improves liveness accuracy by **2-5%** over single-task (binary) training
    - **Liveness + depth + domain** is the standard multi-task combination for face anti-spoofing
    - **Shared backbone** reduces total compute — one model serves multiple purposes
    - Task weighting (relative loss importance) requires careful tuning

---

## Related Articles

- [Liveness Model Architectures](../02-biometrics-face/liveness-model-architectures.md)
- [Knowledge Distillation](knowledge-distillation.md)
