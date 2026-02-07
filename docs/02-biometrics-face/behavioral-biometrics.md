# Behavioral Biometrics

## Definition

**Behavioral biometrics** identifies individuals based on patterns in their behavior — how they type, swipe, hold their phone, and interact with devices. Unlike physiological biometrics (face, fingerprint), behavioral biometrics provides **continuous, passive authentication** without requiring explicit user action.

---

## Behavioral Signals

| Signal | What's Analyzed | eKYC Application |
|--------|----------------|-----------------|
| **Keystroke dynamics** | Typing speed, pressure, rhythm, flight time | Continuous authentication during form filling |
| **Touch/swipe patterns** | Pressure, speed, angle, gesture shape | Passive identity during app interaction |
| **Device motion** | Accelerometer/gyroscope patterns during hold | Distinguish human from bot/emulator |
| **Mouse dynamics** | Movement speed, click patterns, trajectory | Web-based verification |
| **Navigation patterns** | How user moves through app screens | Fraud detection during onboarding |

---

## Role in eKYC

Behavioral biometrics complements face verification as an **additional signal**:

- During onboarding: detect bots, emulators, automated attacks
- Post-onboarding: continuous authentication without explicit re-verification
- Risk scoring: behavioral anomalies trigger step-up verification

---

## Key Takeaways

!!! success "Summary"
    - Behavioral biometrics provides **passive, continuous** identity assurance
    - Complements face biometrics — adds a layer that deepfakes and injection attacks cannot easily replicate
    - Most useful for **ongoing authentication** rather than initial onboarding
    - Key providers: BioCatch, BehavioSec (LexisNexis), Callsign

---

## Related Articles

- [Face Liveness Detection Overview](face-liveness-detection-overview.md)
- [On-Device Biometric Processing](on-device-biometric-processing.md)
