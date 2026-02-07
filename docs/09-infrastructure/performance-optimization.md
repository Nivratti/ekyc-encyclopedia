# Performance Optimization

## Definition

Reducing end-to-end verification latency and maximizing throughput — from SDK capture to final decision.

---

## Latency Budget

| Stage | Target | Optimization |
|-------|--------|-------------|
| **SDK capture + upload** | < 5s | Image compression, quality pre-check on-device |
| **Image ingestion** | < 200ms | Direct S3 upload, pre-signed URLs |
| **Face processing** | < 500ms | GPU batching, TensorRT, INT8 |
| **Document processing** | < 1s | Parallel OCR + forensics, TensorRT |
| **Screening** | < 500ms | Cached lists, parallel API calls |
| **Decision** | < 100ms | In-memory rules engine |
| **Webhook delivery** | < 200ms | Async, non-blocking |
| **Total server** | < 3s | Pipeline parallelism |

## Optimization Techniques

| Technique | Impact |
|-----------|--------|
| **Pipeline parallelism** | Run face + document + screening concurrently | 
| **GPU batching** | Process multiple images in single GPU call |
| **Pre-signed upload** | Skip API server for image upload → direct to S3 |
| **Connection pooling** | Reuse DB/API connections |
| **Result caching** | Cache screening results for same-day re-checks |
| **CDN for SDK** | Fast SDK delivery globally |

---

## Key Takeaways

!!! success "Summary"
    - Target: **< 3 seconds** server-side processing (< 5 seconds total including upload)
    - **Pipeline parallelism** is the biggest win — face, document, and screening run concurrently
    - **GPU optimization** (TensorRT, INT8, batching) directly reduces the processing bottleneck
    - Pre-signed uploads bypass API server — reduces latency and API server load

---

## Related Articles

- [Model Optimization & Quantization](../08-ai-ml-techniques/model-optimization-quantization.md)
- [GPU Infrastructure](gpu-infrastructure.md)
