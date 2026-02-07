# NIST FRVT

## Definition

**NIST FRVT (Face Recognition Vendor Test)** is the most authoritative independent benchmark for face recognition technology, operated by the National Institute of Standards and Technology (USA). FRVT evaluates algorithms submitted by vendors and researchers against standardized datasets and protocols.

---

## FRVT Tracks

| Track | What It Tests | Key Metric |
|-------|-------------|-----------|
| **1:1 Verification** | Same-person verification accuracy | FNMR at fixed FMR thresholds |
| **1:N Identification** | Search accuracy in large galleries | FNIR at fixed FPIR |
| **FATE (Fairness)** | Demographic performance differentials | FMR/FNMR ratios across demographics |
| **MORPH** | Age-related accuracy changes | Performance on age-separated pairs |
| **Quality** | Face image quality estimation | Correlation with verification performance |

---

## How FRVT Works

1. **Vendors submit compiled algorithms** (not source code) to NIST
2. NIST runs them on **sequestered datasets** (images vendors have never seen)
3. Results are published in **ongoing reports** (updated regularly)
4. Vendors can resubmit improved versions

### Key Datasets Used

| Dataset | Size | Source |
|---------|------|--------|
| **Visa photos** | Millions | US State Department |
| **Mugshots** | Millions | Law enforcement |
| **Wild/border** | Large | Various operational sources |
| **Webcam** | Large | Various |

---

## Top Performers (Recognition)

The top-performing algorithms achieve:

| Metric | Top Performance (2024) |
|--------|----------------------|
| **1:1 FNMR @ FMR=1e-6** | ~0.1% (visa photos) |
| **1:N FNIR @ FPIR=1e-3** | ~0.5% (1M gallery) |
| **Cross-age (10+ years)** | ~2% FNMR |

**Consistently top-ranked vendors:** NEC, Idemia, Sensetime, Innovatrics, Paravision, Clearview

---

## FRVT FATE (Fairness)

NIST FATE evaluates demographic differentials:

| Finding | Details |
|---------|---------|
| **Skin tone** | Many algorithms show higher FMR for darker skin tones |
| **Age** | Higher error rates for elderly and very young |
| **Gender** | Some algorithms less accurate for women |
| **Improvement trend** | Top algorithms show much smaller differentials than average |

---

## Key Takeaways

!!! success "Summary"
    - NIST FRVT is the **gold standard** for face recognition evaluation — independent, rigorous, ongoing
    - Top algorithms achieve **99.9%+ accuracy** on controlled images, but degrade on cross-age/quality
    - **FRVT ranking is a major sales tool** for eKYC vendors selling to enterprises
    - **FATE fairness evaluation** is increasingly important — demographic bias is documented and measurable
    - FRVT tests **recognition only** — not liveness (that's ISO 30107 / iBeta territory)

---

## Related Articles

- [Biometric Performance Metrics](biometric-performance-metrics.md)
- [Face Recognition Architectures](face-recognition-architectures.md)
- [Biometric Fairness & Bias](biometric-fairness-bias.md)
