# Foundation Models for eKYC

## Definition

**Foundation models** are large-scale pre-trained models (CLIP, DINOv2, SAM, GPT-4V) that provide general-purpose representations applicable across eKYC tasks — sometimes with zero or few-shot capability.

---

## Relevant Foundation Models

| Model | Type | eKYC Application |
|-------|------|-----------------|
| **CLIP** | Vision-language | Zero-shot document classification, text-image matching |
| **DINOv2** | Self-supervised vision | General feature backbone for liveness, recognition, forensics |
| **SAM** | Segmentation | Document segmentation, face segmentation |
| **GPT-4V / Claude Vision** | Multimodal LLM | Document understanding, quality assessment, anomaly description |
| **FLIP-MCL** | Face anti-spoofing specific | Domain-generalized liveness using CLIP features |

## Foundation Model Approaches

| Approach | How It Works |
|----------|-------------|
| **Feature extraction** | Use frozen foundation model as feature backbone + train task-specific head |
| **Fine-tuning** | Adapt foundation model to eKYC task with LoRA/adapter layers |
| **Zero-shot** | Use foundation model directly without task-specific training |
| **Prompt engineering** | For LLMs: describe the task in natural language |

---

## Key Takeaways

!!! success "Summary"
    - Foundation models are **changing eKYC ML** — pre-trained representations reduce task-specific data needs
    - **DINOv2 features + task-specific head** is a strong baseline for any eKYC vision task
    - **CLIP-based liveness (FLIP-MCL)** achieves state-of-the-art cross-dataset generalization
    - **Multimodal LLMs** can understand documents holistically — emerging application for complex document analysis
    - Foundation models are too large for mobile — use for **server-side** processing or **distill to mobile models**

---

## Related Articles

- [Self-Supervised Learning](self-supervised-learning.md)
- [Domain Generalization](domain-generalization.md)
- [Vision Transformers](vision-transformers-ekyc.md)
