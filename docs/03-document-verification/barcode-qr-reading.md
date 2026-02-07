# Barcode & QR Code Reading

## Definition

Many identity documents contain **machine-readable codes** — PDF417 barcodes, QR codes, or Data Matrix — encoding structured data that can be extracted quickly and validated against visually printed information.

---

## Code Types on ID Documents

| Code Type | Found On | Data Encoded |
|-----------|----------|-------------|
| **PDF417** | US/Canadian driving licenses, some IDs | AAMVA standard: name, DOB, address, DL class, restrictions |
| **QR Code** | India Aadhaar, some EU IDs | Digitally signed identity data |
| **Data Matrix** | Some EU IDs, residence permits | Encoded identity fields |
| **1D Barcode** | Older documents | Document number, basic data |

## Aadhaar QR Code

India's Aadhaar QR contains **digitally signed XML** — verifiable offline:

| Feature | Details |
|---------|---------|
| **Content** | Name, DOB, gender, address, photo (optional), last 4 digits of Aadhaar |
| **Signature** | UIDAI digital signature — cryptographically verifiable |
| **Offline verification** | No internet needed — just validate signature against UIDAI public key |
| **Photo in QR** | Newer Aadhaar cards include compressed face photo in QR |

---

## Key Takeaways

!!! success "Summary"
    - Barcodes/QR codes provide **machine-readable, pre-structured data** — faster than OCR
    - **PDF417** is standard on US/Canadian driving licenses (AAMVA format)
    - **Aadhaar QR** enables **offline verification** with digital signature — critical for India eKYC
    - Cross-validating barcode data with OCR data detects tampering (altered visible text won't match barcode)

---

## Related Articles

- [MRZ Parsing](mrz-parsing.md)
- [OCR Pipeline](ocr-pipeline-id-documents.md)
