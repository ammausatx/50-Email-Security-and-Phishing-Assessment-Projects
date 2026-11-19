# Project 31: Email Incident Response Playbook

**Level:** Intermediate  
**Track:** Email Security & Phishing Assessment

## Objective
Create an actionable response workflow for suspected email compromise.

## Scope and authorization
This project is defensive and lab-only. Use synthetic identities, fabricated events, and explicitly authorized test tenants. Evilginx content is limited to threat modeling, telemetry, detection, and mitigation. Do not deploy interception infrastructure, harvest credentials or session tokens, bypass MFA, or target real users or services.

## Prerequisites
IR lab; ticketing sandbox; synthetic message and identity logs; contact tree.

## Lab setup
1. Establish a dedicated lab tenant or offline dataset and document authorization.
2. Use synthetic identities and fabricated indicators only.
3. Ensure no test traffic is routed to public targets.
4. Snapshot configurations and preserve sanitized baseline logs.

## Walkthrough
1. Validate report
2. Preserve original .eml and headers
3. Check sign-in and mailbox audit logs
4. Contain affected synthetic account
5. Remove malicious inbox rules
6. Search for related messages
7. Document recovery and lessons learned.

## Example commands and tools
```bash
# IR checklist: validate, preserve, scope, contain, eradicate, recover, learn
# Use only synthetic accounts and logs
```

## Expected output
- A threat model or defensive detection specification.
- Synthetic test events and repeatable alert results.
- A documented mitigation and validation plan.

## Findings and risk assessment
Describe the threat path, affected identity controls, telemetry confidence, potential business impact, and gaps. Do not treat a single anomalous sign-in as conclusive compromise without corroborating evidence.

## Framework mapping
Consider MITRE ATT&CK phishing and valid-account techniques for threat modeling, NIST CSF 2.0 Protect/Detect/Respond, and CIS Controls v8 access control and audit logging. Map only evidence-supported behaviors.

## Remediation
Prioritize phishing-resistant MFA, conditional access, device trust, risk-based sign-in controls, session protection, least privilege, user reporting, and identity telemetry. Ensure emergency access accounts are protected and monitored.

## Validation criteria
- Test detections with positive and benign synthetic fixtures.
- Verify alerts include actionable context and response ownership.
- Confirm security controls work without disrupting approved access.
- Record residual risk and retest date.

## Evidence and reporting checklist
- [ ] Written authorization and defensive scope
- [ ] Threat model and data-flow diagram
- [ ] Sanitized identity events and detection tests
- [ ] False-positive and coverage analysis
- [ ] Mitigation owner and validation results
- [ ] Explicit confirmation no credentials or tokens were collected

## Training illustrations
![Project 31 baseline workflow](images/01-baseline.svg)

![Project 31 analysis and findings](images/02-findings.svg)

![Project 31 validation workflow](images/03-validation.svg)

## Deliverables
A defensive threat model, detection rules or test cases, prioritized control recommendations, and retest evidence.
