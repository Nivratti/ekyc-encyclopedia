# Active vs Passive Liveness

## Definition

**Active liveness** requires the user to perform specific actions (blink, turn head, smile) during verification. **Passive liveness** analyzes a single image or short clip without any user interaction. The industry is trending toward passive liveness for better user experience.

---

## Comparison

| Aspect | Passive Liveness | Active Liveness |
|--------|-----------------|-----------------|
| **User action** | None — just look at camera | Follow instructions (2-4 challenges) |
| **Duration** | < 1 second analysis | 3-10 seconds |
| **UX score** | ⭐⭐⭐⭐⭐ | ⭐⭐⭐ |
| **Drop-off rate** | ~5% | ~15-25% |
| **Print attack detection** | Strong | Strong |
| **Screen replay detection** | Good-Strong | Strong |
| **3D mask detection** | Moderate | Moderate-Good |
| **Deepfake detection** | Moderate | Better (dynamic expressions harder to fake) |
| **Injection attack detection** | Weak (both) | Weak (both) |
| **Accessibility** | Better (no action needed) | Problematic for motor/cognitive disabilities |
| **iBeta certifiable** | Yes (Level 1 & 2) | Yes (Level 1 & 2) |

---

## Active Liveness Challenges

| Challenge | What It Tests | Deepfake Vulnerability |
|-----------|-------------|----------------------|
| **Blink** | Eye movement control | Easy to fake with deepfake |
| **Head turn (left/right)** | 3D head structure | Medium — real-time deepfake can respond |
| **Smile** | Expression control | Medium — deepfake can generate smiles |
| **Random gaze** | Eye tracking | Harder to fake accurately |
| **Color response** | Screen flashes colors, analyze face reflection | Hard to fake (iProov's Flashmark approach) |

---

## Industry Trend: Passive-First

Most major providers now offer passive-first with active as optional upgrade:

| Provider | Default | Active Available |
|----------|---------|-----------------|
| **iProov** | Passive (Liveness Assurance) | Yes (Genuine Presence with Flashmark) |
| **Onfido** | Passive (Motion capture) | — |
| **Jumio** | Passive + Active | Yes |
| **HyperVerge** | Passive-first | Yes |
| **FacePhi** | Passive | Yes |

---

## Key Takeaways

!!! success "Summary"
    - **Passive liveness is the industry direction** — better UX, lower drop-off, sufficient security for most use cases
    - **Active liveness** still has value for high-security scenarios and as a step-up challenge
    - **Neither approach alone stops injection attacks** — device integrity checks are separate
    - **Deepfakes can respond to active challenges** in real-time — active doesn't guarantee protection
    - Best approach: **passive by default, active as escalation, device integrity always**

---

## Related Articles

- **Previous**: [← Presentation Attack Types](presentation-attack-types.md)
- **Next**: [Liveness Model Architectures →](liveness-model-architectures.md)
- [Face Liveness Detection Overview](face-liveness-detection-overview.md)
- [Deepfake Detection](deepfake-detection.md)
