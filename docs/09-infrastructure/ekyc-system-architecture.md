# eKYC System Architecture

## Definition

The end-to-end system architecture for a production eKYC platform — from client SDK through API gateway, processing pipeline, decision engine, and storage.

---

## Reference Architecture

```mermaid
graph TD
    subgraph Client
        A[Mobile SDK / Web SDK]
    end

    subgraph "API Layer"
        B[API Gateway<br/>Rate limiting, auth, routing]
        C[Session Service<br/>State management]
    end

    subgraph "Processing Pipeline"
        D[Message Queue<br/>Kafka / SQS]
        E[Orchestrator<br/>Workflow engine]

        F[Face Service<br/>Detection, liveness, recognition]
        G[Document Service<br/>OCR, forensics, classification]
        H[Screening Service<br/>Sanctions, PEP, adverse media]
        I[Database Verification<br/>Government API calls]
    end

    subgraph "Decision & Storage"
        J[Decision Engine<br/>Rules + ML scoring]
        K[Review Queue<br/>Manual review cases]
        L[Data Store<br/>Encrypted images, results]
        M[Vector DB<br/>Face deduplication]
    end

    subgraph "Notifications"
        N[Webhook Service<br/>Async result delivery]
    end

    A --> B --> C
    C --> D --> E
    E --> F & G & H & I
    F & G & H & I --> J
    J --> K & L & N
    F --> M

    style E fill:#4051B5,color:#fff
    style J fill:#2E7D32,color:#fff
```

## Service Responsibilities

| Service | Technology | Scaling |
|---------|-----------|---------|
| **API Gateway** | Kong, AWS API Gateway, Nginx | Horizontal (stateless) |
| **Session Service** | Redis + PostgreSQL | Horizontal + replicated cache |
| **Message Queue** | Kafka (high-volume), SQS (simpler) | Partitioned |
| **Face Service** | Python + Triton on GPU | GPU auto-scaling |
| **Document Service** | Python + Triton on GPU | GPU auto-scaling |
| **Screening Service** | REST client to external APIs | Horizontal |
| **Decision Engine** | Rules engine + ML model | Horizontal (CPU) |
| **Vector DB** | Milvus / FAISS | Sharded by volume |
| **Data Store** | S3 (images) + PostgreSQL (metadata) | Standard cloud scaling |

---

## Key Takeaways

!!! success "Summary"
    - **Microservices architecture** with message queue enables independent scaling of GPU-heavy services
    - **Orchestrator** manages the verification workflow — parallel execution of face + document + screening
    - **Face and Document services** are GPU-bound — scale independently based on queue depth
    - **Decision Engine** aggregates all signals — configurable rules per client
    - All data **encrypted at rest and in transit** — compliance requirement

---

## Related Articles

- [Cloud Architecture for eKYC](cloud-architecture-ekyc.md)
- [GPU Infrastructure](gpu-infrastructure.md)
- [Microservices vs Monolith](microservices-vs-monolith.md)
