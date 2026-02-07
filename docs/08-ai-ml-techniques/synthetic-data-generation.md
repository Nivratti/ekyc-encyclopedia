# Synthetic Data Generation

## Definition

**Synthetic data generation** creates artificial training data using generative models or rendering engines — enabling training on scenarios that are rare, expensive, or impossible to collect in the real world.

---

## Generation Methods

| Method | How It Works | Quality | eKYC Use |
|--------|-------------|---------|----------|
| **GAN-based** | Train GAN to generate realistic images | High | Synthetic faces, synthetic attacks |
| **Diffusion-based** | Stable Diffusion/DALL-E generate from prompts | Very High | Document variations, scene generation |
| **3D rendering** | Render faces/documents with controlled parameters | Controllable | Face liveness (3D face + spoof simulation) |
| **Rule-based** | Programmatic manipulation of real images | Variable | Synthetic tampered documents |
| **Digital twin** | Simulate complete capture environment | High | Camera + lighting + attack simulation |

## Applications in eKYC

| Application | Synthetic Data Type |
|-------------|-------------------|
| **Liveness training** | Synthetic spoof images (simulated print/screen/mask) |
| **Face recognition** | Synthetic faces for privacy-compliant training |
| **Document forensics** | Synthetically tampered documents (known ground truth) |
| **Document OCR** | Synthetic text on document backgrounds |
| **Bias mitigation** | Generate underrepresented demographic groups |

---

## Key Takeaways

!!! success "Summary"
    - Synthetic data solves **data scarcity** (rare attacks), **privacy** (no real PII), and **bias** (balanced demographics)
    - **Diffusion models** produce the highest-quality synthetic images currently
    - **Known ground truth** is the biggest advantage — every pixel of synthetic data has a label
    - Risk: **domain gap** between synthetic and real data can limit model performance
    - Best practice: **mix synthetic + real data** rather than training on synthetic alone

---

## Related Articles

- [Data Augmentation](data-augmentation-ekyc.md)
- [Liveness Datasets](../02-biometrics-face/liveness-datasets.md)
