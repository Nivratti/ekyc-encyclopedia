# Vision Transformers for eKYC

## Definition

**Vision Transformers (ViTs)** apply the transformer architecture (self-attention) to image processing — capturing global context that CNNs struggle with, at the cost of higher compute requirements.

---

## Key ViT Models for eKYC

| Model | Params | Key Feature | eKYC Application |
|-------|--------|-------------|-----------------|
| **ViT-Small** | 22M | Standard ViT | Face recognition, liveness |
| **DeiT-Small** | 22M | Distilled, data-efficient | When training data is limited |
| **Swin-T** | 28M | Shifted windows for efficiency | Document understanding |
| **ViT-Base** | 86M | Larger capacity | Server-side processing |
| **DINOv2** | Various | Self-supervised pre-training | General feature backbone |

## ViT vs CNN for eKYC

| Aspect | CNN | ViT |
|--------|-----|-----|
| **Local features** | Strong (convolution is local) | Weaker (global attention) |
| **Global context** | Weak (limited receptive field) | Strong (full image attention) |
| **Mobile speed** | Fast | 2-5x slower |
| **Data efficiency** | Better with small datasets | Needs more data (or pre-training) |
| **Liveness** | CDCN captures fine texture | ViT captures global layout cues |
| **Document understanding** | Limited layout understanding | Excellent (LayoutLMv3 is transformer) |

---

## Key Takeaways

!!! success "Summary"
    - ViTs capture **global context** — valuable for liveness (full-image analysis) and documents (layout understanding)
    - **LayoutLMv3** (transformer) dominates document understanding
    - For face recognition, ViTs **match but don't significantly beat** CNNs — CNNs remain preferred for speed
    - **DINOv2** provides excellent general features for any eKYC task via self-supervised pre-training
    - **Hybrid** (CNN early layers + transformer later layers) may be optimal

---

## Related Articles

- [CNNs for eKYC](cnns-ekyc.md)
- [Foundation Models for eKYC](foundation-models-ekyc.md)
- [Liveness Model Architectures](../02-biometrics-face/liveness-model-architectures.md)
