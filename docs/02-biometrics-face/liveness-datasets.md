# Liveness Datasets

## Definition

This article catalogues the major datasets used for training and evaluating face liveness / presentation attack detection models. Dataset diversity and quality directly determine how well a liveness model generalizes to real-world attacks.

---

## Major Datasets

| Dataset | Year | Subjects | Videos/Images | Attack Types | Capture Devices | Key Feature |
|---------|------|----------|--------------|-------------|-----------------|-------------|
| **OULU-NPU** | 2017 | 55 | 5,940 videos | Print, replay | 6 phones | 4 protocols (cross-device, cross-attack) |
| **CASIA-FASD** | 2012 | 50 | 600 videos | Print, replay | 3 cameras | Early benchmark, still used |
| **Replay-Attack** | 2012 | 50 | 1,300 clips | Print, replay (phone, tablet) | 1 camera | Classic benchmark |
| **SiW** | 2018 | 165 | 4,620 videos | Print, replay | 1 camera | Large scale, high quality |
| **SiW-M** | 2019 | 493 | 1,630 videos | 13 attack types (masks, makeup, partial) | 1 camera | Most diverse attack types |
| **CelebA-Spoof** | 2020 | 10,177 | 625K images | Print, replay, 3D mask | Multiple | Largest dataset |
| **WMCA** | 2019 | 72 | 1,679 videos | Print, replay, mask (rigid, flex, paper) | Multi-spectral (RGB, depth, NIR, thermal) | Multi-modal |
| **HiFiMask** | 2021 | 75 | 54K videos | High-fidelity 3D masks (resin, plaster, transparent) | 7 cameras | Most realistic mask attacks |
| **CeFA** | 2020 | 1,607 | 30K videos | Print, replay, 3D mask | Multi-spectral | Cross-ethnicity focus |
| **CASIA-SURF** | 2019 | 1,000 | 21K videos | Print, cut-out | Multi-modal (RGB, depth, IR) | Multi-modal |

---

## Cross-Dataset Evaluation Protocols

The standard way to evaluate liveness model generalization:

### Leave-One-Out Protocol

Train on 3 datasets, test on the 4th (using OULU-NPU [O], CASIA-FASD [C], Idiap Replay [I], MSU-MFSD [M]):

| Protocol | Train | Test | What It Evaluates |
|----------|-------|------|-------------------|
| **O&C&I → M** | OULU + CASIA + Idiap | MSU | Generalize to unseen capture setup |
| **O&M&I → C** | OULU + MSU + Idiap | CASIA | Generalize to different camera |
| **O&C&M → I** | OULU + CASIA + MSU | Idiap | Generalize to different environment |
| **I&C&M → O** | Idiap + CASIA + MSU | OULU | Generalize to mobile devices |

### Why Cross-Dataset Testing Matters

| Test Type | What It Shows | Typical ACER |
|-----------|--------------|-------------|
| **Intra-dataset** (same dataset train/test) | Model memorization ability | 1-3% |
| **Cross-dataset** (different dataset) | Real generalization ability | 10-30% |
| **Real-world** (production attacks) | Actual deployment performance | Unknown (often worse) |

---

## Dataset Selection for Training

| Goal | Recommended Datasets |
|------|---------------------|
| **Baseline training** | OULU-NPU + CASIA-FASD |
| **Diverse attacks** | Add SiW-M (13 attack types) |
| **3D mask robustness** | Add HiFiMask or WMCA |
| **Scale** | CelebA-Spoof (625K images) |
| **Cross-ethnicity** | CeFA (multi-ethnicity) |
| **Multi-modal** | WMCA or CASIA-SURF (RGB + Depth + NIR) |

---

## Key Takeaways

!!! success "Summary"
    - **OULU-NPU** is the gold standard benchmark with 4 well-defined protocols
    - **Cross-dataset evaluation** reveals true generalization — intra-dataset results are misleading
    - **CelebA-Spoof** (625K images) is the largest, but OULU-NPU protocols remain most cited
    - **HiFiMask** provides the most realistic 3D mask attacks
    - **Dataset diversity** (devices, attack types, ethnicities) is more important than dataset size
    - For production models, train on **as many diverse datasets as possible**

---

## Related Articles

- **Previous**: [← Liveness Model Architectures](liveness-model-architectures.md)
- **Next**: [Domain Generalization for Liveness →](domain-generalization-liveness.md)
- [Face Liveness Detection Overview](face-liveness-detection-overview.md)
- [Presentation Attack Types](presentation-attack-types.md)
