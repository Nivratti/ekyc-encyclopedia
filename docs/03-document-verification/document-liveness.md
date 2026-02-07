# Document Liveness

## Definition

**Document liveness** detects whether a presented document is a **physical original** or a reproduction — such as a screen display, photocopy, or printed photo of a document. It is the document equivalent of face liveness detection.

---

## What Document Liveness Detects

| Attack | Method | Detection Cue |
|--------|--------|--------------|
| **Screen display** | Photo of document shown on phone/tablet screen | Moiré patterns, screen pixel grid, screen bezel, refresh artifacts |
| **Photocopy** | Black-and-white or color photocopy of document | Halftone dots, reduced contrast, paper texture change |
| **Printed photo** | High-quality print of document image | Print dot pattern, color gamut shift, paper texture |
| **Screenshot** | Document image displayed on screen, then screen captured | Screen artifacts, resolution mismatch |

---

## Detection Methods

| Method | What It Analyzes |
|--------|-----------------|
| **Moiré pattern detection** | Interference patterns from screen pixel grid captured by camera |
| **Halftone detection** | Regular dot patterns from photocopier/printer |
| **Texture analysis** | Original document texture vs paper/screen surface |
| **Color analysis** | Color gamut differences between original and reproduction |
| **Frequency analysis** | Specific frequency signatures of screens and printers |
| **Reflection analysis** | Screen glare and reflection patterns |
| **Edge analysis** | Screen bezel or paper edge detection around document |
| **Deep CNN** | Learned features combining all above cues |

---

## Key Takeaways

!!! success "Summary"
    - Document liveness prevents **document replay attacks** — showing photos of documents on screens
    - **Moiré pattern detection** is the strongest single cue for screen display detection
    - **Halftone analysis** catches photocopies
    - Deep CNN models combining multiple cues achieve best results
    - Often combined with **document forensics** in a single pipeline

---

## Related Articles

- [Document Forensics Overview](document-forensics-overview.md)
- [Face Liveness Detection Overview](../02-biometrics-face/face-liveness-detection-overview.md)
