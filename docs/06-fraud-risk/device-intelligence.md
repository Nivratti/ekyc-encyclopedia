# Device Intelligence & Fingerprinting

## Definition

**Device intelligence** uses signals from the user's device — hardware attributes, software configuration, and behavioral patterns — to assess fraud risk before, during, and after eKYC verification.

---

## Device Signals

| Signal | What It Reveals | Risk Indicator |
|--------|----------------|---------------|
| **Device fingerprint** | Unique device identifier | Multiple accounts from same device |
| **Root/jailbreak** | Device security compromised | Can inject camera, modify app |
| **Emulator** | Not a real phone | Likely automated attack |
| **Virtual camera** | Fake camera feed | Injection attack |
| **GPS spoofing** | Fake location | Location fraud |
| **VPN/proxy** | Hidden real IP | Masking true location |
| **Device age** | How long device has been seen | New device = higher risk |
| **App tampering** | Modified app binary | Bypass security checks |
| **Screen recording** | Screen capture active | Data exfiltration risk |
| **Debug mode** | Debugger attached | Analysis/attack in progress |

## Device Fingerprinting Techniques

| Technique | Persistence | Accuracy |
|-----------|------------|----------|
| **Hardware ID** (IMEI, serial) | Permanent | High but privacy-restricted |
| **Canvas fingerprint** | Semi-persistent (web) | Medium |
| **WebGL fingerprint** | Semi-persistent (web) | Medium |
| **Audio fingerprint** | Semi-persistent | Medium |
| **SDK-generated ID** | Per-install | High within app |
| **Behavioral fingerprint** | Session-level | Medium |

## Providers

| Provider | Key Feature |
|----------|-------------|
| **SEON** | Device fingerprinting + email/phone intelligence |
| **ThreatMetrix (LexisNexis)** | Largest device identity network (6B+ devices) |
| **BioCatch** | Behavioral biometrics + device |
| **Sardine** | Device + behavior + transaction |
| **Castle** | Account security + device |

---

## Key Takeaways

!!! success "Summary"
    - Device intelligence is a **critical pre-verification signal** — detect fraud before expensive processing
    - **Same device + multiple identities** is the strongest fraud ring indicator
    - **Root/emulator/virtual camera** detection prevents injection attacks
    - Device fingerprinting faces **privacy restrictions** (GDPR, App Tracking Transparency) — balance needed
    - Combine device signals with verification + behavioral signals for comprehensive risk scoring

---

## Related Articles

- [Risk Scoring Engines](risk-scoring-engines.md)
- [Injection Attacks](../02-biometrics-face/injection-attack.md)
- [Fraud Rings](fraud-rings-organized.md)
