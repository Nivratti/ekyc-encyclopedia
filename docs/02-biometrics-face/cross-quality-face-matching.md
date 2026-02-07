# Cross-Quality Face Matching

## Definition

**Cross-quality face matching** addresses the challenge of comparing a **high-resolution selfie** with a **low-quality ID photo**. ID document photos are often small (100-200px), printed, faded, and captured years ago — creating a significant quality gap with the live selfie.

---

## The Quality Gap

| Attribute | ID Document Photo | Live Selfie |
|-----------|------------------|-------------|
| **Resolution** | 100-200px face | 300-800px face |
| **Source** | Printed on card, scanned | Direct camera capture |
| **Artifacts** | Print dots, moiré, hologram reflections | Camera noise, compression |
| **Color** | Faded, color-shifted | True color |
| **Lighting** | Studio flash (original), ambient (scan) | Variable ambient |
| **Compression** | Multiple generations of compression | Single JPEG |

---

## AdaFace — Quality-Adaptive Recognition

| Aspect | Details |
|--------|---------|
| **Key insight** | Image quality affects embedding reliability — hard samples from low quality should have less gradient impact |
| **Quality proxy** | Feature norm (‖f‖) correlates with image quality |
| **Adaptive margin** | High-quality images get harder margin (more discriminative), low-quality get softer margin (more forgiving) |
| **Result** | Significantly better cross-quality matching than ArcFace |

### AdaFace vs ArcFace on Quality-Degraded Benchmarks

| Benchmark | ArcFace-R100 | AdaFace-R100 | Improvement |
|-----------|-------------|-------------|-------------|
| **IJB-C (TAR@FAR=1e-4)** | 96.02% | 97.39% | +1.37% |
| **IJB-S (Surveillance)** | 58.29% | 63.41% | +5.12% |
| **TinyFace** | 63.89% | 72.02% | +8.13% |

The improvement is most dramatic on **low-quality benchmarks** (TinyFace, IJB-S).

---

## Other Quality-Aware Approaches

| Method | Approach |
|--------|----------|
| **SER-FIQ** | Estimate quality from embedding robustness (self-supervised) |
| **MagFace** | Embedding magnitude indicates quality — penalize low-quality equally |
| **FaceQnet** | Dedicated quality estimation network trained on verification performance |
| **Super-resolution** | Enhance ID photo resolution before embedding (GFPGAN, CodeFormer) |

---

## Key Takeaways

!!! success "Summary"
    - Cross-quality matching is a **core eKYC challenge** — ID photos are 3-10x lower quality than selfies
    - **AdaFace** specifically solves this with quality-adaptive margin — best choice for eKYC
    - **Super-resolution** (GFPGAN) can enhance ID photos but adds computation and may introduce artifacts
    - Quality-aware threshold adjustment provides additional robustness

---

## Related Articles

- **Previous**: [← Cross-Age Face Matching](cross-age-face-matching.md)
- **Next**: [Presentation Attack Types →](presentation-attack-types.md)
- [Face Quality Assessment](face-quality-assessment.md)
- [Face Recognition Architectures](face-recognition-architectures.md)
