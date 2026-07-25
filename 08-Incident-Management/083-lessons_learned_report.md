# Lessons Learned Report

**Organisation:** Westbridge Hospitals Trust (WHT)  
**Document Type:** Lessons Learned Report  
**Owner:** Chief Information Security Officer (CISO)  
**Version:** 1.0  



# 1. Purpose

This report closes the "evidenced lessons-learned feedback" gap identified in [../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) §4.4 and formalised as REC-006 ("formalise a testing and lessons-learned cadence for the Incident Response and Business Continuity Plans"). It documents how findings from exercises and real incidents are captured, tracked, and fed back into [081-incident_response_plan](081-incident_response_plan.md) and the wider risk management process.



# 2. Scope

This report covers the lessons-learned process itself, and the specific findings and actions arising from [082-ransomware_tabletop_exercise](082-ransomware_tabletop_exercise.md), the Trust's first formal exercise under this cadence. Future editions of this report will accumulate findings from subsequent exercises and real incidents rather than being replaced each cycle, so that recurring themes can be identified over time.



# 3. Lessons Learned Process

Following every Medium, High, or Critical severity incident or exercise (per [081-incident_response_plan](081-incident_response_plan.md) §6, Post-Incident Review), the Incident Commander convenes a lessons-learned review within two weeks. Findings are:

1. Recorded in this report with a clear description and linked risk/reference.
2. Assigned an owner and target date, tracked in the action tracker (§4).
3. Where a finding indicates a gap in [081-incident_response_plan](081-incident_response_plan.md) itself, the plan is updated at its next review, or immediately for Critical findings.
4. Where a finding relates to an existing risk register entry, it is fed back to the risk owner for consideration at the next risk review, per [../04-Risk-Management/047-risk_methodology](../04-Risk-Management/047-risk_methodology.md).
5. Reported to the Cyber Security Governance Group (CSGG) as a standing agenda item, per [../05-Governance/051-security_strategy](../05-Governance/051-security_strategy.md) §4.2.



# 4. Findings and Action Tracker

Findings from [082-ransomware_tabletop_exercise](082-ransomware_tabletop_exercise.md) §7:

| Finding | Action | Owner | Target Date | Status |
|---|---|---|---|---|
| Detection relies on manual reporting, not automated correlation (CAF C1/C2 Not Achieved) | No new action created — already tracked as [../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) REC-005 (expand SOC/MSSP monitoring coverage) | CISO / SOC Manager | Q1 2027 | Planned |
| Clinical safety engagement point not clearly timed in the incident response plan | Add an explicit trigger point for Clinical Safety Officer engagement to [081-incident_response_plan](081-incident_response_plan.md) §6 (Identify/Contain phases) | CISO | Q4 2026 | Planned |
| CSGG out-of-cycle convening process untested | Test out-of-cycle CSGG convening as part of the next annual exercise, once the CSGG's regular meeting cycle is established | CISO | Next exercise cycle | Planned |

No finding from this first exercise has yet reached Embedded status, consistent with the "documentation exists, operating rhythm doesn't yet" pattern identified across the programme's other assessments ([../03-Current-State-Assessment/025-maturity_assessment](../03-Current-State-Assessment/025-maturity_assessment.md)).



# 5. Recurring Themes

As this is the first exercise recorded under this process, no recurring theme has yet been established across multiple cycles. This section will be populated as subsequent exercises and incidents are added to the tracker in §4, allowing the Trust to distinguish one-off findings from systemic gaps.



# 6. Review and Maintenance

This report is updated after every exercise or Medium/High/Critical incident, and reviewed in full annually by the CISO alongside [081-incident_response_plan](081-incident_response_plan.md) and [082-ransomware_tabletop_exercise](082-ransomware_tabletop_exercise.md). Action tracker status is reported to the CSGG at each of its meetings until all actions from a given cycle reach Embedded status.
