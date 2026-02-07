# CNNs for eKYC

## Definition

**Convolutional Neural Networks (CNNs)** are the backbone architecture for most eKYC vision tasks — face detection, recognition, liveness, document classification, and OCR.

---

## Key CNN Families Used in eKYC

| Family | Models | Params | Use in eKYC |
|--------|--------|--------|-------------|
| **ResNet** | ResNet-18/34/50/100 | 11-65M | Face recognition backbone (IResNet), liveness |
| **EfficientNet** | B0-B7 | 5-66M | Document classification, liveness (good accuracy/size ratio) |
| **MobileNet** | V2, V3-S, V3-L | 2-5M | Mobile face detection, on-device liveness |
| **MobileOne** | S0-S4 | 2-15M | Ultra-fast mobile inference |
| **GhostNet** | 1.0x, 1.3x | 5-7M | Efficient mobile backbone |
| **ConvNeXt** | Tiny/Small/Base | 28-89M | Modern CNN competitive with ViT |

## Why CNNs Still Dominate eKYC

| Reason | Details |
|--------|---------|
| **Speed** | 2-5x faster than equivalent ViT on mobile |
| **Proven** | Years of production deployment, well-understood |
| **Mobile-friendly** | Efficient convolution ops on mobile hardware |
| **Training data efficient** | CNNs need less data than ViT to train well |
| **Tooling** | TensorRT, ONNX, CoreML all optimized for CNN ops |

---

## Key Takeaways

!!! success "Summary"
    - **ResNet** (server) and **MobileNet** (mobile) remain the workhorse architectures for eKYC
    - **EfficientNet** provides the best accuracy-per-FLOP for many tasks
    - CNNs are **faster and more mobile-friendly** than ViTs — still dominant in production
    - **ConvNeXt** proves modern CNNs can match ViT accuracy with CNN efficiency

---

## Related Articles

- [Vision Transformers for eKYC](vision-transformers-ekyc.md)
- [Knowledge Distillation](knowledge-distillation.md)
- [Model Optimization & Quantization](model-optimization-quantization.md)
