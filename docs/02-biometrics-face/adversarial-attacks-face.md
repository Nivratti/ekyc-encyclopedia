# Adversarial Attacks on Face Models

## Definition

**Adversarial attacks** add carefully crafted perturbations to input images — imperceptible to humans — that cause deep learning models to make incorrect predictions. In eKYC, these can target face recognition (make attacker match victim) or liveness detection (make spoof classified as live).

---

## Attack Types in eKYC

| Attack | Target | Goal | Method |
|--------|--------|------|--------|
| **Evasion** | Recognition | Make faces unmatchable | Add noise to reduce similarity score |
| **Impersonation** | Recognition | Match attacker to victim | Optimize perturbation to maximize similarity to target |
| **Anti-spoofing bypass** | Liveness | Make spoof classified as live | Adversarial patch/noise on spoof image |
| **Physical adversarial** | Both | Real-world attack | Printed glasses, makeup patterns, patches |

---

## Digital vs Physical Adversarial Attacks

| Aspect | Digital | Physical |
|--------|---------|----------|
| **Threat in eKYC** | Requires injection (digital manipulation) | Works with normal camera capture |
| **Perturbation** | Pixel-level noise | Printed accessories, makeup |
| **Robustness** | Fragile to transformations | Must survive printing, viewing angle, lighting |
| **Examples** | FGSM, PGD, C&W attacks | Adversarial glasses, patches, makeup |

### Notable Physical Adversarial Attacks

| Attack | Method | Target |
|--------|--------|--------|
| **Adversarial glasses** | Specially printed eyeglass frames | Fool face recognition into misidentification |
| **Adversarial patches** | Printed patterns worn on clothing/hat | Evade face detection entirely |
| **Adversarial makeup** | Specific makeup patterns | Alter identity embedding |

---

## Defenses

| Defense | Approach | Effectiveness |
|---------|----------|---------------|
| **Adversarial training** | Include adversarial examples during training | Medium — helps but doesn't solve |
| **Input preprocessing** | JPEG compression, spatial smoothing, bit-depth reduction | Low-Medium — simple but bypassed |
| **Ensemble models** | Multiple models — harder to fool all simultaneously | Medium-High |
| **Certified robustness** | Randomized smoothing provides provable guarantees | High but reduces clean accuracy |
| **Detection networks** | Separate model to detect adversarial inputs | Medium |

---

## Key Takeaways

!!! success "Summary"
    - Adversarial attacks are a **theoretical and practical threat** to face models in eKYC
    - **Digital adversarial attacks** require injection — combining two attack vectors
    - **Physical adversarial attacks** (glasses, patches) work in the real world but are less reliable
    - **No single defense is complete** — defense-in-depth with ensemble + preprocessing + adversarial training
    - In practice, **injection attacks and deepfakes** are currently more common threats than adversarial perturbations

---

## Related Articles

- [Face Recognition Architectures](face-recognition-architectures.md)
- [Injection Attacks](injection-attack.md)
- [Deepfake Detection](deepfake-detection.md)
