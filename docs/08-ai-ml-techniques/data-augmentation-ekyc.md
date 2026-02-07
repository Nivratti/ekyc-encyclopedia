# Data Augmentation for eKYC

## Definition

Data augmentation creates training variations from existing data — expanding dataset diversity without collecting new samples. Critical for eKYC where real attack data is scarce.

---

## Augmentation Strategies

| Strategy | Techniques | Best For |
|----------|-----------|----------|
| **Geometric** | Rotation, flip, crop, scale, affine | General robustness |
| **Photometric** | Brightness, contrast, saturation, hue, noise | Lighting variation |
| **Quality degradation** | Blur, JPEG compression, resolution reduction | Cross-quality robustness |
| **Cutout/Erasing** | Random rectangular mask on image | Occlusion robustness |
| **Style transfer** | Apply different "styles" to images | Domain variation |
| **Adversarial** | Add adversarial perturbations during training | Adversarial robustness |
| **Mixup/CutMix** | Blend/overlay two training images | Regularization |

## eKYC-Specific Augmentation

| Task | Augmentation | Purpose |
|------|-------------|---------|
| **Liveness** | Simulate print/screen artifacts (moiré, halftone) | Create synthetic spoof examples |
| **Face recognition** | Age progression/regression | Cross-age robustness |
| **Document OCR** | Add shadows, glare, perspective distortion | Capture quality variation |
| **Document forensics** | Synthetic manipulation (splicing, copy-move) | More tampering examples |

---

## Key Takeaways

!!! success "Summary"
    - Augmentation is the **cheapest way** to improve model robustness
    - **Quality degradation** augmentation is critical for cross-quality matching (ID photo vs selfie)
    - **eKYC-specific** augmentations (moiré simulation, synthetic tampering) provide targeted improvements
    - **RandAugment** automates augmentation policy search — reduces manual tuning

---

## Related Articles

- [Synthetic Data Generation](synthetic-data-generation.md)
- [Domain Generalization](domain-generalization.md)
