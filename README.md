[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Jira-saki/) [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jirasak-pakdeeto-900665214/) [![Findy](https://img.shields.io/badge/Findy-Score%2062.0-007ACC?style=for-the-badge&logo=googlecloud&logoColor=white)](https://findy-code.io/skills-share/hUpw40lAr31N5) [![CKA](https://img.shields.io/badge/CKA-Certified-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)](https://www.credly.com/users/jirasak-pakdeeto) [![AWS SAA](https://img.shields.io/badge/AWS-SAA%20Certified-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)](https://www.credly.com/users/jirasak-pakdeeto)

# Hi there 👋 I'm Jirasak (Jira)

**Cloud Platform, DevSecOps & Data Infrastructure Engineer | SRE**  
Currently based in Osaka 🇯🇵 *(Relocating to Tokyo / Chiba area)*  
Specializing in Hardened Multi-Cloud Infrastructure (AWS/GCP), Kubernetes (CKA 84%), Infrastructure as Code (Terraform), and Privacy-Preserving DataSecOps. Driven by SRE, Runtime Defense, FinOps, and GitOps principles.

<details>
<summary>🇯🇵 <b>日本語プロフィール（クリックして展開）</b></summary>

<br>

**Jirasak（SRE / Platform & DataSecOps Engineer）**
- **職務要約:** Linux/インフラ運用経験。AWS/GCPマルチクラウド設計、Terraform IaCモジュール開発、Kubernetes（CKA 84%合格）運用、Falco/eBPFランタイムセキュリティ、APPI/GDPR準拠のDataSecOpsレイクハウス構築およびFinOpsを推進。
- **ステータス:** 日本永住権（Permanent Resident）保持、就労制限なし。内定後は千葉・東京エリア（またはフルリモート）へ迅速に対応可能です。
- **スキル・ポートフォリオ:** [Findy スキルページ](https://findy-code.io/skills-share/hUpw40lAr31N5) にて詳細な職務経歴およびスキル偏差値を公開しています。

</details>

---

### 🚀 Featured Engineering Projects (Platform, Security & Data Series)

- **[Cloud-Native-Hardened-Infrastructure (v1.2.0 - Multi-Cloud Parity)](https://github.com/Jira-saki/Cloud-Native-Hardened-Infrastructure)**  
  * **Domain:** Multi-Cloud Platform Engineering, Container Hardening & Advanced Observability  
  * **Highlights:**  
    * **1:1 Architectural Parity:** Immutable **AWS EKS** (Bottlerocket OS, IRSA, KMS CMK) paired with a mirrored **GCP GKE** (Container-Optimized OS, Workload Identity, Cloud KMS CMEK) provisioned via modular Terraform.
    * **Modern Ingress & Routing:** AWS ALB Ingress Controller vs. **GKE Gateway API** utilizing container-native Network Endpoint Groups (NEGs).
    * **Hardened Observability:** Prometheus Operator with **AlertmanagerConfig CRD** (multi-tier Critical Paging vs. ChatOps) and Inhibition Rules to eliminate alert fatigue. Validated under **k6 spike stress testing (0% error rate)** with automated HPA scaling.

- **[datasecops-lakehouse](https://github.com/Jira-saki/datasecops-lakehouse)**  
  * **Domain:** Production DataSecOps, Privacy Engineering & Zero-Idle-Cost FinOps  
  * **Highlights:**  
    * **Serverless Lakehouse Architecture:** 100% serverless data pipeline leveraging modular Terraform, S3 (SSE-AES256), AWS Glue Data Catalog, and AWS Athena without operational cluster overhead.
    * **Glue Partition Projection (Zero-Crawler):** Completely eliminated periodic Glue Crawler execution costs and latency by configuring deterministic date-based partition projection, enabling instant queries with sub-kilobyte scan footprints (0.50 KB).
    * **Deterministic PII Masking (APPI/GDPR):** Ingestion-time pseudonymization of network telemetry using a salted SHA-256 cryptographic hasher (`src/utils/hasher.py`) preserving correlation capabilities while isolating corrupt payloads via non-blocking DLQ Parquet routing.
    * **Local-First Verification:** Local DuckDB OLAP zero-copy SQL analytics paired with Floci S3 emulation before AWS deployment.

- **[aws-vpc-flowlog-sanitizer](https://github.com/Jira-saki/aws-vpc-flowlog-sanitizer)**  
  * **Domain:** AI Telemetry Security, Zero-PII Ingestion Gateway & Network SecOps  
  * **Highlights:**  
    * **Enrich-Before-Mask Pattern:** Solved the LLM privacy dilemma by enriching network telemetry (GeoIP, ASN, Tor Exit Node detection, VPC subnet tiers) while raw IPs reside in volatile memory, prior to deterministic pseudonymization.
    * **Salted HMAC-SHA256 Tokenization:** One-way, deterministic token generation (`pub-ip:843d16e8`) enabling external LLMs (Claude, Gemini, Amazon Bedrock) to conduct security incident root-cause analysis without internal IP or AWS Account ID leakage.
    * **Stream & Batch Processing:** Zero-dependency Python architecture compatible with AWS Lambda S3 triggers, Kinesis Data Firehose, or sidecar log shippers.

- **[k8s-incident-containment-remediation](https://github.com/Jira-saki/k8s-incident-containment-remediation)**  
  * **Domain:** Cloud-Native Runtime Security, eBPF & Automated Incident Response  
  * **Highlights:**  
    * **Automated Closed-Loop Remediation:** Sub-second MTTR (< 1s) from unauthorized shell execution detection to full network isolation without human intervention.
    * **Kernel-Level Runtime Detection:** Falco deployed via `modern_ebpf` driver to intercept unauthorized container syscalls across a 3-node cluster.
    * **Dynamic Zero-Trust Containment:** Lightweight Python remediation webhook consuming Falcosidekick alerts to patch compromised workloads with `quarantine=true`, dynamically triggering Calico `NetworkPolicy` ingress/egress drops.

- **[ai-infra-poc](https://github.com/Jira-saki/ai-infra-poc)**  
  * **Domain:** Ephemeral AI Infrastructure, Shift-Left DevSecOps & Hardened EKS  
  * **Highlights:**  
    * **Shift-Left Security Gates:** Pre-deployment CI enforcement with Checkov IaC SAST (36/36 checks passed) and Trivy container gate blocking 16 baseline CVEs, triaged down to **0 actionable CVEs** in v1.0.1.
    * **Hardened Node Baseline:** Ephemeral AWS EKS cluster running on **Bottlerocket OS 1.63.0**, IMDSv2 enforcement (`http_tokens=required`, hop limit 2), and KMS CMK envelope encryption for Kubernetes secrets.
    * **FinOps Guardrails:** Single NAT Gateway topology and Spot instance lifecycle engineered to cap total test run costs at **< ¥1,000**.

- **[Ephemeral-Observability-Runtime-Security-Platform](https://github.com/Jira-saki/Ephemeral-Observability-Runtime-Security-Platform)**  
  * **Domain:** Cloud-Native Observability, Go Microservices & Runtime Threat Detection  
  * **Highlights:**  
    * **Full-Stack Platform Integration:** Hardened Go API compiled into a scratch/distroless image exposing `/healthz`, `/readyz`, and native Prometheus metrics (`/metrics`).
    * **End-to-End Cluster Hardening:** Provisioned via `kubeadm` (Calico CNI), enforcing Pod Security Standards (PSS restricted), default-deny `NetworkPolicy`, and Kubelet serving certs with IP SANs.
    * **Full Observability:** End-to-end metrics telemetry via `kube-prometheus-stack` (ServiceMonitor & Grafana dashboards) alongside kernel-level runtime threat detection with Falco.

- **[The-Walking_Dead-22-Domains](https://github.com/Jira-saki/The-Walking_Dead-22-Domains)**  
  * **Domain:** Linux OS Internals & Production Troubleshooting  
  * **Highlights:** Deep-dive investigation and automated remediation of process lifecycle failures, zombie process leakage, and signal handling (`SIGCHLD`) in POSIX environments.

- **[Linux-namespace-networking-lab](https://github.com/Jira-saki/Linux-namespace-networking-lab)**  
  * **Domain:** Deep Systems & Container Network Interface (CNI) Internals  
  * **Highlights:** Hands-on architectural lab exploring Linux network namespaces, `veth` pair bridging, packet routing, and `iptables` NAT masquerading—uncovering the underlying primitives of CNI plugins without third-party abstractions.

---

### 🛠️ Tech Stack & Ecosystem

- **Container & Orchestration:** Kubernetes (CKA Certified), Bottlerocket OS, Container-Optimized OS (COS), Karpenter (Spot JIT), Docker, Helm, Distroless
- **Cloud Infrastructure:** 
  - **AWS:** EKS, VPC (Flow Logs, Endpoints, Peering), IAM/IRSA, KMS CMK, S3, CloudWatch, AWS Glue, Athena
  - **GCP:** GKE, Gateway API, Workload Identity, Cloud KMS CMEK, Cloud SQL, Cloud NAT, GCS
- **DataSecOps & Privacy Engineering:** APPI / GDPR Data Compliance, Salted HMAC-SHA256 Pseudonymization, Apache Parquet (PyArrow), AWS Glue Partition Projection, DuckDB, `dlt`, Non-Blocking Dead Letter Queue (DLQ)
- **Runtime Security & Networking:** Falco (`modern_ebpf`), Calico CNI (`NetworkPolicy`), Linux Namespaces/cgroups, IMDSv2, Network Telemetry Analysis
- **IaC & GitOps:** Terraform (Modular Architecture, Remote State Backends, Workspaces), ArgoCD, FinOps / Cloud Cost Optimization
- **Observability & SRE:** Prometheus Operator, PromQL, Alertmanager (CRD Routing, Inhibition Rules), Grafana, k6 Performance Testing, OpenSearch
- **Core OS & Scripting:** Linux (Ubuntu/Debian) Administration, POSIX Internals, Kernel Tuning, Bash Scripting, Python, Go
- **CI/CD & Security Auditing:** GitHub Actions, Trivy (Container CVE Triage), Checkov (IaC SAST), Cosign, `pytest`

---

### 🎯 Certifications & Ongoing Focus

**Active Credentials**
- ☸️ **Certified Kubernetes Administrator (CKA)** — *Linux Foundation* (Score: 84% · Aug 2026)
- ☁️ **AWS Certified Solutions Architect – Associate (SAA-C03)** — *Amazon Web Services* (Jan 2026 – Jan 2029)
- 🛡️ **Google Cybersecurity Specialization** — *Google* (Issued: Oct 2024)

**In Active Preparation**
- 📊 **Certified Kubernetes Security Specialist (CKS)** — *Linux Foundation* (Target: Nov 2026)
