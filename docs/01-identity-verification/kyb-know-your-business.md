# KYB — Know Your Business

## Definition

**KYB (Know Your Business)** is the process of verifying the identity and legitimacy of a business entity before establishing a financial relationship. While KYC focuses on individuals, KYB addresses the more complex task of verifying companies, their ownership structures, directors, and beneficial owners.

---

## Why KYB is More Complex Than KYC

```mermaid
graph TD
    A[Individual KYC] --> B[Verify 1 person<br/>1 ID document + 1 selfie]

    C[Business KYB] --> D[Verify the entity<br/>Registration, licenses]
    C --> E[Verify directors<br/>Individual KYC on each]
    C --> F[Identify UBOs<br/>Ownership chain investigation]
    C --> G[Verify authorized signatories]
    C --> H[Understand business activity]
    C --> I[Assess source of funds]

    style A fill:#2E7D32,color:#fff
    style C fill:#e53935,color:#fff
```

---

## KYB Verification Process

```mermaid
graph TD
    A[Business Account Application] --> B[Entity Verification]
    B --> B1[Company registration check<br/>MCA, Companies House, SEC]
    B --> B2[Legal status verification<br/>Active, dormant, struck off]
    B --> B3[License verification<br/>Industry-specific permits]

    B1 & B2 & B3 --> C[Ownership Structure]
    C --> C1[Identify all shareholders]
    C --> C2[Trace to UBOs - 25%+ ownership]
    C --> C3[Identify controlling persons]

    C1 & C2 & C3 --> D[Individual KYC on Key Persons]
    D --> D1[KYC on all directors]
    D --> D2[KYC on all UBOs]
    D --> D3[KYC on authorized signatories]

    D1 & D2 & D3 --> E[Screening]
    E --> E1[Sanctions check - entity + individuals]
    E --> E2[PEP check on all individuals]
    E --> E3[Adverse media on entity + individuals]

    E1 & E2 & E3 --> F[Risk Assessment]
    F --> G{Decision}

    style A fill:#4051B5,color:#fff
```

### Documents Required

| Document | Purpose |
|----------|---------|
| **Certificate of Incorporation** | Proves entity legally exists |
| **Memorandum & Articles of Association** | Business purpose, shareholder rights |
| **Board resolution** | Authorization to open account |
| **Shareholder register** | Identify all owners |
| **UBO declaration** | Declare beneficial owners (25%+ threshold) |
| **Financial statements** | Assess business activity and SOF |
| **Trade licenses** | Industry-specific authorization |
| **GST/VAT certificate** | Tax registration proof |
| **Directors' KYC** | Individual identity verification for each director |

---

## Complex Ownership Structures

The main challenge of KYB — tracing who really owns and controls the entity:

```mermaid
graph TD
    A[Target Company] --> B[Shareholder: Company B - 60%]
    A --> C[Shareholder: Individual X - 25%]
    A --> D[Shareholder: Trust T - 15%]

    B --> E[Shareholder: Company C - 80%]
    B --> F[Shareholder: Individual Y - 20%]

    E --> G["UBO: Individual Z - 80% of C<br/>= 80% × 60% = 48% of Target<br/>✅ UBO (> 25%)"]

    C --> H["UBO: Individual X - 25%<br/>✅ UBO (= 25%)"]

    D --> I[Trustee: Individual W]
    I --> J["Controlling Person<br/>⚠️ May be UBO depending on trust terms"]

    style G fill:#e53935,color:#fff
    style H fill:#e53935,color:#fff
```

---

## KYB by Jurisdiction

| Jurisdiction | UBO Threshold | Key Registry | Special Requirements |
|-------------|--------------|-------------|---------------------|
| **India (RBI)** | 25% or controlling interest | MCA (Ministry of Corporate Affairs) | UBO declaration mandatory |
| **EU (AMLD)** | 25% + 1 share | National UBO registers (public) | Public UBO register access |
| **USA** | 25% equity + 1 control person | FinCEN BOI (from 2024) | Corporate Transparency Act |
| **UK** | 25% + significant control | Companies House PSC Register | Public PSC register |
| **Singapore** | 25% or significant interest | ACRA | Registrable Controllers register |

---

## Key Takeaways

!!! success "Summary"
    - KYB is **significantly more complex** than individual KYC — entities, ownership chains, multiple individuals
    - **UBO identification** (tracing to 25%+ natural person owners) is the hardest and most important part
    - **Individual KYC must be performed** on all directors, UBOs, and authorized signatories
    - **Complex structures** (holding companies, trusts, nominees) are used to obscure ownership — KYB must penetrate these
    - **Corporate Transparency Act** (US) and **public UBO registers** (EU) are making ownership data more accessible

---

## Related Articles

- **Previous**: [← Re-KYC](re-kyc-periodic-reverification.md)
- **Next**: [KYT — Know Your Transaction →](kyt-know-your-transaction.md)
- [Ultimate Beneficial Owner (UBO)](ubo-ultimate-beneficial-owner.md)
- [Customer Due Diligence (CDD)](cdd-customer-due-diligence.md)
- [Enhanced Due Diligence (EDD)](edd-enhanced-due-diligence.md)
