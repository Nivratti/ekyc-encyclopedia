# Domain Generalization

## Definition

**Domain Generalization (DG)** trains models to perform well on **unseen target domains** without requiring any data from those domains during training. In eKYC, this means models that work on new phones, new attack types, new lighting conditions, and new demographics they've never seen.

---

## DG Approaches

| Approach | How It Works | Key Methods |
|----------|-------------|-------------|
| **Domain alignment** | Make feature distributions similar across source domains | DANN, CORAL, MMD |
| **Domain-adversarial** | Train domain discriminator to make features domain-invariant | SSDG, MADDG |
| **Meta-learning** | Simulate domain shift during training (MAML-style) | MAML for FAS |
| **Data augmentation** | Create domain variations through augmentation | RandAugment, style transfer, adversarial augmentation |
| **Self-supervised pre-training** | Learn domain-agnostic representations without labels | MAE, contrastive + fine-tune |
| **Ensemble** | Multiple models trained on different domains | Majority voting, model averaging |

## Why DG Matters for eKYC

| Component | Domain Shift Problem |
|-----------|---------------------|
| **Face liveness** | New phone cameras, new attack instruments, new lighting |
| **Face recognition** | New demographics, cross-quality (ID vs selfie) |
| **Document OCR** | New document designs, new fonts, damaged documents |
| **Document forensics** | New editing tools, new manipulation techniques |

---

## Key Takeaways

!!! success "Summary"
    - DG is the **central research challenge** for production eKYC — lab performance ≠ field performance
    - **Self-supervised pre-training + fine-tuning** is currently the best approach
    - **Diverse training data** remains the most impactful practical strategy
    - DG must be evaluated with **cross-dataset protocols** — intra-dataset results are misleading

---

## Related Articles

- [Domain Generalization for Liveness](../02-biometrics-face/domain-generalization-liveness.md)
- [Self-Supervised Learning](self-supervised-learning.md)
- [Data Augmentation](data-augmentation-ekyc.md)
