# Vector Database for Face Search

## Definition

Vector databases enable fast similarity search across millions of face embeddings — powering 1:N face deduplication in eKYC.

---

## Technology Options

| Database | Type | Search Speed (1M vectors) | Scaling |
|----------|------|--------------------------|---------|
| **FAISS** | Library (Facebook) | < 5ms | In-memory, sharding manual |
| **Milvus** | Purpose-built vector DB | < 10ms | Distributed, cloud-native |
| **Pinecone** | Managed service | < 20ms | Fully managed |
| **Qdrant** | Open-source vector DB | < 10ms | Distributed |
| **Weaviate** | Vector DB + object storage | < 15ms | Managed or self-hosted |
| **pgvector** | PostgreSQL extension | < 50ms | PostgreSQL scaling |

## Index Types

| Index | How It Works | Best For |
|-------|-------------|----------|
| **IVF (Inverted File)** | Cluster vectors, search nearest clusters | 1-10M vectors |
| **HNSW** | Hierarchical graph-based search | Low-latency, < 10M |
| **IVF + PQ** | IVF with product quantization compression | 10M-1B vectors |
| **DiskANN** | Disk-based index | > 1B vectors, cost-optimized |

---

## Key Takeaways

!!! success "Summary"
    - **FAISS** (IVF+PQ) is the standard for high-performance face search — < 5ms for millions of vectors
    - **Milvus** is the best managed vector database for production eKYC deduplication
    - **Index choice** depends on scale: HNSW (< 10M, lowest latency) vs IVF+PQ (> 10M, memory-efficient)
    - At **Aadhaar scale (1.4B)**, custom sharding across multiple FAISS/Milvus clusters is needed

---

## Related Articles

- [Face De-Duplication](../02-biometrics-face/face-deduplication.md)
- [GPU Infrastructure](gpu-infrastructure.md)
