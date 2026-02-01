# Identity and Access Management (IAM) Baseline

## Objective
The objective of this baseline is to ensure that access to cloud resources is tightly controlled, auditable, and aligned with business responsibilities.

For SMEs, weak identity controls are one of the most common causes of cloud security incidents. This baseline focuses on establishing clear ownership, least-privilege access, and strong authentication without unnecessary complexity.

---

## Core Principles
- Identity is the primary security perimeter in the cloud
- Access should be granted based on roles, not individuals
- Default access must be denied unless explicitly required
- All access should be traceable to a human or service identity

---

## Baseline Requirements

### 1. Centralised Identity Management
- Use a single, central identity provider for cloud access
- Avoid creating standalone cloud-only user accounts where possible
- Enforce unique identities for each user; shared accounts must not be used

---

### 2. Least Privilege Access
- Grant users and services only the permissions required to perform their role
- Avoid broad administrative roles for day-to-day operations
- Review permissions regularly and remove unused access

---

### 3. Role-Based Access Control (RBAC)
- Define roles aligned to job functions (e.g. admin, developer, read-only)
- Assign permissions to roles rather than directly to users
- Use temporary elevation for administrative tasks where supported

---

### 4. Multi-Factor Authentication (MFA)
- Enforce MFA for all users with console or administrative access
- Prioritise MFA for privileged roles and external access
- Avoid exceptions unless there is a documented business justification

---

### 5. Service Accounts and Workload Identity
- Use dedicated service accounts for applications and automation
- Prevent service accounts from being used for interactive login
- Rotate credentials regularly or use managed identity mechanisms where available

---

### 6. Access Review and Audit
- Review user and service access at least quarterly
- Remove access immediately when users leave the organisation or change roles
- Enable logging for all authentication and authorisation events

---

## Implementation Notes
This baseline is designed to be implemented incrementally. SMEs should prioritise MFA enforcement and the removal of shared or over-privileged accounts as initial steps.

Platform-specific implementation details (AWS, GCP) should follow the same principles outlined above.

---

## Expected Outcomes
When implemented correctly, this baseline should:
- Reduce the risk of account compromise
- Improve accountability and traceability
- Simplify incident investigation
- Support compliance and audit requirements
