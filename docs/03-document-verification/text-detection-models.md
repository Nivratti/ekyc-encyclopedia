# Text Detection Models

## Definition

Text detection locates regions of text within a document image, outputting bounding polygons for each text instance. This is Stage 1 of the OCR pipeline.

---

## Key Models

| Model | Year | Architecture | Key Innovation | Speed (GPU) |
|-------|------|-------------|----------------|-------------|
| **CRAFT** | 2019 | VGG-16 + U-Net | Character-level affinity scoring | 30-50ms |
| **EAST** | 2017 | PVANet | Direct geometry regression, very fast | 10-20ms |
| **DBNet** | 2020 | ResNet + FPN | Differentiable binarization — adaptive thresholding | 20-40ms |
| **DBNet++** | 2022 | DBNet + ASF | Adaptive scale fusion for multi-scale text | 25-45ms |
| **PSENet** | 2019 | ResNet + FPN | Progressive scale expansion for touching text | 30-50ms |
| **FAST** | 2021 | Lightweight | Fastest text detector, mobile-friendly | 5-15ms |

---

## For ID Documents Specifically

| Consideration | Details |
|--------------|---------|
| **Fixed layouts** | Most text is in known positions — detection can be template-assisted |
| **Small text** | Microprint, fine text on IDs needs high-resolution input |
| **Multi-orientation** | Some fields are vertical or rotated |
| **MRZ** | Fixed-pitch OCR-B font — specialized detection |
| **Embedded in graphics** | Text over holograms, patterns, watermarks |

---

## Key Takeaways

!!! success "Summary"
    - **DBNet** is the current standard — differentiable binarization handles diverse text well
    - **CRAFT** excels at character-level detection (useful for damaged/irregular text)
    - For ID documents, **template-assisted detection** (knowing where text should be) improves accuracy
    - Speed is typically not the bottleneck — recognition (Stage 2) is slower

---

## Related Articles

- [OCR Pipeline for ID Documents](ocr-pipeline-id-documents.md)
- [Text Recognition Models](text-recognition-models.md)
