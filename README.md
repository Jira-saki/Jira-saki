[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Jira-saki/) [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jirasak-pakdeeto-900665214/) [![Findy](https://img.shields.io/badge/Findy-Score%2062.0-007ACC?style=for-the-badge&logo=googlecloud&logoColor=white)](https://findy-code.io/skills-share/hUpw40lAr31N5) [![CKA](https://img.shields.io/badge/CKA-Certified-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)](https://www.credly.com/users/jirasak-pakdeeto) [![AWS SAA](https://img.shields.io/badge/AWS-SAA%20Certified-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)](https://www.credly.com/users/jirasak-pakdeeto)

# Hi there 👋 I'm Jirasak (Jira)

**Cloud Platform, DevSecOps & Data Infrastructure Engineer | SRE**  
Currently based in Osaka 🇯🇵 *(Relocating to Tokyo / Chiba area)*  
Specializing in Hardened Multi-Cloud Infrastructure (AWS/GCP), Kubernetes (CKA 84%), Infrastructure as Code (Terraform), and Privacy-Preserving DataSecOps. Driven by SRE, Runtime Defense, FinOps, and GitOps principles.


> 🇯🇵 **永住権（えいじゅうけん）保持・就労制限（しゅうろうせいげん）なし** | 大阪在住（内定（ないてい）後、東京・千葉へ転居（てんきょ）可能）  
> Linux/インフラ運用・AWS/GCP・Kubernetes (CKA 84%)・Terraform IaC・ランタイムセキュリティ

<details>
<summary><b>職務要約・詳細プロフィールを表示</b></summary>

- **職務要約:** Linux/インフラ運用経験。AWS/GCPマルチクラウド設計、Terraform IaCモジュール開発、Kubernetes（CKA 84%合格）運用、Falco/eBPFランタイムセキュリティ、APPI/GDPR準拠のDataSecOpsレイクハウス構築およびFinOpsを推進。
- **スキル・ポートフォリオ:** [Findy スキルページ](https://findy-code.io/skills-share/hUpw40lAr31N5) にて詳細な職務経歴およびスキル偏差値を公開しています。
</details>

---

### 🚀 Featured Engineering Projects
- **[[cloud-workload-modernization-platform](https://github.com/Jira-saki/cloud-workload-modernization-platform)]** `Enterprise Platform / Zero-Trust GKE`
  * **Architecture:** Enterprise reference blueprint migrating legacy multi-tenant workloads to immutable GKE (Container-Optimized OS, Workload Identity).
  * **Automated Remediation (240ms MTTR):** modern_ebpf Falco driver paired with Falco Talon and Calico quarantine policies to isolate compromised pods in < 1s.
  * **GitOps & Security:** Full-stack delivery via ArgoCD (App-of-Apps) validated by Checkov and Trivy pre-merge CI gates.

- **[Cloud-Native-Hardened-Infrastructure](https://github.com/Jira-saki/Cloud-Native-Hardened-Infrastructure)** `Multi-Cloud Platform / SRE`
  * **1:1 Architectural Parity:** Immutable AWS EKS (Bottlerocket, IRSA) & GCP GKE (COS, Workload Identity) via Terraform.
  * **Ingress & Observability:** AWS ALB vs. GKE Gateway API; Prometheus Operator with Alertmanager inhibition rules (k6 stress tested: 0% error rate).

- **[k8s-incident-containment-remediation](https://github.com/Jira-saki/k8s-incident-containment-remediation)** `Runtime Security / eBPF`
  * **Kernel Detection:** Falco with `modern_ebpf` driver intercepting unauthorized container syscalls.
  * **Sub-Second MTTR (<1s):** Automated webhook isolating compromised workloads via Calico quarantine NetworkPolicies.

- **[datasecops-lakehouse](https://github.com/Jira-saki/datasecops-lakehouse)** `Privacy Engineering / FinOps`
  * **Zero-Idle-Cost Lakehouse:** Serverless S3/Glue/Athena pipeline with zero crawler runtime via Partition Projection (0.50 KB scan queries).
  * **APPI/GDPR Compliance:** Ingestion-time salted SHA-256 PII pseudonymization with non-blocking DLQ Parquet routing.

- **[ai-infra-poc](https://github.com/Jira-saki/ai-infra-poc)** `AI Platform / DevSecOps`
  * **Shift-Left Security:** Automated Checkov (36/36 passed) and Trivy gates triaging baseline CVEs to 0.
  * **Hardened Node Baseline:** Ephemeral Bottlerocket EKS with IMDSv2 and KMS CMK; capped at < ¥1,000 per test run via Spot lifecycle.

<details>
<summary><b>🔍 View More Engineering Projects (Observability, Linux Internals, AI Telemetry)</b></summary>

<br>

- **[aws-vpc-flowlog-sanitizer](https://github.com/Jira-saki/aws-vpc-flowlog-sanitizer)** `AI Telemetry / SecOps`
  * **Enrich-Before-Mask:** In-memory enrichment (GeoIP, ASN, Tor) followed by salted HMAC-SHA256 masking for privacy-safe LLM incident analysis.

- **[Ephemeral-Observability-Runtime-Security-Platform](https://github.com/Jira-saki/Ephemeral-Observability-Runtime-Security-Platform)** `Go / Observability`
  * **Hardened Go Service:** Scratch/distroless Go API on kubeadm (PSS restricted, Calico default-deny) with Prometheus ServiceMonitor & Falco.

- **[The-Walking_Dead-22-Domains](https://github.com/Jira-saki/The-Walking_Dead-22-Domains)** `Linux OS Internals`
  * **Production Troubleshooting:** Deep-dive investigation and automated remediation of zombie process leakage and SIGCHLD handling in POSIX environments.

</details>

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
