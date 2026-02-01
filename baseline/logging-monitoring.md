# Logging, Monitoring, and Visibility Baseline

## Objective
The objective of this baseline is to ensure that security-relevant activity within the cloud environment is visible, traceable, and available for investigation.

For SMEs, lack of visibility is a major barrier to detecting and responding to security incidents. This baseline focuses on establishing consistent logging and basic monitoring without requiring complex tooling.

---

## Core Principles
- You cannot secure what you cannot see
- Logs should be centralised and protected from tampering
- Monitoring should prioritise high-risk activity
- Visibility should support both security and operations

---

## Baseline Requirements

### 1. Centralised Logging
- Enable logging for all cloud control plane activities
- Centralise logs into a single logging platform or account
- Protect logs from deletion or modification by non-administrators

---

### 2. Identity and Access Logs
- Log all authentication and authorisation events
- Monitor for failed login attempts and privilege changes
- Retain identity logs for a defined minimum period

---

### 3. Network and Resource Activity Logs
- Enable logging for network traffic and firewall decisions where supported
- Log creation, modification, and deletion of cloud resources
- Monitor for unexpected or unauthorised changes

---

### 4. Alerting and Monitoring
- Define alerts for high-risk events (e.g. admin access changes, disabled security controls)
- Avoid excessive alerting that cannot be acted upon
- Ensure alerts are delivered to a monitored communication channel

---

### 5. Log Retention and Review
- Define a minimum log retention period aligned with business and compliance needs
- Review logs periodically, even in the absence of incidents
- Ensure logs are accessible during incident investigations

---

## Implementation Notes
SMEs should prioritise enabling control plane and identity logs as an initial step.

Monitoring should focus on a small number of meaningful alerts that indicate potential compromise or misconfiguration.

---

## Expected Outcomes
When implemented correctly, this baseline should:
- Improve detection of security incidents
- Enable faster investigation and response
- Increase accountability for changes and access
- Support compliance and audit requirements
