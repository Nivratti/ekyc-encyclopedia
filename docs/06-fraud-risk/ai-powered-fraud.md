# AI-Powered Fraud

## Definition

**AI-powered fraud** uses artificial intelligence tools — deepfakes, generative AI, and large language models — to create more convincing and scalable identity fraud attacks.

---

## AI Fraud Capabilities

| AI Tool | Fraud Application | Availability |
|---------|------------------|-------------|
| **Real-time face swap** (DeepFaceLive) | Impersonate victim during live eKYC | Free, open-source |
| **Face generation** (StyleGAN, SD) | Create person who never existed | Free, open-source |
| **Document generation** (SD, templates) | Create realistic fake ID documents | Medium effort |
| **Voice cloning** (ElevenLabs, VALL-E) | Impersonate victim's voice for V-KYC | Cheap, accessible |
| **LLM-assisted social engineering** | Generate convincing phishing/pretexting | Free (ChatGPT, open-source LLMs) |
| **Automated form filling** | Bots that navigate eKYC flows | Free tools available |

## The AI Fraud Escalation

| Year | Attack Capability | Defense Gap |
|------|------------------|------------|
| **2020** | Basic deepfakes, noticeable artifacts | Manageable |
| **2022** | Real-time face swap, good voice cloning | Growing |
| **2024** | Near-perfect deepfakes, AI documents, multi-modal | Significant |
| **2026+** | Full synthetic identity pipeline (AI face + AI document + AI voice) | Critical |

---

## Defense Strategies

| Defense | What It Counters |
|---------|-----------------|
| **Injection attack prevention** | Stops deepfake + virtual camera pipeline |
| **Multi-spectral liveness** | Detects non-skin materials (even with perfect visual appearance) |
| **Device attestation** | Proves image came from real camera (not software) |
| **Cryptographic image provenance (C2PA)** | Proves image hasn't been manipulated since capture |
| **Behavioral analytics** | AI-driven sessions have unnatural behavioral patterns |
| **Network analysis** | AI-generated identities still share devices/IPs |

---

## Key Takeaways

!!! success "Summary"
    - **AI dramatically lowers the barrier** to sophisticated identity fraud — free tools, minimal skill needed
    - **Real-time face swap + virtual camera** is the most dangerous current combination
    - **Injection prevention** (not just liveness detection) is the critical defense
    - **C2PA / cryptographic image provenance** is the long-term solution
    - This is the **defining security challenge** for eKYC in the next 5 years

---

## Related Articles

- [Deepfake Detection](../02-biometrics-face/deepfake-detection.md)
- [Injection Attacks](../02-biometrics-face/injection-attack.md)
- [Fraud-as-a-Service](fraud-as-a-service.md)
