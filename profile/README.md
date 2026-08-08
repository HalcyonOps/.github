# HalcyonOps

Platform engineering and DevSecOps work by [@R055LE](https://github.com/R055LE).

Most of this discipline leaves nothing behind to look at. A pipeline that
doesn't break, a cluster that doesn't page anyone, a policy that quietly blocks
a bad deploy. These repos are the parts that can be shown: each one is
self-contained, has working code and CI, and writes down why it's built the way
it is.

## Security and policy

- **[container-hardening-lab](https://github.com/HalcyonOps/container-hardening-lab)**
  CIS and Iron Bank-aligned container hardening. OPA and Kyverno policies, Cosign
  signing, SBOM generation, Falco runtime detection.
- **[iac-security-lab](https://github.com/HalcyonOps/iac-security-lab)**
  Policy-as-code static analysis for Terraform against the CIS AWS Foundations
  Benchmark, using tfsec, Trivy and OPA/Rego.

## Platform and delivery

- **[k8s-bootstrap-lab](https://github.com/HalcyonOps/k8s-bootstrap-lab)**
  Kubernetes platform bootstrap from Kind through to EKS. GitOps, observability
  and runtime security, all managed declaratively.
- **[go-deploy-lab](https://github.com/HalcyonOps/go-deploy-lab)**
  A deliberately simple Go app with a deliberately thorough deployment
  lifecycle: migrations, container hardening, GitOps, observability.
- **[mlops-pipeline-lab](https://github.com/HalcyonOps/mlops-pipeline-lab)**
  A production-grade deployment pipeline wrapped around a HuggingFace model.
  Container hardening, CI/CD, GitOps, Kyverno policy enforcement.

## Operations

- **[sre-observability-lab](https://github.com/HalcyonOps/sre-observability-lab)**
  SLO-based alerting, burn-rate math, chaos engineering, runbooks, and Grafana
  dashboards as code.

## Modules

- **[terraform-aws-secure-baseline](https://github.com/HalcyonOps/terraform-aws-secure-baseline)**
  Composable, secure-by-default AWS Terraform modules with a full authoring
  toolchain: terraform-docs, native tests, tflint, semver.

## In progress

- **[agentic-platform-lab](https://github.com/HalcyonOps/agentic-platform-lab)**
  Agent workloads on tenant-controlled, security-hardened Kubernetes. Phase 1,
  runtime evaluation.

---

These repos aren't maintained by hand. Every one is described by a
`catalog-info.yaml` rendered from a single catalog file, so topics and metadata
can't drift out of sync. A scheduled audit checks the whole fleet against policy
every week, covering repo settings and org-level posture, and opens an issue
when something slips.
