# Face Biometrics in eKYC

## Definition

**Face biometrics** in eKYC encompasses the complete pipeline of capturing a user's face, verifying they are a live person (liveness detection), and matching their face against their identity document photo — the core technology enabling remote identity verification.

---

## The Face Verification Pipeline

```mermaid
graph LR
    A[Selfie Capture] --> B[Face Detection<br/>Locate face in image]
    B --> C[Quality Check<br/>Blur, lighting, pose]
    C --> D[Liveness Detection<br/>Real person vs spoof]
    D --> E[Face Embedding<br/>Extract 512-d vector]
    E --> F[Face Matching<br/>Compare with ID photo]
    F --> G{Match?}
    G -->|Score > threshold| H[✅ Verified]
    G -->|Score < threshold| I[❌ Rejected]
```

## Key Components

| Component | Purpose | Key Challenge |
|-----------|---------|-------------|
| **Face detection** | Find face in image | Multiple faces, small faces, occlusion |
| **Face quality** | Ensure image is usable | Low light, blur, extreme angles |
| **Face liveness** | Prove it's a live person | Deepfakes, printed photos, 3D masks |
| **Face recognition** | Match selfie to ID photo | Cross-quality (selfie vs printed ID photo), cross-age |
| **Face deduplication** | Check against existing database (1:N) | Scale (millions of comparisons), speed |

---

## Key Takeaways

!!! success "Summary"
    - Face verification is a **5-step pipeline**: detect → quality → liveness → embed → match
    - **Liveness detection** is the most critical security component — prevents spoofing
    - **Cross-quality matching** (selfie vs printed ID photo) is the key accuracy challenge
    - The entire pipeline must run in **< 3 seconds** for good user experience

---

## Related Articles

- [Biometrics Overview](biometrics-overview.md)
- [Face Detection Overview](face-detection.md)
- [Face Liveness Detection](face-liveness-detection-overview.md)
- [Face Recognition Overview](face-recognition-overview.md)
