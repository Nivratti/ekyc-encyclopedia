# GPU Infrastructure

## Definition

GPU selection, management, and cost optimization for eKYC ML inference workloads.

---

## GPU Selection for eKYC

| GPU | VRAM | eKYC Throughput | Cost/hr (Cloud) | Best For |
|-----|------|----------------|-----------------|----------|
| **T4** | 16GB | 50-100 verifications/min | $0.50-1.00 | Cost-optimized, standard workloads |
| **A10G** | 24GB | 80-150 verifications/min | $1.00-1.50 | Balanced performance/cost |
| **L4** | 24GB | 100-200 verifications/min | $0.80-1.20 | Newest generation, efficient |
| **A100 (40GB)** | 40GB | 200-400 verifications/min | $3.00-4.00 | High-volume, batch processing |
| **H100** | 80GB | 400-800 verifications/min | $8.00-12.00 | Maximum throughput |

## Cost Optimization

| Strategy | Savings |
|----------|---------|
| **Spot/preemptible instances** | 60-80% cost reduction (use for non-critical batch) |
| **Reserved instances** | 30-60% for committed usage |
| **Right-sizing** | T4 often sufficient — don't default to A100 |
| **Multi-model per GPU** | Run liveness + recognition + OCR on same GPU via Triton |
| **Dynamic scaling** | Scale to zero during low-traffic hours |
| **INT8 quantization** | Same GPU handles 2-4x more requests |

---

## Key Takeaways

!!! success "Summary"
    - **T4/L4** are the sweet spot for most eKYC workloads — best cost/performance ratio
    - **Multi-model serving** (Triton) maximizes GPU utilization — don't dedicate one GPU per model
    - **Spot instances** for batch processing, **reserved** for baseline, **on-demand** for spikes
    - INT8 quantization effectively **doubles GPU capacity** at minimal accuracy cost

---

## Related Articles

- [Model Serving Architecture](../08-ai-ml-techniques/model-serving-architecture.md)
- [Cost Optimization](cost-optimization.md)
