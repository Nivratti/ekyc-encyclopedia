# Adverse Media Screening

## Definition

**Adverse media screening** (also called negative news screening) is the process of searching news sources, public records, and other media for negative information about customers that may indicate involvement in financial crime, fraud, corruption, or other activities that increase risk.

---

## What Adverse Media Includes

| Category | Examples |
|----------|---------|
| **Financial crime** | Money laundering charges, fraud convictions, embezzlement |
| **Corruption** | Bribery allegations, government corruption involvement |
| **Terrorism** | Links to terrorist organizations or financing |
| **Organized crime** | Association with criminal organizations |
| **Sanctions evasion** | Attempts to circumvent sanctions |
| **Tax evasion** | Tax fraud charges or investigations |
| **Regulatory action** | Fines, license revocations, enforcement actions |
| **Cybercrime** | Hacking, data theft, ransomware |
| **Environmental crime** | Illegal dumping, pollution violations |
| **Human rights** | Trafficking, forced labor associations |

---

## How Adverse Media Screening Works

```mermaid
graph TD
    A[Customer Name + Details] --> B[Search Engine]

    B --> C[News databases<br/>LexisNexis, Factiva]
    B --> D[Web search<br/>Google News, Bing]
    B --> E[Court records<br/>Legal databases]
    B --> F[Regulatory filings<br/>SEC, FCA, SEBI]
    B --> G[Social media<br/>where applicable]

    C & D & E & F & G --> H[NLP Processing]
    H --> H1[Entity resolution - is this about our customer?]
    H --> H2[Sentiment analysis - is this negative?]
    H --> H3[Category classification - what type of adverse info?]
    H --> H4[Severity scoring - how serious?]

    H1 & H2 & H3 & H4 --> I{Adverse Hit?}
    I -->|No relevant adverse media| J[Clear]
    I -->|Adverse media found| K[Risk escalation]

    K --> L[Analyst review]
    L --> M[Risk reassessment]
    M --> N[Apply EDD if warranted]

    style K fill:#F57F17,color:#000
    style J fill:#2E7D32,color:#fff
```

---

## Adverse Media Providers

| Provider | Approach | Key Feature |
|----------|----------|-------------|
| **Dow Jones** | Curated by journalists | Highest quality, structured data |
| **Refinitiv World-Check** | Curated + automated | Broad coverage |
| **ComplyAdvantage** | AI-powered, real-time | Lowest false positive rate |
| **LexisNexis** | Extensive news archives | Deep historical coverage |
| **ACAMS / Kharon** | Specialized compliance data | Targeted for compliance teams |

---

## Key Takeaways

!!! success "Summary"
    - Adverse media screening detects **negative news** that PEP and sanctions lists may not capture
    - **NLP and AI** are essential — processing millions of news articles to find relevant hits
    - **Entity resolution** is the biggest challenge — confirming the news article is about YOUR customer
    - **FATF recommends** adverse media as part of CDD and risk assessment
    - Screening should happen at **onboarding and on an ongoing basis**
    - Adverse media findings may trigger **risk reassessment and upgrade to EDD**

---

## Related Articles

- **Previous**: [← Sanctions Screening](sanctions-screening.md)
- **Next**: [Ultimate Beneficial Owner (UBO) →](ubo-ultimate-beneficial-owner.md)
- [Politically Exposed Persons (PEP)](pep-politically-exposed-persons.md)
- [Enhanced Due Diligence (EDD)](edd-enhanced-due-diligence.md)
