# Synthetic Document Detection

## Definition

**Synthetic document detection** identifies identity documents that are **entirely AI-generated** — created from scratch using generative AI rather than altered from genuine documents. As AI image generation improves, fully synthetic fake IDs are becoming a growing threat.

---

## Generation Methods

| Method | Quality | Cost |
|--------|---------|------|
| **Photoshop templates** | Medium | Low — templates available on dark web |
| **GAN-generated** | High | Medium — requires training data |
| **Stable Diffusion / DALL-E** | Variable-High | Low — text-to-image prompts |
| **Specialized forgery tools** | Very High | Medium — purpose-built for document fraud |

## Detection Approaches

| Approach | What It Detects |
|----------|----------------|
| **GAN artifact analysis** | Frequency-domain artifacts from GAN generation |
| **Consistency checks** | Font consistency, alignment precision, security feature presence |
| **Template matching** | Compare layout/design against known genuine templates |
| **Physical cue absence** | Real documents have micro-variations from printing — synthetics are too perfect |
| **Cross-database verification** | Verify document number exists in government database |

---

## Key Takeaways

!!! success "Summary"
    - **AI-generated fake IDs** are an emerging threat — generation quality is improving rapidly
    - Detection combines **GAN artifact analysis**, **template consistency**, and **database verification**
    - **Database verification** is the strongest defense — a fake document number won't exist in government records
    - This is a **rapidly evolving threat** requiring continuous model updates

---

## Related Articles

- [Document Forensics Overview](document-forensics-overview.md)
- [Deepfake Detection](../02-biometrics-face/deepfake-detection.md)
