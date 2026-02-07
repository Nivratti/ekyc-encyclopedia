# Face Anti-Spoofing Feature Extraction

## Definition

This article covers the specific features and cues that liveness detection models use to distinguish real faces from spoofs — texture, frequency, depth, reflection, and temporal features.

---

## Feature Categories

| Feature Type | What It Captures | Detection Target |
|-------------|-----------------|-----------------|
| **Texture** | Surface patterns, print dots, moiré, skin pores | Print, screen replay |
| **Frequency** | Spectral characteristics, high-frequency details | GAN artifacts, print patterns |
| **Depth** | 3D structure of face | 2D attacks (flat) |
| **Reflection** | Specular reflection patterns | Material differences (skin vs paper/screen) |
| **Color** | Color distribution, chrominance | Screen color gamut, paper white point |
| **Temporal** | Motion patterns, flickering, blinking | Video replay, deepfake inconsistency |
| **Contextual** | Background, edges, device frame | Screen bezel, paper edges |

---

## Texture Features

| Technique | How It Works |
|-----------|-------------|
| **LBP (Local Binary Patterns)** | Encode local texture patterns — paper/screen have different micro-texture than skin |
| **Central Difference Convolution** | Capture gradient information that regular convolution misses — key innovation of CDCN |
| **Gabor filters** | Multi-scale, multi-orientation texture analysis |
| **Deep CNN features** | Learned texture representations from convolutional layers |

## Frequency Features

| Technique | How It Works |
|-----------|-------------|
| **FFT/DFT analysis** | Moiré patterns create distinctive frequency peaks |
| **Wavelet decomposition** | Multi-resolution frequency analysis |
| **High-frequency analysis** | Real faces have fine detail; prints/screens lose high-frequency information |

## Depth Features

| Technique | How It Works |
|-----------|-------------|
| **Monocular depth estimation** | Predict depth map from single RGB image — real face is 3D, spoof is flat |
| **Structured light** | Project pattern, measure distortion for depth (iPhone FaceID) |
| **Stereo depth** | Two cameras compute depth via parallax |

---

## Key Takeaways

!!! success "Summary"
    - Multiple feature types work together — no single feature catches all attacks
    - **Texture + depth** is the most effective combination for RGB-only systems
    - **Central Difference Convolution** is the key architectural innovation for fine-grained texture
    - **Frequency analysis** is particularly effective against print attacks (moiré detection)
    - **Temporal features** add significant value when video is available

---

## Related Articles

- [Liveness Model Architectures](liveness-model-architectures.md)
- [Face Liveness Detection Overview](face-liveness-detection-overview.md)
- [Multi-Spectral Liveness](multi-spectral-liveness.md)
