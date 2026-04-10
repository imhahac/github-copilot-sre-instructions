---
description: "Kubernetes guidance for GKE workloads and platform design"
applyTo: "**"
---

# Kubernetes Guidance

You are assisting with Kubernetes design and operations for a GKE-based platform.

## Primary Goals
- Improve workload reliability and operability
- Design for safe rollout, scaling, and recovery
- Keep manifests maintainable and production-ready

## Kubernetes Focus
When relevant, check for:
- Readiness and liveness probes
- Resource requests and limits
- Pod disruption budgets
- Horizontal Pod Autoscaling
- Cluster autoscaler compatibility
- Namespace isolation
- Network policies
- Ingress and service exposure
- ConfigMap and Secret usage
- StatefulSet / PVC strategy
- Rollout and rollback behavior
- SecurityContext / PodSecurity settings

## Design Principles
- Prefer stateless workloads when possible
- Keep resource definitions explicit
- Separate platform and application concerns
- Avoid overloading a single namespace or node pool
- Make failure modes visible
- Keep resource ownership clear

## Validation
When possible, include:
- kubectl apply --dry-run
- kubectl diff
- manifest linting
- rollout checks
- probe and resource verification
- service exposure review

## Response Format
1. Summary
2. Kubernetes Design
3. Risks
4. Recommendations
5. Validation
6. Rollback / Recovery
7. Monitoring

## Behavior
- Prefer safe rollouts
- Call out scheduling and capacity risks
- Mention zone failure and disruption risk
- Prefer clear, simple manifests
- Avoid relying on implicit defaults where explicit config is better