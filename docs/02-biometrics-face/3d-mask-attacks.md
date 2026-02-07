# 3D Mask Attacks

## Definition

**3D mask attacks** use physical three-dimensional replicas of a victim's face to defeat liveness detection. These are the most sophisticated presentation attacks, ranging from cheap paper-craft to expensive custom silicone.

---

## Mask Types

| Type | Material | Cost | Realism | Detection Difficulty |
|------|----------|------|---------|---------------------|
| **Paper-craft** | Folded/curved paper | $5-20 | Low | Easy-Medium |
| **3D-printed (rigid)** | PLA/resin | $50-200 | Medium | Medium |
| **Resin cast** | Polyurethane resin | $100-500 | Medium-High | Hard |
| **Silicone (custom)** | Medical-grade silicone | $300-3,000 | Very High | Very Hard |
| **Transparent overlay** | Thin silicone over real face | $200-1,000 | High | Very Hard |

---

## Detection Approaches

| Method | What It Detects | Hardware Needed |
|--------|----------------|-----------------|
| **Material analysis** | Skin vs silicone/resin reflectance | RGB camera |
| **Thermal imaging** | Masks don't emit body heat | Thermal camera |
| **NIR sub-surface scattering** | Light passes through skin differently than synthetic materials | NIR sensor |
| **Micro-expression analysis** | Masks limit expression range and speed | RGB camera + temporal analysis |
| **Eye movement tracking** | Rigid masks restrict natural eye movement | High-fps camera |
| **Depth sensing** | Detect mask edges, seams, unnatural depth | Structured light / ToF sensor |

---

## Datasets for 3D Mask Research

| Dataset | Mask Types | Key Feature |
|---------|-----------|-------------|
| **HiFiMask** | Resin, plaster, transparent | Most realistic, 54K videos |
| **WMCA** | Rigid, flexible, paper-craft | Multi-spectral (RGB+Depth+NIR+Thermal) |
| **3DMAD** | Paper-craft 3D masks | Early 3D mask dataset |
| **SiW-M** | Various mask categories | Part of larger multi-attack dataset |

---

## Key Takeaways

!!! success "Summary"
    - 3D masks are **rare but dangerous** — silicone masks can defeat many RGB-only liveness systems
    - **Multi-spectral sensors** (NIR, thermal, depth) significantly improve mask detection
    - **iBeta Level 2** specifically tests against 3D mask attacks
    - **HiFiMask** dataset provides the most realistic mask attack data for research

---

## Related Articles

- [Presentation Attack Types](presentation-attack-types.md)
- [Multi-Spectral Liveness](multi-spectral-liveness.md)
- [iBeta Certification](ibeta-certification.md)
