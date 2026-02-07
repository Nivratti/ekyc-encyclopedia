# Disaster Recovery

## Definition

Strategies for recovering eKYC services from major failures — data center outages, regional disasters, data corruption, or security breaches.

---

## DR Metrics

| Metric | Definition | eKYC Target |
|--------|-----------|-------------|
| **RPO** | Recovery Point Objective — max data loss | < 1 hour |
| **RTO** | Recovery Time Objective — max downtime | < 4 hours |

## DR Strategies

| Strategy | RPO | RTO | Cost |
|----------|-----|-----|------|
| **Backup & restore** | Hours | Hours-days | Low |
| **Pilot light** | Minutes | 1-2 hours | Medium |
| **Warm standby** | Seconds | Minutes | High |
| **Multi-region active-active** | Zero | Zero | Very high |

---

## Key Takeaways

!!! success "Summary"
    - **Warm standby** is the sweet spot for most eKYC platforms — minutes RTO, manageable cost
    - **Biometric data backups** must be encrypted and access-controlled — even in DR scenarios
    - Regular **DR drills** are essential — test failover before you need it

---

## Related Articles

- [High Availability](high-availability.md)
- [Security Architecture](security-architecture.md)
