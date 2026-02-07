# Model Optimization & Quantization

## Definition

Techniques to make ML models faster and smaller for production deployment — quantization, pruning, graph optimization, and hardware-specific compilation.

---

## Optimization Techniques

| Technique | Speedup | Size Reduction | Accuracy Impact |
|-----------|---------|----------------|----------------|
| **INT8 quantization** | 2-4x | 4x smaller | < 1% loss |
| **FP16 (half precision)** | 1.5-2x | 2x smaller | Negligible |
| **Pruning (structured)** | 1.5-3x | 2-5x smaller | 1-3% loss |
| **TensorRT optimization** | 2-5x | — | Negligible |
| **ONNX Runtime** | 1.5-3x | — | None (same model) |
| **Operator fusion** | 1.2-1.5x | — | None |
| **Dynamic batching** | Throughput 2-8x | — | None |

## Quantization Types

| Type | Precision | When to Use |
|------|-----------|------------|
| **FP32** | Full precision | Training, reference |
| **FP16** | Half precision | GPU inference (default) |
| **INT8** | 8-bit integer | Production deployment, mobile |
| **INT4** | 4-bit integer | Aggressive compression, LLMs |

## Tools

| Tool | Platform | Best For |
|------|----------|----------|
| **TensorRT** | NVIDIA GPU | Fastest GPU inference |
| **ONNX Runtime** | Cross-platform | Portability, CPU+GPU |
| **OpenVINO** | Intel CPU/GPU | Intel hardware optimization |
| **CoreML** | Apple | iOS/macOS deployment |
| **TFLite** | Mobile | Android/iOS deployment |
| **NCNN** | Mobile | Fastest mobile inference |

---

## Key Takeaways

!!! success "Summary"
    - **INT8 quantization** is the single most impactful optimization: 2-4x faster, < 1% accuracy loss
    - **TensorRT** for NVIDIA GPUs, **ONNX Runtime** for cross-platform, **CoreML/TFLite** for mobile
    - Combine techniques: quantization + operator fusion + batching = 5-10x total speedup
    - Always validate accuracy after optimization — quantization can amplify edge-case errors

---

## Related Articles

- [Knowledge Distillation](knowledge-distillation.md)
- [Edge AI Deployment](edge-ai-deployment.md)
- [Model Serving Architecture](model-serving-architecture.md)
