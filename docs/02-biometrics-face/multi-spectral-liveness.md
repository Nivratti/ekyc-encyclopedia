# Multi-Spectral Liveness

## Definition

**Multi-spectral liveness** uses sensors beyond standard RGB cameras — including Near-Infrared (NIR), depth (ToF/structured light), and thermal — to detect presentation attacks based on physical properties invisible to RGB cameras.

---

## Sensor Types

| Sensor | What It Captures | Spoof Detection Advantage |
|--------|-----------------|--------------------------|
| **NIR (Near-Infrared)** | 850-940nm reflected light | Skin has unique NIR reflectance; paper/screen differ dramatically |
| **Structured Light** | 3D depth via projected dot pattern | Detects flatness of 2D attacks, mask edges |
| **Time-of-Flight (ToF)** | Distance measurement per pixel | 3D shape verification |
| **Thermal** | Heat emission (8-14μm) | Real faces emit heat; masks/prints don't |
| **SWIR** | Short-wave infrared (1-2.5μm) | Deep material classification |

---

## Device Availability

| Sensor | Consumer Phones | Dedicated Hardware |
|--------|----------------|-------------------|
| **NIR** | Limited (some phones have IR) | Widely available |
| **Structured light** | iPhone FaceID, some Android | Yes |
| **ToF** | Samsung, some flagships | Yes |
| **Thermal** | FLIR add-ons only | Specialized devices |

---

## Key Takeaways

!!! success "Summary"
    - Multi-spectral approaches are **significantly more robust** than RGB-only, especially against 3D masks
    - **NIR** is the most practical additional sensor — detects material differences RGB cannot
    - **iPhone FaceID** (structured light + NIR) is the gold standard for consumer multi-spectral liveness
    - **Most eKYC operates RGB-only** because users have diverse phone models — multi-spectral is for premium/dedicated devices
    - For RGB-only systems, **strong AI models must compensate** for the lack of additional sensor data

---

## Related Articles

- [3D Mask Attacks](3d-mask-attacks.md)
- [Face Anti-Spoofing Feature Extraction](face-anti-spoofing-features.md)
- [Liveness Datasets](liveness-datasets.md)
