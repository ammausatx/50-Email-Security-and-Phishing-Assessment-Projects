# Project 33: User Awareness Metrics and Risk Reporting

**Level:** Intermediate  
**Track:** Email Security & Phishing Assessment

## Objective
Build privacy-conscious awareness metrics that measure program effectiveness.

## Scope and authorization
This project is defensive and lab-only. Use synthetic identities, fabricated events, and explicitly authorized test tenants. Evilginx content is limited to threat modeling, telemetry, detection, and mitigation. Do not deploy interception infrastructure, harvest credentials or session tokens, bypass MFA, or target real users or services.

## Prerequisites
Synthetic campaign export; spreadsheet or Python; privacy policy.

## Lab setup
1. Establish a dedicated lab tenant or offline dataset and document authorization.
2. Use synthetic identities and fabricated indicators only.
3. Ensure no test traffic is routed to public targets.
4. Snapshot configurations and preserve sanitized baseline logs.

## Walkthrough
1. Calculate delivery, report, and training completion rates
2. Avoid ranking individuals
3. Segment by department only when group sizes protect privacy
4. Compare trends
5. Document sampling limitations and improvements.

## Example commands and tools
```bash
python3 - <<'PY'
delivered,reported=100,24
print(f'Report rate: {reported/delivered:.1%}')
PY
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
![Project 33 baseline workflow](images/01-baseline.svg)

![Project 33 analysis and findings](images/02-findings.svg)

![Project 33 validation workflow](images/03-validation.svg)

## Deliverables
A defensive threat model, detection rules or test cases, prioritized control recommendations, and retest evidence.
