# Digital Tampering Detection

## Definition

Specific techniques for detecting digital manipulation of identity document images — photo editing, text replacement, splicing, and AI-generated alterations.

---

## Detection Techniques

| Technique | What It Detects | How It Works |
|-----------|----------------|-------------|
| **Error Level Analysis (ELA)** | Edited regions | Re-compress JPEG, compare error levels — edits show higher residuals |
| **Noise inconsistency** | Spliced regions from different sources | Different camera sensors produce different noise patterns |
| **JPEG ghost detection** | Double compression | Edited and re-saved JPEGs show compression ghosts at certain quality levels |
| **Copy-move forgery** | Cloned regions | SIFT/deep features find duplicate patches within same image |
| **Font anomaly detection** | Text replacement | Classify font at character level — replaced text uses different font |
| **Edge inconsistency** | Splicing boundaries | Analyze edge sharpness and artifacts at region boundaries |
| **Metadata analysis** | Editing software traces | EXIF data reveals if edited with Photoshop, GIMP, etc. |

---

## Deep Learning Approaches

| Model | Approach |
|-------|----------|
| **ManTraNet** | Pixel-level manipulation detection — no prior knowledge of manipulation type needed |
| **MVSS-Net** | Multi-view multi-scale — detects both boundary and noise artifacts |
| **CAT-Net** | Compression artifact tracing — traces JPEG compression history |
| **ObjectFormer** | Transformer for object-level forgery detection |

---

## Key Takeaways

!!! success "Summary"
    - Multiple complementary techniques needed — no single method catches all tampering
    - **ELA + noise analysis** are fast baselines; **deep learning** adds learned pattern detection
    - **Font analysis** is critical for ID documents — most fraud involves text editing
    - **Cross-validation** between OCR text, MRZ, and barcode data catches many edits

---

## Related Articles

- [Document Forensics Overview](document-forensics-overview.md)
- [Synthetic Document Detection](synthetic-document-detection.md)
