# GCP SRE and Infrastructure Copilot Instructions

A curated set of AI instruction files for Site Reliability Engineering and Infrastructure Architecture work in a GCP environment.

These instructions are designed to help AI assistants provide safer, more consistent, and more production-oriented guidance for:

- Site Reliability Engineering
- Infrastructure Architecture
- GCP IAM, VPC, GCE, GKE, and Cloud SQL
- Terraform-based infrastructure
- Kubernetes / GKE workloads
- Operational planning and incident-aware recommendations

---

## Why This Exists

Infrastructure and reliability work often requires consistent standards around:

- security
- rollback
- observability
- failure domains
- maintainability
- deployment safety

This repository provides reusable instruction files that help AI assistants produce more useful results for those scenarios.

---

## Supported Tools

This repository is intended for use with:

- **VS Code / GitHub Copilot**
- **Gemini / Antigravity IDE**

---

## What’s Included

### VS Code / Copilot Instructions
Place these files under `.github/instructions/`:

```text
.github/instructions/
├── sre-iam.instructions.md
├── sre-vpc.instructions.md
├── sre-gce.instructions.md
├── sre-gke.instructions.md
├── sre-cloudsql.instructions.md
├── infrastructure-architecture.instructions.md
├── terraform.instructions.md
└── kubernetes.instructions.md