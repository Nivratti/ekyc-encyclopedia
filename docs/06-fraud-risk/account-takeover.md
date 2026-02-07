# Account Takeover (ATO)

## Definition

**Account takeover** occurs when a fraudster gains unauthorized access to an existing, legitimately verified account — bypassing the initial eKYC by compromising the account after onboarding.

---

## ATO Methods

| Method | How It Works | Prevalence |
|--------|-------------|-----------|
| **Credential stuffing** | Use stolen username/password from data breaches | Very common |
| **Phishing** | Trick user into revealing credentials | Very common |
| **SIM swapping** | Convince telecom to transfer victim's number → intercept OTP | Growing |
| **Social engineering** | Call center manipulation to reset credentials | Common |
| **Malware/keylogger** | Capture credentials from infected device | Common |
| **Session hijacking** | Steal active session tokens | Technical |

## Relevance to eKYC

| Aspect | Details |
|--------|---------|
| **Post-KYC problem** | ATO happens after initial verification — eKYC alone doesn't prevent it |
| **Re-authentication** | Step-up verification (re-verify face) when suspicious activity detected |
| **SIM swap detection** | Check if phone number recently ported before OTP-based verification |
| **Behavioral biometrics** | Detect if account user's behavior pattern suddenly changes |

---

## Key Takeaways

!!! success "Summary"
    - ATO is a **post-onboarding** threat — eKYC prevents it only if re-authentication is triggered
    - **SIM swapping** specifically undermines OTP-based verification — critical for eKYC
    - **Behavioral biometrics** and **re-authentication** are the primary defenses
    - eKYC providers increasingly offer **continuous authentication** products alongside onboarding

---

## Related Articles

- [Identity Fraud Overview](identity-fraud-overview.md)
- [Behavioral Biometrics](../02-biometrics-face/behavioral-biometrics.md)
- [Re-KYC](../01-identity-verification/re-kyc-periodic-reverification.md)
