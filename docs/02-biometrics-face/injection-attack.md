# Injection Attacks

## Definition

An **injection attack** bypasses the camera entirely by feeding fake images, video, or data directly into the verification pipeline. Unlike presentation attacks (holding a photo to the camera), injection attacks insert pre-recorded, synthetic, or deepfake content at a digital level — making them **invisible to camera-based liveness detection**.

---

## Injection Attack Vectors

```mermaid
graph TD
    A[Injection Attack Vectors] --> B[Virtual Camera<br/>OBS, ManyCam, v4l2loopback]
    A --> C[Emulator<br/>Android emulator + virtual camera]
    A --> D[API Injection<br/>Send fake data directly to API]
    A --> E[App Hooking<br/>Frida, Xposed modify app behavior]
    A --> F[Camera API Hijack<br/>Intercept at OS level]

    B --> G[Feed pre-recorded/deepfake video as camera]
    C --> H[Run app in emulator, inject at camera driver]
    D --> I[Bypass SDK entirely, POST fake images to API]
    E --> J[Hook camera capture function, replace frames]
    F --> K[Root device, replace camera driver output]

    style D fill:#e53935,color:#fff
    style E fill:#e53935,color:#fff
```

---

## Why Injection Attacks Are Dangerous

| Reason | Details |
|--------|---------|
| **Invisible to PAD** | Liveness models analyze what the "camera" sees — if injection replaces camera, PAD sees "real" face |
| **Scalable** | Once pipeline is built, can attack thousands of times |
| **Deepfake-ready** | Real-time deepfake + virtual camera = perfect attack |
| **Growing tools** | Virtual cameras, Frida, Android emulators are freely available |
| **SDK bypass** | API injection skips all client-side security checks |

---

## Defense Layers

```mermaid
graph TD
    A[Defense Against Injection] --> B[Layer 1: Device Integrity]
    A --> C[Layer 2: SDK Protection]
    A --> D[Layer 3: Frame Integrity]
    A --> E[Layer 4: Server Validation]

    B --> B1[Root/jailbreak detection]
    B --> B2[Emulator detection]
    B --> B3[Debug mode detection]

    C --> C1[Virtual camera detection]
    C --> C2[App hooking detection<br/>Frida, Xposed]
    C --> C3[Screen recording detection]
    C --> C4[Code obfuscation + integrity check]

    D --> D1[Camera API attestation]
    D --> D2[Frame metadata validation]
    D --> D3[Random challenge injection]

    E --> E1[Server-side liveness re-check]
    E --> E2[Consistency validation]
    E --> E3[Behavioral analysis]

    style A fill:#4051B5,color:#fff
```

### Platform-Specific Defenses

| Platform | Available Defenses |
|----------|-------------------|
| **Android** | SafetyNet/Play Integrity API, camera2 API validation, root detection |
| **iOS** | App Attest, DeviceCheck, jailbreak detection (limited by Apple restrictions) |
| **Web** | Limited — WebRTC constraints, but fundamentally less secure than native |

---

## Key Takeaways

!!! success "Summary"
    - Injection attacks are the **industry's biggest current security gap** — most eKYC providers underprotect against them
    - Virtual camera + deepfake is the **most dangerous combination** — bypasses both PAD and face matching
    - Defense requires **multiple layers**: device integrity → SDK protection → frame integrity → server validation
    - **API injection** is the hardest to defend against — requires server-side validation of all submissions
    - **Platform attestation** (Play Integrity, App Attest) is becoming essential
    - This is an **active arms race** — defenses must continuously evolve

---

## Related Articles

- **Previous**: [← Deepfake Detection](deepfake-detection.md)
- **Next**: [3D Mask Attacks →](3d-mask-attacks.md)
- [Face Liveness Detection Overview](face-liveness-detection-overview.md)
- [eKYC Challenges & Limitations](../00-foundations/ekyc-challenges-and-limitations.md)
