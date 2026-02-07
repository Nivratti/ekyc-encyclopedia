# Cloud Architecture for eKYC

## Definition

Cloud-specific reference architectures for deploying eKYC systems on AWS, GCP, and Azure — leveraging managed services for scalability, reliability, and security.

---

## AWS Reference Architecture

| Component | AWS Service |
|-----------|-----------|
| **API Gateway** | Amazon API Gateway |
| **Compute (GPU)** | EC2 P4d/G5 + EKS, or SageMaker Endpoints |
| **Message Queue** | SQS / MSK (Kafka) |
| **Object Storage** | S3 (SSE-KMS encrypted) |
| **Database** | RDS PostgreSQL / Aurora |
| **Cache** | ElastiCache Redis |
| **Vector Search** | OpenSearch (k-NN) / self-managed Milvus on EC2 |
| **ML Serving** | SageMaker / Triton on EKS |
| **Monitoring** | CloudWatch, X-Ray |
| **Key Management** | KMS |

## GCP Reference

| Component | GCP Service |
|-----------|-----------|
| **GPU Compute** | GKE with GPU node pools, Vertex AI |
| **Object Storage** | Cloud Storage (CMEK) |
| **Database** | Cloud SQL, AlloyDB |
| **ML Serving** | Vertex AI Endpoints, Triton on GKE |
| **Vector Search** | Vertex AI Matching Engine |

---

## Key Takeaways

!!! success "Summary"
    - All major clouds support eKYC workloads — **AWS** has the broadest GPU instance selection
    - **Managed Kubernetes (EKS/GKE/AKS)** + Triton is the most flexible GPU serving approach
    - **Multi-region deployment** required for global eKYC — data sovereignty regulations vary
    - **Managed services** reduce operational burden but increase vendor lock-in

---

## Related Articles

- [eKYC System Architecture](ekyc-system-architecture.md)
- [On-Premise vs Cloud](on-premise-vs-cloud.md)
