# Address Verification

## Definition

**Address verification** confirms a customer's residential address using supporting documents — utility bills, bank statements, or government correspondence. It is a required component of CDD in most jurisdictions.

---

## Accepted Address Proof Documents

| Document | Recency Requirement | Common Jurisdictions |
|----------|-------------------|---------------------|
| **Utility bill** (electricity, gas, water) | < 2-3 months | Global |
| **Bank/credit card statement** | < 2-3 months | Global |
| **Tax assessment** | Current year | India, UK |
| **Government correspondence** | < 6 months | Various |
| **Rental agreement** | Current, registered | India |
| **Aadhaar** (with address) | Current | India |

## Verification Approaches

| Approach | Method |
|----------|--------|
| **OCR extraction** | Extract name + address from utility bill, match against declared address |
| **Database verification** | Check address against credit bureau, postal, or government records |
| **Geo-verification** | GPS location during eKYC compared with declared address |
| **Digital document pull** | DigiLocker, Open Banking — pull address proof digitally |

---

## Key Takeaways

!!! success "Summary"
    - Address verification is required for **CDD compliance** in most jurisdictions
    - **OCR on utility bills** is the most common approach — extract and match address
    - **Digital verification** (DigiLocker, Open Banking) is replacing paper documents
    - **Recency matters** — documents must be within 2-3 months

---

## Related Articles

- [Customer Due Diligence (CDD)](../01-identity-verification/cdd-customer-due-diligence.md)
- [OCR Pipeline](ocr-pipeline-id-documents.md)
