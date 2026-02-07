# Document Fraud Patterns

## Definition

Common patterns and techniques used to create fraudulent identity documents — from simple photo editing to sophisticated counterfeiting.

---

## Fraud Pattern Taxonomy

| Pattern | Method | Sophistication | Detection |
|---------|--------|---------------|-----------|
| **Photo substitution** | Replace face photo on genuine document | Medium | ELA, edge analysis, font consistency |
| **Text editing** | Change name, DOB, or ID number | Low-High | Font analysis, noise inconsistency |
| **Whole document counterfeit** | Create complete fake document | High | Template mismatch, security feature absence |
| **Expired document modification** | Change expiry date | Low | Font analysis, compression artifacts |
| **Address alteration** | Change address on utility bill/ID | Low-Medium | Layout analysis, font mismatch |
| **Digitally printed counterfeit** | High-quality print of digitally created document | High | Print artifact analysis, no security features |
| **Scan + edit + print** | Scan real document, edit digitally, print | Medium | Double compression, print artifacts |

## Most Common Patterns by Region

| Region | Most Common Fraud | Typical Document Targeted |
|--------|------------------|--------------------------|
| **India** | Aadhaar letter editing, PAN card photo swap | Aadhaar, PAN |
| **USA** | State DL counterfeit, SSN fraud | Driving license, SSN card |
| **EU** | ID card photo substitution, residence permit forgery | National ID, residence permit |
| **UK** | Utility bill fabrication, passport alteration | Utility bills, passport |
| **SEA** | National ID counterfeit | Various national IDs |

---

## Key Takeaways

!!! success "Summary"
    - **Photo substitution and text editing** are the most common document fraud patterns
    - **Font analysis** catches most text edits — attackers rarely match the original font perfectly
    - **Regional patterns vary** — India sees Aadhaar edits, USA sees DL counterfeits
    - **Multi-signal detection** (forensics + database verification + NFC) catches what single methods miss

---

## Related Articles

- [Document Forensics Overview](../03-document-verification/document-forensics-overview.md)
- [Digital Tampering Detection](../03-document-verification/digital-tampering-detection.md)
- [Synthetic Document Detection](../03-document-verification/synthetic-document-detection.md)
