# Knowledge Distillation

## Definition

**Knowledge distillation** trains a small (student) model to mimic a large (teacher) model — compressing eKYC models for mobile/edge deployment while retaining most of the teacher's accuracy.

---

## Distillation Pipeline

```mermaid
graph LR
    A[Large Teacher Model<br/>ResNet-100, 65M params] --> B[Soft Labels<br/>Teacher's output distributions]
    B --> C[Train Student Model<br/>MobileNet, 5M params]
    D[Hard Labels<br/>Ground truth] --> C
    C --> E[Compact Student<br/>Near-teacher accuracy at 1/10 the size]

    style E fill:#2E7D32,color:#fff
```

## Distillation for eKYC

| Teacher | Student | Task | Accuracy Retention |
|---------|---------|------|-------------------|
| **IResNet-100 (65M)** | MobileFaceNet (1M) | Face recognition | 97-99% of teacher |
| **ResNet-50 (25M)** | CDCN-Lite (1M) | Face liveness | 95-98% of teacher |
| **EfficientNet-B4 (20M)** | MobileNetV3 (5M) | Document classification | 97-99% of teacher |

---

## Key Takeaways

!!! success "Summary"
    - Distillation enables **mobile-deployable models** with near-server-class accuracy
    - Typical compression: **10-60x** fewer parameters with **95-99%** accuracy retention
    - **Soft label** learning (teacher's probability distribution) provides richer training signal than hard labels alone
    - Essential for on-device eKYC SDK models

---

## Related Articles

- [On-Device Biometric Processing](../02-biometrics-face/on-device-biometric-processing.md)
- [Model Optimization & Quantization](model-optimization-quantization.md)
- [Edge AI Deployment](edge-ai-deployment.md)
