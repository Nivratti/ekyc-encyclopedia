# Multi-Language OCR

## Definition

Identity documents worldwide use **100+ writing systems** — Latin, Devanagari, Arabic, Chinese, Cyrillic, Thai, Korean, and more. Multi-language OCR must handle all of these with high accuracy.

---

## Script-Specific Challenges

| Script | Challenge | Accuracy |
|--------|-----------|----------|
| **Latin** | Well-solved, many fonts | 98-99% |
| **Devanagari** | Connected characters, shirorekha (headline), matras | 92-97% |
| **Arabic** | Right-to-left, connected cursive, contextual forms | 90-96% |
| **Chinese** | 3,000+ common characters, similar strokes | 95-98% |
| **Korean (Hangul)** | Syllable blocks, compositional | 96-98% |
| **Thai** | No word spacing, tonal marks above/below | 92-96% |
| **Cyrillic** | Similar to Latin but distinct characters | 97-99% |
| **Japanese** | Three scripts (kanji + hiragana + katakana) mixed | 94-97% |

## Multi-Language Solutions

| Solution | Approach |
|----------|----------|
| **PaddleOCR** | Supports 80+ languages, unified pipeline |
| **Tesseract 5** | Open-source, 100+ languages, LSTM-based |
| **Google Cloud Vision** | Cloud API, broad language support |
| **EasyOCR** | Python library, 80+ languages |
| **TrOCR** | Fine-tune per script family |

---

## Key Takeaways

!!! success "Summary"
    - **PaddleOCR** is the best practical multi-language solution (80+ languages, fast, mobile-ready)
    - **Script detection** before recognition improves accuracy — route to script-specific model
    - **Latin and Chinese** are well-solved; **Arabic and Devanagari** remain challenging
    - ID documents often have **bilingual text** — must handle multiple scripts in one image

---

## Related Articles

- [Text Recognition Models](text-recognition-models.md)
- [Document Understanding Models](document-understanding-models.md)
