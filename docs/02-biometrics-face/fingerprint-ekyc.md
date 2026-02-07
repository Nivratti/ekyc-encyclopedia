# Fingerprint in eKYC

## Definition

**Fingerprint biometrics** in eKYC uses fingerprint capture and matching for identity verification, primarily in systems like India's Aadhaar where fingerprint data is available for authentication.

---

## Fingerprint in Different eKYC Contexts

| Context | How Fingerprint Is Used |
|---------|----------------------|
| **Aadhaar biometric eKYC** | Customer places finger on certified scanner, matched against UIDAI database |
| **Phone fingerprint sensor** | On-device authentication (not identity verification against database) |
| **Border control** | Live fingerprint matched against passport chip or database |
| **Law enforcement** | AFIS (Automated Fingerprint Identification System) |

## Aadhaar Fingerprint eKYC

| Aspect | Details |
|--------|---------|
| **Capture device** | Certified fingerprint scanner (STQC approved) |
| **Template format** | Minutiae-based (ISO 19794-2) |
| **Matching** | Against UIDAI central database |
| **Accuracy** | ~95% first-attempt success (lower for manual laborers with worn fingerprints) |
| **Challenge** | Worn/dry fingerprints in elderly and manual workers |

---

## Key Takeaways

!!! success "Summary"
    - Fingerprint is primarily relevant in **Aadhaar-based eKYC** (India) and border control
    - **Worn fingerprints** in elderly and manual laborers reduce accuracy (~5-10% failure rate)
    - Phone fingerprint sensors are for **device authentication**, not identity verification against databases
    - Face is **replacing fingerprint** as the primary biometric for eKYC due to contactless capture

---

## Related Articles

- [Face Liveness Detection Overview](face-liveness-detection-overview.md)
- [Iris Recognition](iris-recognition.md)
