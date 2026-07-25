# NHS Data Security and Protection Toolkit (DSPT) Review

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** NHS DSPT Readiness Review
**Owner:** Chief Information Security Officer (CISO)
**Version:** 1.0

## 1. Introduction

### 1.1 Purpose

This review assesses WHT's readiness against the NHS Data Security and Protection Toolkit (DSPT), the annual self-assessment through which NHS organisations evidence compliance with the National Data Guardian's 10 Data Security Standards. It answers the question: *if the Trust submitted its DSPT today, what outcome would it achieve, and what stands in the way of "Standards Met"?* It draws on the same evidence base as [021-current_state_assessment](021-current_state_assessment.md), [022-caf_assessment](022-caf_assessment.md), and [023-ISO27001_assessment](023-ISO27001_assessment.md), since the current DSPT incorporates CAF-aligned assertions.

### 1.2 Scope

This review covers all 10 National Data Guardian Data Security Standards as expressed in the current DSPT assertion set, applied Trust-wide. It does not constitute a formal DSPT submission — it is a readiness review intended to inform submission preparation and identify evidence gaps ahead of the annual deadline. The detailed control-by-control mapping is maintained in [../07-Compliance/074-nhs_dsp_toolkit_mapping.xlsx](../07-Compliance/074-nhs_dsp_toolkit_mapping.xlsx).

## 2. Assessment Criteria

### 2.1 Framework(s) Applied

NHS Data Security and Protection Toolkit, structured around the National Data Guardian's 10 Data Security Standards.

### 2.2 Rating Scale

Per-standard rating:

| Rating | Description |
|---|---|
| Not Met | Mandatory evidence items for the standard are not satisfied |
| Partially Met | Some mandatory evidence items are satisfied; others require further work |
| Met | All mandatory evidence items for the standard are satisfied |

Overall submission outcome (DSPT publishes one of three outcomes per organisation per year):

| Outcome | Description |
|---|---|
| Standards Met | All mandatory assertions evidenced |
| Standards Not Met (Plan Agreed) | Gaps exist but an improvement plan has been agreed |
| Standards Not Met | Gaps exist with no agreed improvement plan |

## 3. Current State

Based on the evidence gathered across this engagement, WHT would currently achieve a **Standards Not Met** outcome if it submitted its DSPT today, with the most material gaps in Standard 8 (Unsupported Systems), Standard 10 (Accountable Suppliers), Standard 4 (Managing Data Access), and Standard 3 (Training). This is a direct, material consequence flagged in [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §2.3: a "Standards Not Met" outcome can restrict the Trust's access to shared national systems such as the NHS Spine and shared care record services.

| Standard | Description | Assessed Status |
|---|---|---|
| 1 | Personal Confidential Data | Partially Met |
| 2 | Staff Responsibilities | Partially Met |
| 3 | Training | Not Met |
| 4 | Managing Data Access | Not Met |
| 5 | Process Reviews | Partially Met |
| 6 | Responding to Incidents | Partially Met |
| 7 | Continuity Planning | Partially Met |
| 8 | Unsupported Systems | Not Met |
| 9 | IT Protection | Partially Met |
| 10 | Accountable Suppliers | Not Met |

## 4. Observations

### 4.1 Standard 8 (Unsupported Systems) is Not Met

25 medical devices are recorded as running unsupported operating systems with limited vendor patching options, which is a direct, named evidence item under Standard 8. (Ref: [../02-Asset-Management/024-medical_device_register.xlsx](../02-Asset-Management/024-medical_device_register.xlsx); [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.4)

### 4.2 Standard 10 (Accountable Suppliers) is Not Met

The Trust has no central process for assessing supplier security posture, embedding security requirements into contracts, or monitoring ongoing supplier risk across its 150+ suppliers. (Ref: [../02-Asset-Management/025-supplier_register.xlsx](../02-Asset-Management/025-supplier_register.xlsx); [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.5)

### 4.3 Standard 4 (Managing Data Access) is Not Met

Excessive user access privileges, inadequate access reviews, and weak segregation of duties were identified in an internal review, and remain an open, High-rated risk. (Ref: [../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md) CR-004; [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.3)

### 4.4 Standard 3 (Training) is Not Met

Security awareness training completion is low, with no evidenced Trust-wide tracking or reporting of completion rates to a governance forum. (Ref: [../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md) CR-008)

### 4.5 Standards 1, 2, 5, 6, 7, and 9 are Partially Met

Personal Confidential Data handling (Standard 1) is undermined by inconsistent data classification and uncontrolled copies of patient reports (Standard 1); process review (Standard 5) and IT protection (Standard 9) benefit from a newly established risk register and asset register but lack a full review cadence; incident response (Standard 6) and continuity planning (Standard 7) have documented plans ([../08-Incident-Management/](../08-Incident-Management/), [../10-Business-Continuity/](../10-Business-Continuity/)) but inconsistent testing evidence. (Ref: [021-current_state_assessment](021-current_state_assessment.md) §4.7)

## 5. Evidence

| Evidence ID | Description | Source | Date | Linked Observation |
|---|---|---|---|---|
| EVD-001 | Medical Device Register — unsupported OS devices | [../02-Asset-Management/024-medical_device_register.xlsx](../02-Asset-Management/024-medical_device_register.xlsx) | 2026-07-23 | 4.1 |
| EVD-002 | Supplier Register — no central assurance process | [../02-Asset-Management/025-supplier_register.xlsx](../02-Asset-Management/025-supplier_register.xlsx) | 2026-07-23 | 4.2 |
| EVD-003 | CR-004 Excessive user access privileges, scored 16 (High) | [../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md) CR-004 | 2026-07-23 | 4.3 |
| EVD-004 | CR-008 Security awareness failure, scored 16 (High) | [../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md) CR-008 | 2026-07-23 | 4.4 |
| EVD-005 | Incident Response Plan, Business Continuity Plan, Disaster Recovery Plan | [../08-Incident-Management/](../08-Incident-Management/), [../10-Business-Continuity/](../10-Business-Continuity/) | 2026-07-23 | 4.5 |
| EVD-006 | Detailed DSPT evidence mapping (working papers) | [../07-Compliance/074-nhs_dsp_toolkit_mapping.xlsx](../07-Compliance/074-nhs_dsp_toolkit_mapping.xlsx) | 2026-07-23 | 4.1-4.5 |

## 6. Analysis

### 6.1 Findings

The four standards rated Not Met (3, 4, 8, 10) are the same underlying gaps already surfaced independently through the CAF and ISO 27001 assessments — unsupported legacy devices, supplier assurance, access management, and security awareness. This is the third framework in this folder to converge on the same priority list, which should give the Trust Board high confidence that these are the genuine top priorities rather than an artefact of any one assessment methodology.

### 6.2 Root Cause

The DSPT is explicitly evidence-based: it requires named artefacts (asset inventories, supplier contracts with security clauses, training completion records, access review logs) rather than narrative assurance. The Trust's gap is therefore partly a genuine control gap and partly an evidence gap — some activity may exist informally (e.g. ad hoc supplier due diligence) without the structured, retrievable evidence DSPT assertions require. Closing this gap requires both fixing the underlying control and ensuring it produces auditable evidence as a by-product.

## 7. Risk Rating

| Risk ID | Description | Likelihood | Impact | Rating | Linked Observation |
|---|---|---|---|---|---|
| CR-003 | Unsupported medical devices exploited | 4 | 5 | Critical | 4.1 |
| CR-006 | Third-party supplier compromise | 4 | 5 | Critical | 4.2 |
| CR-004 | Excessive user access privileges | 4 | 4 | High | 4.3 |
| CR-008 | Security awareness failure | 4 | 4 | High | 4.4 |

## 8. Recommendations

| Recommendation ID | Recommendation | Priority | Owner | Target Timeframe |
|---|---|---|---|---|
| REC-001 | Produce a vulnerability assessment and remediation/replacement plan for all unsupported medical devices, with evidence retained for DSPT Standard 8 | High | Clinical Engineering Manager | Q4 2026 |
| REC-002 | Establish a supplier security assurance process with retrievable assessment records to evidence DSPT Standard 10 | High | Procurement Director | Q4 2026 |
| REC-003 | Implement a documented, logged access review cycle to evidence DSPT Standard 4 | High | IAM Manager | Q1 2027 |
| REC-004 | Deploy tracked security awareness training with completion reporting to evidence DSPT Standard 3 | High | Security Awareness Lead | Q1 2027 |
| REC-005 | Agree a formal DSPT improvement plan with NHS England / the ICB ahead of this year's submission to secure "Standards Not Met (Plan Agreed)" as an interim position while REC-001 to REC-004 are delivered | High | CISO | Q3 2026 |

## 9. Conclusion

WHT would currently achieve a **Standards Not Met** DSPT outcome, driven primarily by four standards — Training, Managing Data Access, Unsupported Systems, and Accountable Suppliers — that are also the leading gaps identified independently in the CAF and ISO 27001 assessments. Given the timing risk associated with the annual DSPT submission cycle, the immediate priority is agreeing a formal improvement plan with NHS England to secure a "Standards Not Met (Plan Agreed)" position while the underlying recommendations in this document, [022-caf_assessment](022-caf_assessment.md), and [023-ISO27001_assessment](023-ISO27001_assessment.md) are delivered, protecting the Trust's access to shared national systems in the interim.
