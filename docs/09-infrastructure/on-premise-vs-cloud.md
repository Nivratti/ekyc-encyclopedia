# On-Premise vs Cloud Deployment

## Definition

When and why to deploy eKYC on-premise vs cloud — driven by regulation, data sovereignty, security requirements, and cost.

---

## Comparison

| Aspect | Cloud | On-Premise |
|--------|-------|-----------|
| **Setup time** | Hours-days | Weeks-months |
| **Scaling** | Auto-scaling | Manual capacity planning |
| **Cost model** | OpEx (pay-as-you-go) | CapEx (upfront hardware) |
| **Data sovereignty** | Data in cloud provider's region | Data in your own data center |
| **GPU availability** | On-demand | Fixed capacity |
| **Maintenance** | Cloud provider manages | Your team manages |
| **Compliance** | SOC2, ISO 27001 (cloud) | Full control for audit |

## When On-Premise Is Required

| Driver | Example |
|--------|---------|
| **Regulation** | Government agencies requiring data within national boundaries |
| **Military/defense** | Classified environments |
| **Banking regulation** | Some jurisdictions require on-premise biometric processing |
| **Data sovereignty** | Country without local cloud region |
| **Latency** | Edge processing at border control points |

---

## Key Takeaways

!!! success "Summary"
    - **Cloud is default** for most eKYC — faster, cheaper, more scalable
    - **On-premise** when regulation demands it — government, defense, specific banking requirements
    - **Hybrid** is increasingly common — processing on-premise, management/updates from cloud
    - eKYC vendors that offer **both deployment models** have competitive advantage

---

## Related Articles

- [Cloud Architecture](cloud-architecture-ekyc.md)
- [eKYC System Architecture](ekyc-system-architecture.md)
