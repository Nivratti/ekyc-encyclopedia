# MRZ Parsing

## Definition

**MRZ (Machine Readable Zone)** is a standardized text block on passports, visas, and some national IDs — printed in OCR-B font following **ICAO 9303** specifications. MRZ provides machine-readable identity data with built-in error detection through check digits.

---

## MRZ Formats

| Type | Lines | Characters/Line | Used On |
|------|-------|-----------------|---------|
| **TD1** | 3 lines | 30 characters each | ID cards (CR80 format) |
| **TD2** | 2 lines | 36 characters each | Some ID cards, older passports |
| **TD3** | 2 lines | 44 characters each | Passports, travel documents |
| **MRVA** | 2 lines | 44 characters each | Visa Type A |
| **MRVB** | 2 lines | 36 characters each | Visa Type B |

---

## MRZ TD3 Structure (Passport)

```
Line 1: P<UTOERIKSSON<<ANNA<MARIA<<<<<<<<<<<<<<<<<<<
Line 2: L898902C36UTO7408122F1204159ZE184226B<<<<<10
```

| Field | Position (Line 2) | Example | Check Digit |
|-------|------------------|---------|-------------|
| **Document number** | 1-9 | L898902C3 | Position 10 |
| **Nationality** | — (Line 1) | UTO | — |
| **Date of birth** | 14-19 | 740812 (YYMMDD) | Position 20 |
| **Sex** | 21 | F | — |
| **Expiry date** | 22-27 | 120415 (YYMMDD) | Position 28 |
| **Personal number** | 29-42 | ZE184226B | Position 43 |
| **Composite check** | 44 | 0 | Over doc# + DOB + expiry + personal# |

---

## Check Digit Calculation

MRZ uses a weighted checksum: weights cycle through 7, 3, 1 for each character position.

```python
def mrz_check_digit(data):
    weights = [7, 3, 1]
    values = []
    for char in data:
        if char == '<':
            values.append(0)
        elif char.isdigit():
            values.append(int(char))
        elif char.isalpha():
            values.append(ord(char) - ord('A') + 10)
    total = sum(v * weights[i % 3] for i, v in enumerate(values))
    return str(total % 10)
```

---

## Key Takeaways

!!! success "Summary"
    - MRZ provides **standardized, machine-readable** identity data on travel documents
    - **Check digits** enable mathematical verification of extracted data — catch OCR errors
    - **99.5%+ accuracy** achievable with OCR-B optimized recognition
    - MRZ data can be **cross-validated** with visually extracted (VIZ) data for additional confidence
    - Essential for **passport verification** in eKYC

---

## Related Articles

- [OCR Pipeline](ocr-pipeline-id-documents.md)
- [NFC Chip Reading](nfc-chip-reading.md)
- [Barcode & QR Code Reading](barcode-qr-reading.md)
