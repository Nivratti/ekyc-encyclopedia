# Few-Shot & Zero-Shot Learning

## Definition

Learning from minimal (few-shot) or no (zero-shot) task-specific examples — enabling eKYC systems to handle new document types, new attack types, or new demographics without extensive retraining.

---

## Applications in eKYC

| Scenario | Approach | Example |
|----------|----------|---------|
| **New document type** | Few-shot classification | New country ID with 5-10 sample images |
| **New attack type** | Zero-shot detection | Detect unseen mask type using learned spoof features |
| **New language OCR** | Few-shot adaptation | Recognize new script with minimal labeled text |
| **Rare fraud pattern** | Few-shot anomaly detection | Detect pattern seen only 2-3 times before |

## Key Methods

| Method | How It Works |
|--------|-------------|
| **Prototypical Networks** | Learn class prototypes from few examples, classify by nearest prototype |
| **MAML** | Meta-learn initialization that adapts quickly to new tasks |
| **CLIP zero-shot** | Use language-vision model to classify without task-specific training |
| **Siamese Networks** | Learn similarity function, compare new examples to references |

---

## Key Takeaways

!!! success "Summary"
    - Few-shot learning enables rapid adaptation to **new document types and attack types**
    - **CLIP-based zero-shot** is emerging as powerful for document classification without training
    - **Meta-learning (MAML)** enables quick adaptation to new domains with minimal data
    - Critical for eKYC vendors supporting **200+ countries** — can't collect large datasets for every document type

---

## Related Articles

- [Foundation Models for eKYC](foundation-models-ekyc.md)
- [Document Classification](../03-document-verification/document-classification.md)
