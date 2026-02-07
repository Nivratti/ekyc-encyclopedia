# Text Recognition Models

## Definition

Text recognition (Stage 2 of OCR) reads the text content from detected regions, converting image patches containing text into character strings.

---

## Key Models

| Model | Architecture | Key Feature | Accuracy (IC13) |
|-------|-------------|-------------|-----------------|
| **CRNN** | CNN + BiLSTM + CTC | Classic, fast, reliable baseline | 92-95% |
| **TrOCR** | ViT encoder + GPT-2 decoder | Pretrained transformer, highest accuracy | 97-99% |
| **PaddleOCR PP-OCRv4** | Lightweight CNN + SVTR | Best practical system, mobile-ready | 96-98% |
| **SVTR** | Single Visual Transformer | No RNN, attention-based | 96-98% |
| **ABINet** | Autonomous + Bidirectional + Iterative | Built-in language model correction | 97-98% |
| **PARSeq** | Permutation-aware transformer | Handles any reading order | 97-99% |

---

## CTC vs Attention Decoding

| Approach | How It Works | Pros | Cons |
|----------|-------------|------|------|
| **CTC** | Align output to input sequence | Fast, simple, no length limit | Cannot model character dependencies |
| **Attention** | Attend to relevant input parts | Models dependencies, higher accuracy | Slower, attention drift on long text |
| **Hybrid** | CTC loss + attention decoder | Best of both | More complex training |

---

## ID Document-Specific Considerations

| Content | Best Approach | Notes |
|---------|-------------|-------|
| **Printed Latin** | Any model (well-solved) | 98%+ accuracy |
| **MRZ (OCR-B)** | Specialized MRZ recognizer | 99.5%+ with checksum validation |
| **Devanagari** | PaddleOCR / Tesseract with Indic models | 92-96% accuracy |
| **Arabic** | Right-to-left models, PaddleOCR | 90-95% accuracy |
| **Chinese** | Large character set models | 95-98% (3000+ characters) |
| **Handwritten** | HTR-specific models (TrOCR fine-tuned) | 70-90% depending on quality |

---

## Key Takeaways

!!! success "Summary"
    - **TrOCR** provides highest accuracy; **PaddleOCR** is the best practical system (fast, multilingual)
    - **CRNN + CTC** remains a solid baseline for production systems
    - Recognition accuracy: printed (98%+), MRZ (99.5%+), handwritten (70-90%)
    - For ID documents, **constrained vocabulary** (known field types) allows post-processing correction

---

## Related Articles

- [OCR Pipeline for ID Documents](ocr-pipeline-id-documents.md)
- [Text Detection Models](text-detection-models.md)
- [Multi-Language OCR](multi-language-ocr.md)
