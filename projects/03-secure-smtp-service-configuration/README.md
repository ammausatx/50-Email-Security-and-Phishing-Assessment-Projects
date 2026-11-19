# Project 03: Secure SMTP Service Configuration

**Level:** Beginner  
**Track:** Email Security & Phishing Assessment

## Objective
Assess and harden SMTP submission and relay settings in a controlled mail lab.

## Scope and authorization
Use only systems, domains, DNS zones, and mailboxes you own or have written permission to assess. This exercise is restricted to an isolated lab and synthetic data. Do not contact real users or external mail systems unless separately authorized.

## Prerequisites
Local SMTP test server; Kali; openssl; configuration backups; synthetic accounts.

## Lab setup
1. Create a dedicated isolated lab network and record its subnet, hostnames, and owner.
2. Use the fictional namespace `mail.lab.test` and reserved example domains; do not impersonate a real organization.
3. Create synthetic users and test mailboxes. Keep credentials disposable and local.
4. Snapshot the lab and store configuration backups before changing controls.

## Walkthrough
1. Review listener exposure
2. Require authenticated submission
3. Restrict relay destinations
4. Enable TLS
5. Set hostname and banner
6. Test allowed and denied relay cases using synthetic recipients
7. Preserve before/after configs.

## Example commands and tools
```bash
openssl s_client -connect mail.lab.test:587 -starttls smtp
# Use only the lab's documented test account and sink
```

Run commands only against your lab. Adapt hostnames and ports to the documented lab configuration.

## Expected output
- A repeatable baseline or test record tied to the lab asset and timestamp.
- Sanitized evidence showing the relevant protocol, DNS, message, gateway, or policy behavior.
- A clear pass/fail/needs-review result for each test case.

## Findings and risk assessment
Record the observed condition, affected asset, evidence reference, likelihood, impact, and business consequence. Separate confirmed weaknesses from assumptions. Prioritize spoofing, unauthorized relay, weak transport protection, missing authentication alignment, and visibility gaps according to the specific scope.

## Framework mapping
Map applicable observations to NIST CSF 2.0 (Protect/Detect/Respond), CIS Controls v8 (secure configuration, access control, audit logging), and MITRE ATT&CK email/identity techniques only where evidence supports the mapping. Avoid assigning a technique solely because a tool was used.

## Remediation
Apply least-privilege sender authorization, strong authentication, TLS, SPF/DKIM/DMARC alignment, gateway policy, monitoring, and documented exception handling as appropriate. Roll out policy changes in stages and validate legitimate business mail flows.

## Validation criteria
- Re-run the same safe test cases after remediation.
- Confirm expected allowed and blocked outcomes using synthetic identities.
- Verify logs, alert routing, and evidence retention.
- Record residual risk, owner, and retest date.

## Evidence and reporting checklist
- [ ] Written authorization and scope
- [ ] Lab topology and test date
- [ ] Sanitized configuration and test outputs
- [ ] Finding severity, rationale, and affected asset
- [ ] Remediation owner and validation evidence
- [ ] Executive summary and limitations

## Training illustrations
![Project 03 baseline workflow](images/01-baseline.svg)

![Project 03 analysis and findings](images/02-findings.svg)

![Project 03 validation workflow](images/03-validation.svg)

## Deliverables
A concise assessment worksheet, sanitized evidence bundle, prioritized findings, and remediation/retest notes.
