# Project 36: Evilginx Lab Deployment for Defensive Telemetry

**Level:** Advanced  
**Track:** Email Security & Phishing Assessment

## Objective
Build a safe defensive telemetry lab that represents reverse-proxy phishing indicators without deploying an interception proxy.

## Scope and authorization
This project is defensive and lab-only. Use synthetic identities, fabricated events, and explicitly authorized test tenants. Evilginx content is limited to threat modeling, telemetry, detection, and mitigation. Do not deploy interception infrastructure, harvest credentials or session tokens, bypass MFA, or target real users or services.

## Prerequisites
Isolated identity test tenant; synthetic events; SIEM; architecture diagram.

## Lab setup
1. Establish a dedicated lab tenant or offline dataset and document authorization.
2. Use synthetic identities and fabricated indicators only.
3. Ensure no test traffic is routed to public targets.
4. Snapshot configurations and preserve sanitized baseline logs.

## Walkthrough
1. Create a mock event generator or import sanitized sample logs
2. Map reverse-proxy indicators to identity events
3. Build dashboards and alerts
4. Validate incident escalation
5. Document that no proxy, credential capture, or session-token handling is performed.

## Example commands and tools
```bash
# Use synthetic event fixtures only
python3 -c "print('Generate mock identity-risk events; no live proxy or token capture')"
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
![Project 36 baseline workflow](images/01-baseline.svg)

![Project 36 analysis and findings](images/02-findings.svg)

![Project 36 validation workflow](images/03-validation.svg)

## Deliverables
A defensive threat model, detection rules or test cases, prioritized control recommendations, and retest evidence.
