# Document Data Verification

## Definition

After extracting data from a document via OCR, the next step is **verifying that data** against authoritative databases — confirming that the document number, name, DOB, and other details are genuine and match official records.

---

## Verification Sources

| Source | What's Verified | Countries |
|--------|----------------|-----------|
| **Aadhaar authentication** | Name, DOB, address, photo via UIDAI API | India |
| **PAN verification** | PAN number, name via NSDL/UTITSL | India |
| **DL verification** | DL number, name, validity via Vahan/Sarathi | India |
| **DigiLocker** | Pull verified documents directly from government | India |
| **DVS (Document Verification Service)** | Passport, DL, Medicare, visa | Australia |
| **DHS SAVE** | Immigration status verification | USA |
| **Credit bureau data** | Name, address, DOB cross-reference | USA, UK, India |
| **Passport chip (NFC)** | Cryptographically signed data | Global (ePassports) |
| **Electoral roll** | Voter ID verification | India, various |

---

## Verification Types

| Type | What It Does | Confidence |
|------|-------------|-----------|
| **Database match** | Exact match of document number + name against government DB | Highest |
| **Cross-field validation** | OCR front matches MRZ matches barcode | High |
| **Checksum validation** | MRZ check digits, Aadhaar Verhoeff, Luhn for card numbers | High |
| **Pattern validation** | Document number matches expected format for that country/type | Medium |
| **Expiry check** | Document not expired | Binary |

---

## Key Takeaways

!!! success "Summary"
    - **Government database verification** provides the highest confidence — India (Aadhaar/PAN APIs) leads globally
    - **Cross-validation** between OCR, MRZ, barcode, and NFC catches tampering and OCR errors
    - **Checksum/pattern validation** provides quick local verification without API calls
    - Not all countries offer government verification APIs — coverage varies significantly

---

## Related Articles

- [OCR Pipeline](ocr-pipeline-id-documents.md)
- [NFC Chip Reading](nfc-chip-reading.md)
- [MRZ Parsing](mrz-parsing.md)
