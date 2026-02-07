# Behavioral Analytics for Fraud

## Definition

Analyzing user behavior patterns during the eKYC session to detect fraudulent intent — how fast they complete steps, hesitation patterns, interaction style, and session anomalies.

---

## Behavioral Signals

| Signal | Legitimate User | Fraud Indicator |
|--------|----------------|-----------------|
| **Time to complete** | 30-90 seconds | < 10s (automated) or > 5min (struggling with fake docs) |
| **Document capture attempts** | 1-3 tries | 10+ tries (trying different fake documents) |
| **Selfie retries** | 1-2 | Many retries (spoof failing liveness) |
| **Navigation pattern** | Linear progression | Back-and-forth, hesitation |
| **Typing speed** | Consistent | Copy-pasting or auto-fill (bot-like) |
| **Session time of day** | Business hours, evening | 2-5 AM (fraud peaks at odd hours) |
| **Interaction velocity** | Natural variation | Unnaturally uniform (bot) |

---

## Key Takeaways

!!! success "Summary"
    - Behavioral analytics adds a **layer that AI spoofing can't easily fake**
    - **Session timing and retry patterns** are the strongest individual behavioral signals
    - Combine with device + verification signals for comprehensive fraud detection
    - Key providers: **BioCatch, Sardine, Featurespace**

---

## Related Articles

- [Risk Scoring Engines](risk-scoring-engines.md)
- [Behavioral Biometrics](../02-biometrics-face/behavioral-biometrics.md)
