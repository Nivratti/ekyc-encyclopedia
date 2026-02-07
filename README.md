# 📚 eKYC Knowledge Base

**The Complete Encyclopedia of Electronic Know Your Customer**

212 in-depth articles · 105,000+ words · 12 sections · Built with MkDocs Material

---

## What is this?

A comprehensive, structured knowledge base covering **everything about eKYC** — from foundational concepts and biometric algorithms to fraud prevention, regulatory compliance, system architecture, and business strategy. Designed as a reference for engineers, product managers, compliance officers, and anyone building or evaluating eKYC systems.

## 🔗 Live Site

👉 **[View the Knowledge Base](https://YOUR_USERNAME.github.io/ekyc-encyclopedia/)** *(update after deploying to GitHub Pages)*

---

## 📖 Sections

| # | Section | Articles | Topics |
|---|---------|----------|--------|
| 00 | **🏗️ Foundations** | 12 | What is KYC/eKYC, ecosystem, market, use cases, trends |
| 01 | **🔐 Identity Verification** | 18 | V-KYC, cKYC, KYB, AML/CFT, FATF, PEP, sanctions |
| 02 | **👤 Biometrics & Face** | 34 | Face detection, recognition, liveness, deepfakes, PAD, iBeta, NIST FRVT |
| 03 | **📄 Document Verification** | 20 | OCR pipeline, forensics, NFC, MRZ, document liveness |
| 04 | **🌐 Digital Identity** | 12 | eIDAS, VCs, DIDs, SSI, EUDI Wallet, India Stack, Singpass |
| 05 | **🚀 Onboarding Workflow** | 15 | SDK architecture, UX, decision engine, webhooks, orchestration |
| 06 | **🛡️ Fraud & Risk** | 15 | Synthetic identity, fraud rings, device intelligence, AI fraud |
| 07 | **⚖️ Regulations & Standards** | 18 | GDPR, DPDP, RBI, EU AI Act, ISO 30107, NIST 800-63 |
| 08 | **🧠 AI/ML Techniques** | 20 | Transfer learning, ViTs, distillation, MLOps, XAI |
| 09 | **🏗️ Infrastructure** | 18 | System architecture, GPU infra, security, HA, DR |
| 10 | **📋 Case Studies** | 15 | Banking, fintech, crypto, telecom, regional deployments |
| 11 | **💼 Business Strategy** | 15 | Market sizing, pricing, build vs buy, GTM, emerging markets |

---

## 🚀 Quick Start

### Prerequisites

```bash
pip install mkdocs-material
```

### Local Development

```bash
# Clone the repo
git clone https://github.com/YOUR_USERNAME/ekyc-encyclopedia.git
cd ekyc-encyclopedia

# Serve locally with hot reload
mkdocs serve

# Open http://127.0.0.1:8000
```

### Build Static Site

```bash
mkdocs build
# Output in ./site/
```

---

## 🌐 Deploy to GitHub Pages

### Option 1: One-Command Deploy

```bash
mkdocs gh-deploy
```

This builds the site and pushes to the `gh-pages` branch automatically.

### Option 2: GitHub Actions (Automated)

Add `.github/workflows/deploy.yml` (included in this repo) to auto-deploy on every push to `main`.

---

## 📁 Project Structure

```
ekyc-encyclopedia/
├── mkdocs.yml              # MkDocs configuration + nav
├── README.md               # This file
├── MASTER_PLAN.md           # Original planning document
├── .github/
│   └── workflows/
│       └── deploy.yml       # GitHub Actions CI/CD
└── docs/
    ├── index.md             # Home page
    ├── 00-foundations/       # 12 articles
    ├── 01-identity-verification/  # 18 articles
    ├── 02-biometrics-face/   # 34 articles
    ├── 03-document-verification/  # 20 articles
    ├── 04-digital-identity/  # 12 articles
    ├── 05-onboarding-workflow/  # 15 articles
    ├── 06-fraud-risk/        # 15 articles
    ├── 07-regulations-standards/  # 18 articles
    ├── 08-ai-ml-techniques/  # 20 articles
    ├── 09-infrastructure/    # 18 articles
    ├── 10-case-studies/      # 15 articles
    └── 11-business-strategy/ # 15 articles
```

---

## 🛠️ Tech Stack

- **[MkDocs](https://www.mkdocs.org/)** — Static site generator
- **[Material for MkDocs](https://squidfunk.github.io/mkdocs-material/)** — Theme with search, dark mode, navigation
- **Mermaid** — Diagrams and flowcharts
- **GitHub Pages** — Hosting

---

## 📄 License

This knowledge base is intended for educational and reference purposes.

---

## 🙏 Acknowledgments

Built as a comprehensive reference for the eKYC industry, synthesizing knowledge from academic papers, industry standards (NIST, ISO, ICAO, FATF), regulatory frameworks, and vendor documentation.
