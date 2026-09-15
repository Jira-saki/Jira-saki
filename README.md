[![portfolio](https://img.shields.io/badge/my_portfolio-000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/Jira-saki/) [![linkedin](https://img.shields.io/badge/linkedin-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/jirasak-pakdeeto-900665214/) [![CKA](https://img.shields.io/badge/CKA-Certified-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white)](https://www.credly.com/users/jirasak-pakdeeto) [![AWS SAA](https://img.shields.io/badge/AWS-SAA%20Certified-FF9900?style=for-the-badge&logo=amazonaws&logoColor=white)](https://www.credly.com/users/jirasak-pakdeeto)

# Hi there 👋 I'm Jirasak (Jira)

Cloud Platform & Site Reliability Engineer (SRE)
Currently based in Osaka 🇯🇵 (Relocating to Tokyo / Chiba area)
Specializing in Hardened & Scalable Infrastructure, Kubernetes (CKA), and Infrastructure as Code (Terraform). Driven by SRE, Observability, DevSecOps, and GitOps principles.

---

### 🚀 Featured Engineering Projects (Platform Series)


* **[AWS-EKS-Hardened-Infrastructure (v1.2.0 - Multi-Cloud Parity)](https://github.com/Jira-saki/Cloud-Native-Hardened-Infrastructure)**  
  * **Domain:** Multi-Cloud Platform Engineering, Container Hardening & Advanced Observability  
  * **Highlights:** 
    * **1:1 Architectural Parity:** Immutable **AWS EKS (Bottlerocket OS, IRSA, KMS)** paired with a mirrored **GCP GKE (Container-Optimized OS, Workload Identity, Cloud KMS CMEK)** environment provisioned via modular Terraform.
    * **Modern Traffic Routing:** AWS ALB Ingress Controller vs. **GKE Gateway API** using container-native Network Endpoint Groups (NEGs).
    * **Hardened Observability:** Prometheus Operator with **AlertmanagerConfig CRD** featuring multi-tier routing (Critical Paging vs. ChatOps) and **Inhibition Rules** for alert fatigue elimination. Validated under **k6 spike stress testing (0% error rate)** with automated HPA scaling.

* **[The-Walking_Dead-22-Domains](https://github.com/Jira-saki/The-Walking_Dead-22-Domains)**  
  * **Domain:** Linux OS Internals & Production Troubleshooting  
  * **Highlights:** Deep-dive investigation and automated remediation of process lifecycle failures, zombie process leakage, and signal handling (`SIGCHLD`) in POSIX environments.

* **[Linux-namespace-networking-lab](https://github.com/Jira-saki/Linux-namespace-networking-lab)**
  * **Domain:** Deep Systems & Container Network Interface (CNI) Internals  
  * **Highlights:** Hands-on architectural lab exploring Linux network namespaces, veth pair bridging, packet routing, and iptables NAT masquerading—uncovering the underlying primitives of Docker and Kubernetes CNI plugins without third-party abstractions.



---

### 🛠️ Tech Stack & Ecosystem

* **Container & Orchestration:** Kubernetes (CKA Certified), Bottlerocket OS, Karpenter (Spot JIT), Docker, Helm
* **Observability & DevSecOps:** Prometheus, PromQL, Alertmanager, Grafana, OpenSearch, Checkov, Trivy, Cosign, AWS SSM
* **IaC & GitOps:** Terraform (Modular Architecture, State Isolation), ArgoCD
* **Core OS & Networking:** Linux (Ubuntu/Debian) Administration, POSIX Internals, Kernel Parameters, Bash Scripting
* **Cloud Infrastructure:** AWS (EKS, VPC Architecture, IAM/IRSA, KMS, S3, CloudWatch)
* **CI/CD & Automation:** GitHub Actions, Python (`pytest`, Infrastructure Tooling)

---

### 🎯 Certifications & Roadmap

**Active Credentials**
* ☸️ **Certified Kubernetes Administrator (CKA)** — *Linux Foundation* (Score: 84% · Aug 2026)
* ☁️ **AWS Certified Solutions Architect – Associate (SAA-C03)** — *Amazon Web Services* (Jan 2026 – Jan 2029)
* 🛡️ **Google Cybersecurity Specialization** (Issued: Oct 2024)

**Target Roadmap (2026)**
* 🧠 **Prometheus Certified Associate (PCA)** ⏳ *(In Progress / Q3 2026)*
* ☸️ **Certified Kubernetes Security Specialist (CKS)** ⏳ *(Targeting: Q4 2026)*

*(Foundational Background: AWS Data Analytics DAS [Retired], Google/IBM Data Engineering Professional Certifications)*
