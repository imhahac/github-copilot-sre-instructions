# GCP SRE and Infrastructure Copilot Instructions

Reusable AI instruction files for Site Reliability Engineering and Infrastructure Architecture in GCP.

This repository provides a structured set of guidance files for AI assistants so they can give safer, more consistent, and more production-oriented help with:

- Site Reliability Engineering
- Infrastructure Architecture
- GCP IAM, VPC, GCE, GKE, and Cloud SQL
- Terraform-based infrastructure
- Kubernetes / GKE workloads
- Operational planning, rollout safety, and incident-aware recommendations

---

## Overview

Infrastructure and reliability work require consistent standards around:

- security
- rollback
- observability
- failure domains
- maintainability
- deployment safety

This repository centralizes those standards into reusable instruction files for AI tools.

---

## Supported Tools

This repository is intended for:

- **VS Code / GitHub Copilot**
- **Gemini / Antigravity IDE**

---

## Recommended Usage

### Start with the general guidance
Use these files first:

- `infrastructure-architecture.instructions.md`
- `terraform.instructions.md`
- `kubernetes.instructions.md`

These provide the broadest guidance and apply to most infrastructure work.

### Add service-specific guidance as needed
Use the service-specific files when working on focused topics:

- IAM and access control
- VPC and networking
- GCE workloads
- GKE operations
- Cloud SQL reliability

### Keep both tool families aligned
If you use both VS Code / Copilot and Gemini / Antigravity, keep the corresponding files aligned so the guidance remains consistent across tools.

---

## How It Works

The instruction files are designed to help AI tools:

- prioritize reliability and safety
- highlight risks and rollback needs
- consider monitoring and alerting
- suggest practical implementation steps
- align recommendations with GCP, Terraform, and Kubernetes best practices

Different tools may interpret repository context differently, but these files provide a shared baseline for infrastructure and reliability decisions.

---

## Installation / Setup

### VS Code / GitHub Copilot
1. Copy the Copilot instruction files into `.github/instructions/`.
2. Open the repository in VS Code.
3. Ask Copilot to help with infrastructure, operations, or reliability tasks.
4. Copilot should follow the relevant instruction file automatically.

### Gemini / Antigravity IDE
1. Copy the `GEMINI_*.md` files into the repository root.
2. Open the repository in Gemini or Antigravity.
3. Ask the assistant to review or design infrastructure.
4. The assistant should use the matching guidance file as project context.

### Recommended initial verification
After setup, test with prompts such as:

- “Review this Terraform module for safety and maintainability.”
- “How should this GKE workload be deployed safely?”
- “What risks do you see in this IAM change?”
- “How would you design this Cloud SQL failover path?”

---

## Suggested Workflow

1. Start with the general architecture and tooling files.
2. Add service-specific rules for the area you are working on.
3. Review the AI output for:
   - correctness
   - reliability
   - security
   - rollback strategy
   - observability
4. Refine the files over time based on your team’s standards and platform needs.
5. Re-run representative prompts after major updates to verify the guidance still behaves as expected.

---

## Best Practices for Editing These Files

When customizing the instructions:

- keep language clear and direct
- prefer production-ready guidance over theory
- call out risk, rollback, and monitoring
- avoid unnecessary complexity
- use explicit checks and response formats
- keep general guidance in shared files and special cases in service-specific files
- keep Copilot and Gemini versions consistent when possible
- prefer small, reviewable changes
- update the README when structure or usage changes

---

## File Overview

### VS Code / Copilot Files
- `sre-iam.instructions.md` — IAM and access control guidance
- `sre-vpc.instructions.md` — Networking and VPC guidance
- `sre-gce.instructions.md` — Compute Engine reliability guidance
- `sre-gke.instructions.md` — GKE and Kubernetes operations guidance
- `sre-cloudsql.instructions.md` — Cloud SQL reliability guidance
- `infrastructure-architecture.instructions.md` — General infrastructure architecture guidance
- `terraform.instructions.md` — Terraform best practices and safety guidance
- `kubernetes.instructions.md` — Kubernetes design and operations guidance

### Gemini / Antigravity IDE Files
- `GEMINI_IAM.md` — IAM and access control guidance
- `GEMINI_VPC.md` — VPC and networking guidance
- `GEMINI_GCE.md` — Compute Engine guidance
- `GEMINI_GKE.md` — GKE guidance
- `GEMINI_CLOUDSQL.md` — Cloud SQL guidance
- `GEMINI_INFRA.md` — General infrastructure architecture guidance
- `GEMINI_TERRAFORM.md` — Terraform guidance
- `GEMINI_KUBERNETES.md` — Kubernetes guidance

---

## Project Layout

```text
.github/
└── instructions/
    ├── sre-iam.instructions.md
    ├── sre-vpc.instructions.md
    ├── sre-gce.instructions.md
    ├── sre-gke.instructions.md
    ├── sre-cloudsql.instructions.md
    ├── infrastructure-architecture.instructions.md
    ├── terraform.instructions.md
    └── kubernetes.instructions.md

GEMINI_IAM.md
GEMINI_VPC.md
GEMINI_GCE.md
GEMINI_GKE.md
GEMINI_CLOUDSQL.md
GEMINI_INFRA.md
GEMINI_TERRAFORM.md
GEMINI_KUBERNETES.md
README.md