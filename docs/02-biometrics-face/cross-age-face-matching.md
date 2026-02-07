# Cross-Age Face Matching

## Definition

**Cross-age face matching** addresses the challenge of matching a live selfie against an ID photo that may be **5-15 years old**. Facial appearance changes significantly over time due to aging, weight changes, and lifestyle — making this one of the hardest practical problems in eKYC face recognition.

---

## Impact on Match Scores

| Age Gap | Typical Score Drop | Match Rate Impact |
|---------|-------------------|-------------------|
| 0-2 years | < 2% | Negligible |
| 2-5 years | 2-5% | Minor |
| 5-10 years | 5-15% | Significant — may fall below threshold |
| 10-15 years | 15-30% | Major — high false rejection risk |
| 15+ years | 30%+ | Often fails standard thresholds |

---

## Facial Changes with Age

| Change | Impact on Recognition |
|--------|---------------------|
| **Facial fat redistribution** | Changes face shape, jawline, cheek fullness |
| **Wrinkles and skin texture** | Alters texture features models rely on |
| **Hair changes** | Loss, graying, style changes (less impact on cropped face) |
| **Weight gain/loss** | Changes face shape significantly |
| **Facial hair** | Beard/mustache alters lower face features |
| **Glasses** | Partially occlude eye region (critical for recognition) |
| **Surgical changes** | Cosmetic surgery can dramatically alter features |

---

## Cross-Age Datasets

| Dataset | Pairs | Age Range | Key Feature |
|---------|-------|-----------|-------------|
| **MORPH-II** | 55K images, 13K subjects | 16-77 | Largest cross-age dataset |
| **CACD** | 163K images, 2K celebrities | Multi-decade | Celebrity cross-age |
| **FG-NET** | 1,002 images, 82 subjects | 0-69 | Small but wide age range |
| **AgeDB-30** | 16K images, 568 subjects | 30-year gaps | Standard benchmark |
| **CALFW** | 12K pairs | Cross-age LFW | Cross-age evaluation protocol |

---

## Strategies for Cross-Age Robustness

| Strategy | How It Works |
|----------|-------------|
| **Age-invariant training** | Include cross-age pairs in training data |
| **Age augmentation** | Synthetically age/de-age training faces using GANs |
| **Lower threshold for old documents** | Accept lower similarity for documents > 5 years old |
| **Compensating liveness weight** | If face match is lower, require stronger liveness proof |
| **Document renewal encouragement** | Prompt users to use most recent ID |
| **Manual review fallback** | Route low-confidence cross-age matches to human review |

---

## Key Takeaways

!!! success "Summary"
    - Cross-age matching is a **major practical challenge** — ID photos can be 5-15+ years old
    - Match scores drop **5-30%** over a decade, often causing false rejections
    - **AdaFace** and **AgeDB-30** training help, but no model fully solves this
    - Practical mitigations: adaptive thresholds, compensating liveness weight, manual review path

---

## Related Articles

- **Previous**: [← Face Matching & Thresholds](face-matching-thresholds.md)
- **Next**: [Cross-Quality Face Matching →](cross-quality-face-matching.md)
- [Face Recognition Architectures](face-recognition-architectures.md)
