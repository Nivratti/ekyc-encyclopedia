# Voice Biometrics

## Definition

**Voice biometrics** verifies identity based on unique vocal characteristics — pitch, tone, cadence, and vocal tract shape. In eKYC, voice can serve as an additional biometric factor during Video KYC or as a standalone verification method.

---

## Voice in eKYC

| Use Case | How It Works |
|----------|-------------|
| **V-KYC speaker verification** | Verify the person on video call is who they claim (voice + face) |
| **Voice-based authentication** | "My voice is my password" — voiceprint matching |
| **Voice anti-spoofing** | Detect recorded, synthetic, or cloned voice |
| **Accessibility** | Voice-guided eKYC for visually impaired users |

## Voice Anti-Spoofing (ASVspoof)

| Attack | Method |
|--------|--------|
| **Replay** | Play recorded voice of victim |
| **TTS (Text-to-Speech)** | Generate victim's voice synthetically |
| **Voice cloning** | Clone voice using AI (ElevenLabs, VALL-E) |
| **Voice conversion** | Transform attacker's voice to sound like victim |

---

## Key Takeaways

!!! success "Summary"
    - Voice biometrics adds a **second modality** to face-based eKYC
    - **Voice cloning** (AI-generated voice) is a growing threat — parallels deepfake for face
    - Most practical in **Video KYC** where audio is already captured
    - Key providers: Nuance (Microsoft), ID R&D, Pindrop

---

## Related Articles

- [Video KYC](../01-identity-verification/vkyc-video-kyc.md)
- [Face Liveness Detection Overview](face-liveness-detection-overview.md)
