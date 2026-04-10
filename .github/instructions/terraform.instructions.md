---
description: "Terraform guidance for GCP infrastructure"
applyTo: "**"
---

# Terraform Guidance

You are assisting with Terraform for a GCP-based platform.

## Primary Goals
- Produce safe, reusable, production-ready infrastructure code
- Favor clarity, idempotency, and modularity
- Keep environment separation explicit
- Reduce operational risk during provisioning and updates

## GCP Terraform Focus
When relevant, check for:
- Correct provider configuration
- Version pinning
- Project and billing scoping
- IAM permissions
- VPC and networking resources
- GKE and cluster resources
- GCE and instance resources
- Cloud SQL resources
- Secret Manager integration
- State management
- Artifact Registry or storage dependencies where needed

## Module Design
Prefer:
- Small, focused modules
- Clear inputs and outputs
- Minimal hidden coupling
- Reusable environment patterns
- Explicit naming conventions
- Minimal surface area per module

## Safety Checks
- Are changes idempotent?
- Is the plan understandable before apply?
- Are destructive changes clearly called out?
- Is state isolated appropriately?
- Are secrets handled securely?
- Is drift detection considered?
- Are resource dependencies intentional and minimal?
- Could a partial apply leave the environment in a broken state?

## Validation
When possible, include:
- terraform fmt
- terraform validate
- terraform plan
- policy checks
- peer review before apply

## Response Format
1. Summary
2. Architecture / Resource Design
3. Risks
4. Recommendations
5. Validation
6. Rollback / Recovery
7. Monitoring / State

## Behavior
- Prefer secure defaults
- Avoid over-complex modules
- Call out destructive changes
- Mention state and drift risks
- Prefer patterns that are easy to operate over clever abstractions