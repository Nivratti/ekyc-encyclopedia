# High Availability Architecture

## Definition

Designing eKYC systems for **99.9%+ uptime** — redundancy, failover, health checks, and multi-region deployment to ensure verification is always available.

---

## HA Components

| Component | Strategy |
|-----------|---------|
| **API Gateway** | Multi-AZ, auto-scaling group |
| **Processing** | Multiple GPU instances, queue-based (survives instance failure) |
| **Database** | Multi-AZ RDS with read replicas |
| **Cache** | Redis cluster with replicas |
| **Message Queue** | Kafka with replication factor 3, or SQS (managed) |
| **Object Storage** | S3 (99.999999999% durability by design) |

## Availability Targets

| Tier | Uptime | Annual Downtime | For |
|------|--------|----------------|-----|
| **99.9%** | 8.77 hours/year | Standard eKYC |
| **99.95%** | 4.38 hours/year | Enterprise eKYC |
| **99.99%** | 52.6 minutes/year | Critical financial infrastructure |

---

## Key Takeaways

!!! success "Summary"
    - **Queue-based architecture** is naturally HA — processing survives instance failures
    - **Multi-AZ** deployment is the minimum for production eKYC
    - **Multi-region** needed for global availability and data sovereignty
    - **99.9% uptime** is the standard SLA for enterprise eKYC platforms

---

## Related Articles

- [Disaster Recovery](disaster-recovery.md)
- [eKYC System Architecture](ekyc-system-architecture.md)
