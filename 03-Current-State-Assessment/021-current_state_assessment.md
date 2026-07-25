# Current State Assessment

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Current State Assessment (Programme Overview)
**Owner:** Chief Information Security Officer (CISO)
**Version:** 1.0

## 1. Introduction

### 1.1 Purpose

This document answers the question: **how good is the Trust's cyber security today?** It establishes the baseline current state of cyber security governance, risk management, asset management, and compliance across Westbridge Hospitals Trust (WHT), ahead of the detailed framework-specific assessments that follow in this folder: the NCSC Cyber Assessment Framework (CAF) review ([022-caf_assessment](022-caf_assessment.md)), the ISO/IEC 27001 assessment ([023-ISO27001_assessment](023-ISO27001_assessment.md)), and the NHS Data Security and Protection Toolkit (DSPT) review ([024-dsp_toolkit_review](024-dsp_toolkit_review.md)).

It also provides the factual basis consolidated into the overall maturity roll-up in [025-maturity_assessment](025-maturity_assessment.md).

### 1.2 Scope

This assessment covers: security governance and policy; cyber risk management; asset and medical device management; identity and access management (IAM); third-party supplier security; data governance; security monitoring; incident management; and business continuity, as these are the areas identified as business challenges in [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.

It does not cover clinical safety assessment (which follows the Trust's separate clinical governance process) or detailed technical penetration testing — technical testing outcomes, where referenced, are treated as supporting evidence only.

## 2. Assessment Criteria

### 2.1 Framework(s) Applied

This overview assessment does not itself score against a named external framework — it synthesises the Trust's cyber risk register ([../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md)), asset management documentation ([../02-Asset-Management/](../02-Asset-Management/)), and business context ([../01-Discovery/003-business-context](../01-Discovery/003-business-context.md)) into a single current-state picture, using the maturity scale defined below. Framework-specific scoring against NCSC CAF, ISO/IEC 27001:2022, and NHS DSPT is performed in the three assessments that follow this one.

### 2.2 Rating Scale

| Level | Rating | Description |
|---|---|---|
| 1 | Initial | Little to no formal process; activity is ad hoc, reactive, or dependent on individuals |
| 2 | Developing | Basic process exists but is applied inconsistently and lacks central ownership |
| 3 | Established | Process is documented, consistently applied, and has a clear owner |
| 4 | Managed | Process is measured, reviewed, and reported to governance forums on a regular cycle |
| 5 | Optimised | Process is continuously improved using metrics, lessons learned, and benchmarking |

## 3. Current State

WHT has undergone rapid digital transformation over the past five years — expanding cloud adoption, electronic patient records, connected medical devices, and patient-facing digital services (see [../01-Discovery/002-organisation_profile](../01-Discovery/002-organisation_profile.md) §6). Cyber security governance, risk management, and compliance processes have not scaled at the same pace, which is the core driver behind Project SentinelCare.

Governance activity currently exists but is fragmented: security policies are in place but not consistently maintained or applied across departments, and there is limited evidence of control effectiveness reporting to a central governance forum. Risk management has recently been formalised through the central Cyber Risk Register ([../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md)), which records 12 active risks (CR-001 to CR-012), 8 of which are rated High or Critical — but risk ownership is still maturing and treatment plans are largely in the Planned stage rather than embedded business-as-usual activity.

Asset management has matured considerably following the completion of the master asset register ([../02-Asset-Management/022-master_assets_register.xlsx](../02-Asset-Management/022-master_assets_register.xlsx)), which records 35 assets across eight categories with assigned owners and criticality ratings. However, this maturity has surfaced specific weaknesses: 25 medical devices were identified as running unsupported operating systems (2 of 11 sampled devices in [../02-Asset-Management/024-medical_device_register.xlsx](../02-Asset-Management/024-medical_device_register.xlsx) are flagged "Unsupported - Risk Accepted"), and the Trust depends on more than 150 external suppliers without a central supplier security assessment process.

Identity and access management, data governance, and security monitoring remain the least mature areas: an internal review identified excessive access privileges across some clinical and corporate systems, an internal audit found inconsistent data classification and uncontrolled copies of patient reports, and the Trust has limited security monitoring and metrics capability (addressed further in [../09-Security-Operations/](../09-Security-Operations/) and [../13-Security-Metrics/](../13-Security-Metrics/)).

## 4. Observations

### 4.1 Security Governance is Fragmented

Security policies exist but are applied inconsistently across departments, with no single governance forum currently reviewing control effectiveness across the whole Trust. (Ref: [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.2)

### 4.2 Cyber Risk Management is Newly Centralised but Immature

A central Cyber Risk Register now exists and records 12 risks, 8 of which are High or Critical, but most treatment actions remain "Planned" rather than in progress or embedded. (Ref: [../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md) §4, §6)

### 4.3 Asset Management Has a Strong Foundation

A master asset register covering 35 assets across eight categories, each with an assigned owner and criticality rating, has been established and is the authoritative source for the Trust's digital estate. (Ref: [../02-Asset-Management/022-master_assets_register.xlsx](../02-Asset-Management/022-master_assets_register.xlsx))

### 4.4 Legacy Medical Devices Present Unpatched Risk

25 medical devices are recorded as running unsupported operating systems, with vendor patching options limited for long-lifecycle clinical equipment. (Ref: [../02-Asset-Management/024-medical_device_register.xlsx](../02-Asset-Management/024-medical_device_register.xlsx); [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.4)

### 4.5 Third-Party Supplier Assurance is Not Centrally Managed

The Trust relies on over 150 external suppliers, but has no central process for assessing supplier security posture, embedding security requirements into contracts, or monitoring ongoing supplier risk. (Ref: [../02-Asset-Management/025-supplier_register.xlsx](../02-Asset-Management/025-supplier_register.xlsx); [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.5)

### 4.6 Identity and Access Management Has Excessive Privilege Exposure

An internal review found users retaining unnecessary privileges, inadequate access reviews, and weak segregation of duties across some systems. (Ref: [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.3)

### 4.7 Data Governance Practices are Inconsistent

An internal audit identified inconsistent data classification, excessive access permissions, and uncontrolled copies of patient reports stored outside approved systems. (Ref: [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.6)

### 4.8 Security Monitoring Capability is Limited

The Trust has limited visibility of security events across its estate, constraining its ability to detect and respond to attacks in a timely manner. (Ref: [../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md) CR-009)

## 5. Evidence

| Evidence ID | Description | Source | Date | Linked Observation |
|---|---|---|---|---|
| EVD-001 | Cyber Risk Register recording 12 risks, 8 High/Critical | [../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md) | 2026-07-23 | 4.2 |
| EVD-002 | Master Asset Register recording 35 assets across 8 categories | [../02-Asset-Management/022-master_assets_register.xlsx](../02-Asset-Management/022-master_assets_register.xlsx) | 2026-07-23 | 4.3 |
| EVD-003 | Medical Device Register flagging unsupported devices | [../02-Asset-Management/024-medical_device_register.xlsx](../02-Asset-Management/024-medical_device_register.xlsx) | 2026-07-23 | 4.4 |
| EVD-004 | Supplier Register covering NHS Digital, clinical software, device, and MSSP suppliers | [../02-Asset-Management/025-supplier_register.xlsx](../02-Asset-Management/025-supplier_register.xlsx) | 2026-07-23 | 4.5 |
| EVD-005 | Internal review findings on access privileges and data governance | [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.3, §3.6 | 2026-07-23 | 4.6, 4.7 |

## 6. Analysis

### 6.1 Findings

Across all domains reviewed, a consistent pattern emerges: WHT has the *documentation and structural foundations* for good governance (registers, policies, ownership models) but lacks the *operating rhythm* that turns those foundations into managed, reviewed, continuously improving practice. Asset management is the domain furthest along this maturity curve, precisely because it has recently received focused programme attention — this suggests that the same investment applied to IAM, supplier assurance, and monitoring would yield comparable gains.

The risks with the highest scores in the Cyber Risk Register (ransomware, medical device exploitation, supplier compromise, patient data exposure — all scored 20-25) cluster around exactly the domains flagged as weakest in this assessment (Sections 4.1, 4.4, 4.5, 4.7), confirming that current governance gaps are not abstract — they map directly to the Trust's most severe quantified risks.

### 6.2 Root Cause

The underlying root cause is that cyber security governance did not scale in step with the pace of digital transformation. Individual systems, devices, and supplier relationships were onboarded to meet clinical and operational need, but no single accountable function was resourced to maintain central oversight of the resulting estate, its risks, and its third-party dependencies until the commissioning of Project SentinelCare. This produced consistent secondary effects across domains: incomplete ownership records, inconsistent policy application, and limited central visibility.

## 7. Risk Rating

| Risk ID | Description | Likelihood | Impact | Rating | Linked Observation |
|---|---|---|---|---|---|
| CR-001 | Ransomware affecting clinical services | 5 | 5 | Critical | 4.1, 4.8 |
| CR-003 | Unsupported medical devices exploited | 4 | 5 | Critical | 4.4 |
| CR-005 | Patient data exposure | 4 | 5 | Critical | 4.7 |
| CR-006 | Third-party supplier compromise | 4 | 5 | Critical | 4.5 |
| CR-004 | Excessive user access privileges | 4 | 4 | High | 4.6 |
| CR-009 | Insufficient security monitoring | 3 | 5 | High | 4.8 |

## 8. Recommendations

| Recommendation ID | Recommendation | Priority | Owner | Target Timeframe |
|---|---|---|---|---|
| REC-001 | Establish a Cyber Security Governance Group with a standing mandate to review policy application and control effectiveness Trust-wide | High | CISO | Q3 2026 |
| REC-002 | Move risk treatment actions from "Planned" to "In Progress" for all Critical-rated risks, starting with CR-001, CR-003, CR-005, CR-006 | High | CISO / CDIO | Q3 2026 |
| REC-003 | Complete a full medical device inventory and vulnerability assessment, and produce a replacement/remediation roadmap for unsupported devices | High | Clinical Engineering Manager | Q4 2026 |
| REC-004 | Establish a supplier security assurance process covering onboarding assessment, contractual security requirements, and annual review | High | Procurement Director | Q4 2026 |
| REC-005 | Implement a Trust-wide access review cycle with role-based access control for clinical and corporate systems | Medium | IAM Manager | Q1 2027 |
| REC-006 | Complete data classification and remediate uncontrolled copies of patient reports identified in the internal audit | Medium | Data Protection Officer | Q1 2027 |
| REC-007 | Expand security monitoring coverage and reporting, building on the Managed Security Service Provider relationship | Medium | CISO / SOC Manager | Q1 2027 |

## 9. Conclusion

WHT enters Project SentinelCare with real strengths to build on — most notably a newly established, well-structured asset register and a central cyber risk register — but with governance, identity and access management, supplier assurance, and security monitoring still at an early stage of maturity. The risks this creates are not hypothetical: they are the same risks already rated Critical or High in the Trust's own risk register. The framework-specific assessments that follow (NCSC CAF, ISO/IEC 27001, NHS DSPT) will validate and add granularity to this picture, and the recommendations above form the starting point for the programme's prioritisation, carried forward into [025-maturity_assessment](025-maturity_assessment.md) and the improvement roadmap in [../14-RoadMap/](../14-RoadMap/).
