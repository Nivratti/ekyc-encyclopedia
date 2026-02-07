# ICAO 9303 (Travel Documents)

## Definition

**ICAO Doc 9303** is the international standard for Machine Readable Travel Documents (MRTDs) — defining passport format, MRZ structure, ePassport chip specifications, and biometric data storage. Published by the International Civil Aviation Organization.

---

## What ICAO 9303 Specifies

| Component | Specification |
|-----------|--------------|
| **MRZ format** | TD1 (30×3), TD2 (36×2), TD3 (44×2) character layouts |
| **MRZ content** | Document type, name, nationality, DOB, sex, expiry, document number, check digits |
| **OCR-B font** | Standard font for MRZ printing |
| **ePassport chip** | LDS (Logical Data Structure), data groups DG1-DG16 |
| **Face photo** | ICAO face quality requirements (frontal, neutral, eyes open) |
| **Fingerprint** | Storage format for optional fingerprint data (DG3) |
| **PKI** | BAC, PACE, passive/active authentication protocols |

---

## Key Takeaways

!!! success "Summary"
    - ICAO 9303 is **the global standard** for passports and travel documents
    - Defines MRZ format, check digits, ePassport chip, and biometric storage
    - Essential for eKYC passport verification — MRZ parsing, NFC chip reading
    - Updated periodically — latest editions cover NFC security enhancements

---

## Related Articles

- [MRZ Parsing](../03-document-verification/mrz-parsing.md)
- [NFC Chip Reading](../03-document-verification/nfc-chip-reading.md)
- [Face Quality Assessment](../02-biometrics-face/face-quality-assessment.md)
