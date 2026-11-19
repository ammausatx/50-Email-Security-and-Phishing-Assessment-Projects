# Project 22: Microsoft 365 Email Security Baseline Review

**Level:** Intermediate  
**Track:** Email Security & Phishing Assessment

## Objective
Assess Microsoft 365 email protection settings using an authorized tenant configuration review.

## Scope and authorization
Assess only explicitly authorized tenants, mail gateways, domains, and synthetic mailboxes. Prefer read-only review and isolated test cases. Do not send phishing content to real users or collect credentials, tokens, or personal data.

## Prerequisites
Authorized test tenant; read-only admin access; Secure Score; Exchange Online PowerShell.

## Lab setup
1. Identify the authorized tenant or isolated lab and document its owner.
2. Export baseline settings and preserve rollback copies.
3. Use synthetic accounts and sanitized test events.
4. Confirm logs are available and time-synchronized.

## Walkthrough
1. Review anti-phishing and anti-spam policies
2. Spoof intelligence
3. Safe Links/Safe Attachments licensing and policy
4. External forwarding
5. Mailbox auditing
6. Privileged roles
7. Record deviations and business exceptions.

## Example commands and tools
```bash
Get-AntiPhishPolicy
Get-HostedContentFilterPolicy
Get-RemoteDomain
```

Use vendor-supported read-only queries where possible; adapt syntax to your tenant and permissions.

## Expected output
- A control inventory and repeatable test matrix.
- Sanitized logs or configuration evidence.
- Detection results, exceptions, and analyst disposition.

## Findings and risk assessment
For each finding record condition, evidence, affected service, likelihood, impact, confidence, and compensating controls. Note false positives and dependencies such as mail-flow connectors or third-party senders.

## Framework mapping
Map applicable controls to NIST CSF 2.0, CIS Controls v8, and MITRE ATT&CK only where the evidence supports the mapping. Consider identity governance, secure configuration, audit logging, and incident response.

## Remediation
Apply least privilege, narrow exceptions, strong authentication, mail authentication alignment, alerting, and change control. Coordinate changes with mail owners and validate legitimate business workflows.

## Validation criteria
- Re-run test cases against the updated configuration.
- Confirm expected mail routing, block, quarantine, and alert outcomes.
- Verify audit coverage and incident ownership.
- Record residual risk and retest date.

## Evidence and reporting checklist
- [ ] Authorization and scope
- [ ] Baseline configuration snapshot
- [ ] Sanitized test cases and audit events
- [ ] Finding rationale and severity
- [ ] Remediation and rollback plan
- [ ] Retest evidence and residual risk

## Training illustrations
![Project 22 baseline workflow](images/01-baseline.svg)

![Project 22 analysis and findings](images/02-findings.svg)

![Project 22 validation workflow](images/03-validation.svg)

## Deliverables
A configuration assessment, safe test matrix, findings register, and remediation/retest report.
