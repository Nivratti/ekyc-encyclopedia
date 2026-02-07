# eKYC Knowledge Base — Master Plan

## Total Files: ~210+ detailed markdown articles

---

## 00 — Foundations (12 files)
1. `what-is-kyc.md` — What is KYC, history, why it exists
2. `what-is-ekyc.md` — Electronic KYC, evolution from paper KYC
3. `kyc-vs-ekyc.md` — Detailed comparison
4. `why-ekyc-matters.md` — Business case, cost savings, conversion rates
5. `ekyc-ecosystem-overview.md` — All players: regulators, providers, banks, fintechs
6. `ekyc-end-to-end-flow.md` — Complete user journey with flowcharts
7. `ekyc-market-landscape.md` — Market size, growth, trends (2024-2030)
8. `ekyc-use-cases-by-industry.md` — Banking, fintech, telecom, insurance, crypto, gaming
9. `ekyc-global-adoption.md` — Country-by-country adoption status
10. `ekyc-challenges-and-limitations.md` — Edge cases, failures, inclusivity
11. `ekyc-future-trends.md` — Decentralized identity, AI advances, reusable KYC
12. `ekyc-vendor-landscape.md` — Major vendors comparison (Jumio, Onfido, HyperVerge, IDenfy, etc.)

## 01 — Identity Verification & Compliance (18 files)
13. `kyc-know-your-customer.md`
14. `ekyc-electronic-kyc-deep-dive.md`
15. `vkyc-video-kyc.md`
16. `ckyc-central-kyc.md` (India-specific)
17. `re-kyc-periodic-reverification.md`
18. `kyb-know-your-business.md`
19. `kyt-know-your-transaction.md`
20. `cdd-customer-due-diligence.md`
21. `edd-enhanced-due-diligence.md`
22. `sdd-simplified-due-diligence.md`
23. `aml-anti-money-laundering.md`
24. `cft-combating-financing-of-terrorism.md`
25. `fatf-financial-action-task-force.md`
26. `pep-politically-exposed-persons.md`
27. `sanctions-screening.md`
28. `adverse-media-screening.md`
29. `ubo-ultimate-beneficial-owner.md`
30. `sof-sow-source-of-funds-wealth.md`

## 02 — Biometrics & Face Technology (32 files)

### Core Concepts
31. `biometrics-overview.md` — What are biometrics, types, role in eKYC
32. `face-biometrics-in-ekyc.md` — Why face is dominant in eKYC

### Face Detection
33. `face-detection-overview.md` — What, why, how
34. `scrfd-face-detection.md` — SCRFD architecture and usage
35. `retinaface.md` — RetinaFace architecture
36. `mtcnn.md` — MTCNN pipeline
37. `face-detection-comparison.md` — SCRFD vs RetinaFace vs MTCNN vs BlazeFace

### Face Recognition
38. `face-recognition-overview.md` — 1:1 vs 1:N, embeddings, similarity
39. `face-matching-verification.md` — 1:1 selfie-to-ID matching
40. `face-identification-1-to-n.md` — 1:N search
41. `face-embeddings-feature-vectors.md` — How face embeddings work
42. `arcface.md` — ArcFace loss and architecture
43. `adaface.md` — AdaFace for quality-aware recognition
44. `cosface.md` — CosFace loss function
45. `face-recognition-comparison.md` — ArcFace vs AdaFace vs CosFace vs others

### Face Liveness / PAD
46. `pad-presentation-attack-detection.md` — Complete overview
47. `face-liveness-detection-overview.md` — Why and how
48. `active-liveness.md` — Challenge-response methods
49. `passive-liveness.md` — Single-frame / silent detection
50. `print-attack.md` — Photo print spoofing
51. `screen-replay-attack.md` — Digital display attacks
52. `3d-mask-attack.md` — Physical mask spoofing
53. `deepfake-detection.md` — Synthetic face detection
54. `injection-attack.md` — Virtual camera / API injection
55. `liveness-detection-methods-comparison.md`

### Biometric Metrics
56. `far-false-acceptance-rate.md`
57. `frr-false-rejection-rate.md`
58. `eer-equal-error-rate.md`
59. `bpcer-apcer.md` — ISO 30107 metrics for PAD
60. `acer-average-classification-error-rate.md`
61. `fmr-fnmr.md` — False Match / Non-Match Rate
62. `biometric-metrics-comparison.md` — When to use which metric

## 03 — Document Verification (20 files)

### Core
63. `document-verification-overview.md` — Role in eKYC pipeline
64. `id-document-types.md` — Passport, DL, national ID, Aadhaar, PAN, etc.
65. `document-capture-best-practices.md` — Camera, lighting, framing

### OCR & Data Extraction
66. `ocr-optical-character-recognition.md`
67. `id-parsing-data-extraction.md` — Structured field extraction
68. `mrz-machine-readable-zone.md`
69. `viz-visual-inspection-zone.md`
70. `barcode-qr-verification.md`
71. `nfc-chip-verification.md` — e-Passport / smart card chips

### Document Forensics
72. `document-forensics-overview.md`
73. `document-liveness.md` — Real vs screen/photocopy
74. `document-tampering-detection.md` — Photoshop, splicing
75. `copy-move-detection.md`
76. `splicing-detection.md`
77. `screen-recapture-detection.md`
78. `document-template-matching.md`
79. `document-classification.md` — Auto-detect document type
80. `security-features-verification.md` — Holograms, microprint, UV

### Models & Tools
81. `layoutlmv3-for-documents.md`
82. `lilt-for-documents.md`
83. `paddleocr.md`
84. `tesseract-ocr.md`
85. `document-ai-models-comparison.md`

## 04 — Digital Identity & Authentication (16 files)
86. `digital-identity-overview.md`
87. `iam-identity-access-management.md`
88. `mfa-multi-factor-authentication.md`
89. `otp-one-time-password.md`
90. `sso-single-sign-on.md`
91. `oauth-oidc.md` — OAuth 2.0 / OpenID Connect
92. `did-decentralized-identity.md`
93. `verifiable-credentials.md` — W3C standard
94. `self-sovereign-identity.md`
95. `digital-identity-wallet.md` — EU EUDI, India DigiLocker
96. `eidas-regulation.md`
97. `aadhaar-system.md` — India's biometric identity
98. `digilocker.md` — India's digital document storage
99. `fido2-webauthn.md` — Passwordless authentication
100. `zero-knowledge-proofs-identity.md`
101. `reusable-kyc.md` — Verify once, use everywhere

## 05 — Onboarding & Workflow (12 files)
102. `digital-onboarding-overview.md`
103. `customer-lifecycle-management.md`
104. `onboarding-flow-design.md` — UX best practices with flowcharts
105. `straight-through-processing.md` — STP / auto-approval
106. `manual-review-ops-queue.md`
107. `case-management-systems.md`
108. `conversion-rate-optimization.md` — Drop-off analysis
109. `tat-turnaround-time.md`
110. `workflow-orchestration-engines.md`
111. `retry-fallback-mechanisms.md`
112. `multi-channel-onboarding.md` — Web, mobile, in-branch, agent-assisted
113. `sdk-integration-patterns.md` — Mobile SDK, Web SDK, API patterns

## 06 — Fraud & Risk (16 files)
114. `identity-fraud-overview.md`
115. `synthetic-identity-fraud.md`
116. `account-takeover.md`
117. `mule-accounts.md`
118. `device-fingerprinting.md`
119. `behavioral-biometrics.md`
120. `geofencing-ip-risk.md`
121. `velocity-checks.md`
122. `risk-scoring-engines.md`
123. `fraud-detection-ml-models.md`
124. `transaction-monitoring.md`
125. `deduplication-1-to-n.md`
126. `social-engineering-attacks.md`
127. `document-fraud-typology.md`
128. `biometric-fraud-typology.md`
129. `fraud-prevention-best-practices.md`

## 07 — Regulations & Standards (18 files)
130. `gdpr-overview.md`
131. `gdpr-and-ekyc.md` — Specific implications
132. `dpdp-act-india.md`
133. `ccpa-california.md`
134. `rbi-kyc-master-direction.md` — India banking KYC rules
135. `rbi-vkyc-guidelines.md`
136. `iso-30107-pad-standard.md`
137. `iso-19795-biometric-testing.md`
138. `nist-frvt.md` — Face Recognition Vendor Test
139. `ibeta-pad-certification.md`
140. `soc2-compliance.md`
141. `pci-dss.md`
142. `fatf-recommendations-detail.md`
143. `eu-aml-directives.md` — 4AMLD, 5AMLD, 6AMLD
144. `us-bank-secrecy-act.md`
145. `data-localization-requirements.md`
146. `consent-management.md`
147. `audit-trail-requirements.md`

## 08 — AI/ML Techniques (20 files)
148. `domain-generalization.md`
149. `self-supervised-learning.md`
150. `contrastive-learning.md`
151. `vision-transformers-vit.md`
152. `cnns-for-ekyc.md` — ResNet, EfficientNet, MobileNet in eKYC
153. `knowledge-distillation.md`
154. `model-quantization.md`
155. `edge-ai-on-device-inference.md`
156. `onnx-runtime.md`
157. `tensorrt.md`
158. `coreml.md`
159. `data-augmentation-for-biometrics.md`
160. `transfer-learning-in-ekyc.md`
161. `few-shot-learning.md`
162. `anomaly-detection.md`
163. `gan-for-synthetic-data.md`
164. `diffusion-models-synthetic-faces.md`
165. `model-fairness-bias.md` — Bias in face recognition
166. `explainability-interpretability.md` — XAI for compliance
167. `federated-learning-privacy.md`

## 09 — Architecture & Integration (15 files)
168. `ekyc-system-architecture.md` — Full system design
169. `microservices-architecture.md`
170. `api-design-for-ekyc.md` — REST API patterns
171. `webhook-patterns.md`
172. `mobile-sdk-architecture.md` — Android / iOS
173. `web-sdk-architecture.md`
174. `camera-capture-pipeline.md`
175. `image-quality-assessment.md`
176. `model-serving-infrastructure.md` — Triton, TorchServe, etc.
177. `scalability-high-availability.md`
178. `security-hardening.md` — API security, model protection
179. `data-encryption-at-rest-in-transit.md`
180. `logging-monitoring-observability.md`
181. `ci-cd-for-ml-models.md` — MLOps
182. `multi-region-deployment.md`

## 10 — Case Studies & Real-World (15 files)
183. `case-study-india-banking-ekyc.md`
184. `case-study-aadhaar-ekyc.md`
185. `case-study-upi-onboarding.md`
186. `case-study-eu-eidas-digital-id.md`
187. `case-study-singapore-singpass.md`
188. `case-study-crypto-exchange-kyc.md`
189. `case-study-neobank-onboarding.md`
190. `case-study-telecom-sim-activation.md`
191. `case-study-insurance-onboarding.md`
192. `case-study-deepfake-attack-prevention.md`
193. `case-study-presentation-attack-in-wild.md`
194. `case-study-cross-border-kyc.md`
195. `case-study-financial-inclusion.md`
196. `case-study-large-scale-deduplication.md`
197. `case-study-ekyc-failure-analysis.md`

## 11 — Business & Strategy (13 files)
198. `ekyc-build-vs-buy.md`
199. `ekyc-pricing-models.md`
200. `ekyc-rfp-evaluation-criteria.md`
201. `ekyc-competitive-analysis.md`
202. `ekyc-for-startups-vs-enterprises.md`
203. `ekyc-roi-calculation.md`
204. `ekyc-implementation-roadmap.md`
205. `ekyc-testing-benchmarking.md`
206. `ekyc-vendor-evaluation-matrix.md`
207. `ekyc-consultant-positioning.md` — How to sell eKYC expertise
208. `ekyc-white-label-solutions.md`
209. `ekyc-partnership-models.md`
210. `ekyc-sales-pitch-framework.md`

---

## TOTAL: 210 files across 12 categories

Each file includes:
- Definition & overview
- Why it matters in eKYC
- How it works (technical deep dive)
- Flowcharts / diagrams (Mermaid)
- Real-world examples
- Tools & technologies
- Comparison tables where applicable
- Links to related concepts
- Key takeaways
