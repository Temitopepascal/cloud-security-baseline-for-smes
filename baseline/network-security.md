# Network Security and Segmentation Baseline

## Objective
The objective of this baseline is to reduce the blast radius of security incidents by controlling how workloads communicate within the cloud environment.

For SMEs, flat and overly permissive networks significantly increase risk. This baseline focuses on simple, intentional segmentation that limits exposure while remaining easy to operate.

---

## Core Principles
- Assume workloads will eventually be compromised
- Limit network access to what is explicitly required
- Separate management, application, and data traffic
- Prefer deny-by-default network rules

---

## Baseline Requirements

### 1. Network Segmentation
- Separate environments (e.g. production, staging, development) at the network level
- Avoid deploying all workloads into a single flat network
- Isolate sensitive systems from general application traffic

---

### 2. Controlled Ingress and Egress
- Restrict inbound access to workloads using explicit allow rules
- Avoid exposing services directly to the internet unless required
- Control outbound traffic to reduce data exfiltration risk

---

### 3. East–West Traffic Controls
- Limit communication between internal services to required paths only
- Avoid unrestricted internal traffic between workloads
- Use network policies or firewall rules to enforce service-to-service boundaries

---

### 4. Management Plane Separation
- Restrict administrative access to cloud resources
- Separate management access paths from application traffic
- Avoid managing infrastructure from the same network used by workloads

---

### 5. Network Monitoring and Logging
- Enable logging for network traffic where supported
- Monitor for unexpected connections or traffic patterns
- Retain network logs for incident investigation and troubleshooting

---

## Implementation Notes
SMEs should prioritise basic segmentation between environments and the restriction of public exposure as initial steps.

Network security controls should align with the IAM baseline to ensure that access is enforced consistently across identity and network layers.

---

## Expected Outcomes
When implemented correctly, this baseline should:
- Limit the impact of compromised workloads
- Reduce the risk of lateral movement
- Improve visibility into network activity
- Support faster and more effective incident response
