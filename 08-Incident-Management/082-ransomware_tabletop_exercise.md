# Ransomware Tabletop Exercise

**Organisation:** Westbridge Hospitals Trust (WHT)  
**Document Type:** Exercise Record  
**Owner:** Chief Information Security Officer (CISO)  
**Version:** 1.0  



# 1. Purpose

This document records WHT's first ransomware tabletop exercise, run under the testing cadence established in [081-incident_response_plan](081-incident_response_plan.md) §9. It is the exercise already cited as existing evidence in [../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) §4.4 and [../03-Current-State-Assessment/024-dsp_toolkit_review](../03-Current-State-Assessment/024-dsp_toolkit_review.md) §4.5.



# 2. Scope

The exercise tested the Trust's response to a simulated ransomware incident affecting clinical systems, directly rehearsing the scenario underlying the Trust's highest-scored risk, CR-001 ([../04-Risk-Management/049-risk_register](../04-Risk-Management/049-risk_register.md) §5). It exercised detection, containment, internal escalation, and communication — it did not include a live technical failover to backup systems, which is scoped separately under [../10-Business-Continuity/](../10-Business-Continuity/).



# 3. Exercise Scenario

A simulated phishing email leads to credential compromise and lateral movement, culminating in ransomware encryption affecting a subset of clinical systems including the Electronic Patient Record (EPR). The scenario was designed to mirror CR-001's recorded threat and vulnerability profile: cyber criminals exploiting phishing, privilege escalation, and insufficient network segmentation.



# 4. Participants

| Role | Function in Exercise |
|---|---|
| Chief Information Security Officer (CISO) | Exercise lead; acted as Incident Commander |
| Cyber Security Team | Simulated detection, containment, and eradication actions |
| Chief Digital Information Officer (CDIO) | Represented risk ownership of CR-001; clinical system recovery prioritisation |
| Clinical Safety Officer | Assessed simulated patient safety implications |
| Data Protection Officer (DPO) | Assessed simulated ICO notification trigger |
| Service Desk | Simulated initial incident reporting intake |

Participants were drawn from the roles defined in [../01-Discovery/006-stakeholders](../01-Discovery/006-stakeholders.md) and [../05-Governance/052-roles_and_responsibilities](../05-Governance/052-roles_and_responsibilities.md).



# 5. Exercise Timeline

| Inject | Simulated Event | Expected Action |
|---|---|---|
| 1 | Phishing email reported by staff member | Service Desk logs and escalates to Cyber Security Team |
| 2 | Endpoint detection alert (simulated) | Cyber Security Team investigates, confirms compromise |
| 3 | Lateral movement and ransomware encryption on EPR-adjacent systems | Incident classified Critical; SIRO and CDIO notified |
| 4 | Simulated patient safety impact from EPR unavailability | Clinical Safety Officer engaged; business continuity considered |
| 5 | Simulated personal data exposure | DPO assesses ICO 72-hour notification trigger |



# 6. Observations

## What Worked

- The reporting path from Service Desk to the Cyber Security Team was clear and well understood by participants.
- Incident classification against the Critical/High/Medium/Low scale in [081-incident_response_plan](081-incident_response_plan.md) §3 was applied consistently and without disagreement.
- Participants correctly identified that ransom payment was not an option under the plan (§8).

## What Did Not Work

- Detection of the initial lateral movement relied on manual investigation rather than automated correlation, consistent with the current CAF C1/C2 Not Achieved position ([../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) §3) — the exercise did not demonstrate detection capability beyond what the Trust already has, since none exists to test yet.
- The handoff between the Cyber Security Team and Clinical Safety Officer for patient safety assessment was not clearly timed in the plan at the point of the exercise — participants had to improvise the point at which clinical safety was engaged.
- CSGG escalation was simulated as a notification but the exercise did not test an out-of-cycle CSGG convening, since the group's first meeting had not yet occurred at the time of the exercise.



# 7. Findings Mapped to Risk IDs

| Finding | Linked Risk / Reference |
|---|---|
| Detection relies on manual reporting, not automated correlation | CR-009 (Insufficient security monitoring); CAF C1/C2 |
| Clinical safety engagement point not clearly timed in the plan | CR-001; patient safety impact category |
| CSGG out-of-cycle convening process untested | CR-001; [../05-Governance/051-security_strategy](../05-Governance/051-security_strategy.md) §4 |



# 8. Actions Arising

Actions from this exercise are tracked in full, with owners and target dates, in [083-lessons_learned_report](083-lessons_learned_report.md) §4.



# 9. Review and Maintenance

This exercise establishes the first cycle of the annual testing cadence set out in [081-incident_response_plan](081-incident_response_plan.md) §9. The next exercise is due within 12 months of this record's date, or sooner if a real Critical-severity incident occurs and supersedes the need for a simulated one that cycle.
