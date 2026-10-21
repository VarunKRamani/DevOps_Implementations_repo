# About the project
- We move beyond simple deployments to explore how industry-standard tools interact to create a secure software supply chain.
- We Will see how infrastructure is provisioned as code, how pipelines are hardened with automated security gates, and how ArgoCD ensures the cluster state matches your configuration repository.


**🛠️ The Tech Stack & Architecture:**
Infrastructure as Code (IaC):
Terraform: Complete provisioning of AWS VPC, Subnets, IAM Roles, and the EKS Cluster. Infrastructure as ephemeral and reproducible.

**Continuous Integration (CI) & Security:**
- **Jenkins**: The automation engine orchestrating the pipeline.
- **SonarQube**: Integrated for Static Application Security Testing (SAST) to catch code smells and vulnerabilities early.
- **Trivy**: Applied for container image scanning (CVE detection in OS/layers) and filesystem scanning.
- **Docker**: Building optimised container images.

**Continuous Delivery (CD) & GitOps:**
- **ArgoCD**: The GitOps controller running inside K8S. It monitors the manifest repository and automatically syncs changes to the cluster, ensuring zero drift.

**AWS EKS**: The managed Kubernetes control plane hosting the workload.
