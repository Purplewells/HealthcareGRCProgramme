# NCSC CAF Assessment

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** NCSC Cyber Assessment Framework (CAF) Assessment
**Owner:** Chief Information Security Officer (CISO)
**Version:** 1.0

## 1. Introduction

### 1.1 Purpose

This assessment measures WHT's current cyber security capability against the NCSC Cyber Assessment Framework (CAF) v3.2, as adopted by NHS England for the DSPT's CAF-aligned assertions. It builds on the cross-domain findings in [021-current_state_assessment](021-current_state_assessment.md) and provides the CAF-specific evidence base feeding into the DSPT review ([024-dsp_toolkit_review](024-dsp_toolkit_review.md)) and the overall maturity roll-up ([025-maturity_assessment](025-maturity_assessment.md)).

### 1.2 Scope

This assessment covers all four CAF objectives and their fourteen constituent principles, applied to the Trust's clinical systems, corporate systems, infrastructure, medical devices, and third-party services as recorded in [../02-Asset-Management/022-master_assets_register.xlsx](../02-Asset-Management/022-master_assets_register.xlsx). It does not include a control-by-control Indicator of Good Practice (IGP) walkthrough — that level of detail is maintained in the working papers behind [../07-Compliance/073-ncsc_caf_assessment.xlsx](../07-Compliance/073-ncsc_caf_assessment.xlsx); this document records the principle-level achievement position and the reasoning behind it.

## 2. Assessment Criteria

### 2.1 Framework(s) Applied

NCSC Cyber Assessment Framework (CAF) v3.2, comprising four objectives (A: Managing Security Risk, B: Protecting Against Cyber Attack, C: Detecting Cyber Security Events, D: Minimising the Impact of Cyber Security Incidents) and fourteen principles.

### 2.2 Rating Scale

CAF's standard three-point achievement scale is used for each principle:

| Rating | Description |
|---|---|
| Not Achieved | Few or none of the principle's Indicators of Good Practice (IGPs) are met |
| Partially Achieved | Some IGPs are met, or controls exist but are inconsistently applied, unowned, or unverified |
| Achieved | All IGPs are met, controls are consistently applied, owned, and evidenced |

## 3. Current State

The Trust's CAF position is uneven across the four objectives. Objective A (Managing Security Risk) shows the most progress, reflecting recent investment in asset management and risk registration, though supply chain risk management remains an outlier at Not Achieved. Objective B (Protecting Against Cyber Attack) is the weakest objective overall, with identity and access control, resilience, and staff awareness all falling short. Objective C (Detecting Cyber Security Events) is Not Achieved across both principles, consistent with the limited security monitoring capability identified in [021-current_state_assessment](021-current_state_assessment.md) §4.8. Objective D (Minimising the Impact) benefits from documented incident and continuity plans already in place in [../08-Incident-Management/](../08-Incident-Management/) and [../10-Business-Continuity/](../10-Business-Continuity/), but testing and lessons-learned embedding are not yet consistent.

| Objective | Principle | Achievement |
|---|---|---|
| A – Managing Security Risk | A1 Governance | Partially Achieved |
| A – Managing Security Risk | A2 Risk Management | Partially Achieved |
| A – Managing Security Risk | A3 Asset Management | Partially Achieved |
| A – Managing Security Risk | A4 Supply Chain | Not Achieved |
| B – Protecting Against Cyber Attack | B1 Service Protection Policies and Processes | Partially Achieved |
| B – Protecting Against Cyber Attack | B2 Identity and Access Control | Not Achieved |
| B – Protecting Against Cyber Attack | B3 Data Security | Partially Achieved |
| B – Protecting Against Cyber Attack | B4 System Security | Partially Achieved |
| B – Protecting Against Cyber Attack | B5 Resilient Networks and Systems | Not Achieved |
| B – Protecting Against Cyber Attack | B6 Staff Awareness and Training | Not Achieved |
| C – Detecting Cyber Security Events | C1 Security Monitoring | Not Achieved |
| C – Detecting Cyber Security Events | C2 Proactive Security Event Discovery | Not Achieved |
| D – Minimising the Impact | D1 Response and Recovery Planning | Partially Achieved |
| D – Minimising the Impact | D2 Lessons Learned | Partially Achieved |

## 4. Observations

### 4.1 Objective A – Managing Security Risk is Partially Achieved Overall

Governance, risk management, and asset management each show real foundations (a risk register, an asset register, and defined ownership models) but lack the consistent, board-reviewed operating rhythm CAF expects at "Achieved." Supply chain risk management (A4) is the clear outlier, with no central supplier assurance process despite more than 150 active suppliers. (Ref: [021-current_state_assessment](021-current_state_assessment.md) §4.1–4.3, §4.5)

### 4.2 Objective B – Protecting Against Cyber Attack is the Weakest Objective

Three of six principles (B2, B5, B6) are Not Achieved. Identity and access control weaknesses (excessive privileges, weak segregation of duties), resilience gaps (backup and recovery testing), and low security awareness training completion together represent the largest concentration of unmet CAF principles in the assessment. (Ref: [../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md) CR-004, CR-008, CR-010, CR-011)

### 4.3 Objective C – Detecting Cyber Security Events is Not Achieved

Neither security monitoring nor proactive threat discovery meets CAF expectations. The Trust has a Managed Security Service Provider relationship (asset AST-035) and a Security Monitoring Platform (asset AST-019), but current capability does not yet provide the continuous, correlated visibility CAF requires. (Ref: [../02-Asset-Management/022-master_assets_register.xlsx](../02-Asset-Management/022-master_assets_register.xlsx) AST-019, AST-035; [../09-Security-Operations/094-threat_intelligence](../09-Security-Operations/094-threat_intelligence.md))

### 4.4 Objective D – Minimising the Impact Has a Documented but Unproven Foundation

An Incident Response Plan, Business Continuity Plan, and Disaster Recovery Plan already exist ([../08-Incident-Management/](../08-Incident-Management/), [../10-Business-Continuity/](../10-Business-Continuity/)), and a ransomware tabletop exercise has been run, but consistent testing cadence and evidenced lessons-learned feedback into the plans are not yet demonstrated Trust-wide.

## 5. Evidence

| Evidence ID | Description | Source | Date | Linked Observation |
|---|---|---|---|---|
| EVD-001 | Cyber Risk Register — treatment status predominantly "Planned" | [../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md) §6 | 2026-07-23 | 4.1 |
| EVD-002 | Supplier Register with no documented assurance status for 4 of 11 sampled suppliers | [../02-Asset-Management/025-supplier_register.xlsx](../02-Asset-Management/025-supplier_register.xlsx) | 2026-07-23 | 4.1 |
| EVD-003 | Internal review of access privileges and segregation of duties | [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.3 | 2026-07-23 | 4.2 |
| EVD-004 | CR-009 Insufficient security monitoring, scored 15 (High) | [../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md) CR-009 | 2026-07-23 | 4.3 |
| EVD-005 | Incident Response Plan and Ransomware Tabletop Exercise record | [../08-Incident-Management/081-incident_response_plan](../08-Incident-Management/081-incident_response_plan.md), [../08-Incident-Management/082-ransomware_tabletop_exercise](../08-Incident-Management/082-ransomware_tabletop_exercise.md) | 2026-07-23 | 4.4 |

## 6. Analysis

### 6.1 Findings

The CAF assessment confirms the pattern identified in [021-current_state_assessment](021-current_state_assessment.md): the Trust's strongest objective (A) is strong only in a relative sense — even its best-performing principles sit at Partially Achieved, not Achieved. No principle in this assessment currently meets the full "Achieved" bar. Detection (Objective C) is uniformly Not Achieved, which is a material concern independent of the other objectives' scores, because weak detection capability reduces the Trust's ability to identify whether preventive controls elsewhere (Objective B) have already failed.

### 6.2 Root Cause

The root cause mirrors that identified in the wider current state assessment: governance and monitoring capability were not resourced or scaled alongside the pace of digital transformation. CAF's emphasis on continuous, evidenced, board-reviewed practice — rather than one-off policy or documentation — exposes this most clearly in Objectives B and C, where technical controls may exist but are not yet operated to a managed standard.

## 7. Risk Rating

| Risk ID | Description | Likelihood | Impact | Rating | Linked Observation |
|---|---|---|---|---|---|
| CR-006 | Third-party supplier compromise | 4 | 5 | Critical | 4.1 |
| CR-004 | Excessive user access privileges | 4 | 4 | High | 4.2 |
| CR-010 | Clinical service disruption | 3 | 5 | High | 4.2 |
| CR-011 | Data loss due to inadequate backup protection | 3 | 5 | High | 4.2 |
| CR-009 | Insufficient security monitoring | 3 | 5 | High | 4.3 |
| CR-008 | Security awareness failure | 4 | 4 | High | 4.2 |

## 8. Recommendations

| Recommendation ID | Recommendation | Priority | Owner | Target Timeframe |
|---|---|---|---|---|
| REC-001 | Stand up a supplier security assurance process to close A4, prioritising suppliers with access to Restricted-classified data | High | Procurement Director | Q4 2026 |
| REC-002 | Implement role-based access control and a recurring access review cycle to progress B2 | High | IAM Manager | Q1 2027 |
| REC-003 | Establish a recurring backup and disaster recovery test schedule with recorded outcomes to progress B5 | High | Infrastructure Manager | Q4 2026 |
| REC-004 | Deploy mandatory, tracked security awareness training with completion reporting to the Cyber Security Governance Group to progress B6 | Medium | Security Awareness Lead | Q1 2027 |
| REC-005 | Expand SOC/MSSP monitoring coverage and define security metrics reported monthly to progress C1 and C2 | High | CISO / SOC Manager | Q1 2027 |
| REC-006 | Formalise a testing and lessons-learned cadence for the Incident Response and Business Continuity Plans to progress D1 and D2 | Medium | CISO / Business Continuity Manager | Q2 2027 |

## 9. Conclusion

Against the NCSC CAF, WHT currently sits predominantly at Partially Achieved or Not Achieved across all four objectives, with no principle yet meeting the full "Achieved" standard. The clearest priorities are closing the two Not Achieved principles in Objective C (Detecting Cyber Security Events) and the three in Objective B related to access control, resilience, and awareness, since these represent both the framework's largest gaps and the areas most directly linked to the Trust's highest-scored risks. This position is carried forward into the DSPT review ([024-dsp_toolkit_review](024-dsp_toolkit_review.md)), which maps directly to a subset of these CAF outcomes, and into the overall maturity roll-up in [025-maturity_assessment](025-maturity_assessment.md).
