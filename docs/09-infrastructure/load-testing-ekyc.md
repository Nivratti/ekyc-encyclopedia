# Load Testing eKYC

## Definition

Simulating production-level traffic to validate eKYC system capacity, identify bottlenecks, and ensure reliability under peak load.

---

## Load Test Scenarios

| Scenario | Traffic Pattern | Purpose |
|----------|----------------|---------|
| **Steady state** | Constant N requests/sec | Validate baseline capacity |
| **Ramp up** | Gradually increase to peak | Find breaking point |
| **Peak spike** | Sudden 5-10x traffic burst | Validate auto-scaling response |
| **Sustained peak** | High traffic for hours | Memory leaks, GPU thermal throttling |
| **GPU saturation** | Exceed GPU capacity | Validate queue behavior, graceful degradation |

## Tools

| Tool | Best For |
|------|----------|
| **Locust** | Python-based, scriptable, distributed |
| **k6** | JavaScript-based, developer-friendly |
| **JMeter** | Traditional, comprehensive |
| **Gatling** | Scala-based, good reporting |

---

## Key Takeaways

!!! success "Summary"
    - **GPU saturation** is the most likely bottleneck — test GPU scaling specifically
    - **Auto-scaling lag** (2-5 min for new GPU instances) means you need headroom
    - Test with **realistic payloads** — actual document/selfie images, not synthetic

---

## Related Articles

- [Performance Optimization](performance-optimization.md)
- [GPU Infrastructure](gpu-infrastructure.md)
