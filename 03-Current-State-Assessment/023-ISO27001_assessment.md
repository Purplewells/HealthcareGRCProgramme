# ISO/IEC 27001 Assessment

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** ISO/IEC 27001:2022 Conformance Assessment
**Owner:** Chief Information Security Officer (CISO)
**Version:** 1.0

## 1. Introduction

### 1.1 Purpose

This assessment measures WHT's current conformance with ISO/IEC 27001:2022, at the Annex A control-theme level, as part of the Trust's aspiration to work towards a certifiable Information Security Management System (ISMS). It builds on [021-current_state_assessment](021-current_state_assessment.md) and complements the NCSC CAF assessment ([022-caf_assessment](022-caf_assessment.md)), which assesses the same underlying capability against a UK critical-national-infrastructure-oriented framework rather than a certifiable management-system standard.

### 1.2 Scope

This assessment covers the four Annex A control themes of ISO/IEC 27001:2022 — Organizational, People, Physical, and Technological controls — applied Trust-wide across the clinical, corporate, infrastructure, medical device, and third-party estate recorded in [../02-Asset-Management/022-master_assets_register.xlsx](../02-Asset-Management/022-master_assets_register.xlsx). It assesses conformance at the level of control themes and representative controls, not a full 93-control audit; the detailed control-by-control mapping and evidence is maintained separately in [../07-Compliance/072-iso27001_control_mapping.xlsx](../07-Compliance/072-iso27001_control_mapping.xlsx). This assessment also excludes the management-system clauses (Clauses 4-10, e.g. management review, internal audit programme, ISMS scope statement), which are not yet formally established and are out of scope until the Trust commits to a certification timeline.

## 2. Assessment Criteria

### 2.1 Framework(s) Applied

ISO/IEC 27001:2022 Annex A, comprising 93 controls across four themes: Organizational (37 controls), People (8 controls), Physical (14 controls), and Technological (34 controls).

### 2.2 Rating Scale

| Rating | Description |
|---|---|
| Not Implemented | No meaningful control activity in place |
| Partially Implemented | Control activity exists but is inconsistent, undocumented, or unowned |
| Largely Implemented | Control is documented and applied in most areas, with some gaps |
| Fully Implemented | Control is documented, consistently applied, owned, and evidenced across the Trust |

## 3. Current State

WHT's conformance is strongest in Physical controls, reflecting the Trust's existing estate and facilities management practices for its hospital sites and data centres, though this has not been subject to a dedicated review in this engagement and is assessed on the absence of contrary evidence rather than direct testing. Organizational and Technological controls are Partially Implemented, mirroring the governance fragmentation and technical control gaps identified in [021-current_state_assessment](021-current_state_assessment.md) and [022-caf_assessment](022-caf_assessment.md). People controls are Partially Implemented, with the clearest gap being security awareness training completion.

| Theme | Control Count | Assessed Conformance | Representative Gap |
|---|---:|---|---|
| Organizational (A.5) | 37 | Partially Implemented | Supplier relationship security (A.5.19-A.5.23), incident management policy consistency |
| People (A.6) | 8 | Partially Implemented | Security awareness and training (A.6.3) |
| Physical (A.7) | 14 | Largely Implemented | Not independently tested in this engagement |
| Technological (A.8) | 34 | Partially Implemented | Access rights management (A.8.2-A.8.5), backup (A.8.13), monitoring (A.8.15-A.8.16), legacy device patching (A.8.8) |

## 4. Observations

### 4.1 Organizational Controls are Partially Implemented

Information security policies exist (A.5.1) but are not consistently applied across departments, and supplier relationship security controls (A.5.19-A.5.23) are the weakest area within this theme, with no central supplier security assessment process despite more than 150 active suppliers. (Ref: [021-current_state_assessment](021-current_state_assessment.md) §4.1, §4.5)

### 4.2 People Controls are Partially Implemented

Screening and terms-of-employment controls are assumed to follow standard NHS HR process, but security awareness and training (A.6.3) is a documented gap, with low training completion rates recorded against risk CR-008. (Ref: [../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md) CR-008)

### 4.3 Physical Controls are Assessed as Largely Implemented, Pending Direct Verification

No evidence gathered during this engagement identifies weaknesses in physical security of hospital sites or data centres. This rating should be treated as provisional until a dedicated physical security review is scoped, since it is currently based on absence of negative evidence rather than direct testing.

### 4.4 Technological Controls are Partially Implemented

Access control (A.8.2-A.8.5), backup (A.8.13), security monitoring and logging (A.8.15-A.8.16), and vulnerability/patch management for legacy medical devices (A.8.8) are all documented gaps, consistent with findings already recorded in the Cyber Risk Register and the medical device register. (Ref: [../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md) CR-003, CR-004, CR-009, CR-011; [../02-Asset-Management/024-medical_device_register.xlsx](../02-Asset-Management/024-medical_device_register.xlsx))

## 5. Evidence

| Evidence ID | Description | Source | Date | Linked Observation |
|---|---|---|---|---|
| EVD-001 | Supplier Register with no central assurance process across 11 sampled suppliers | [../02-Asset-Management/025-supplier_register.xlsx](../02-Asset-Management/025-supplier_register.xlsx) | 2026-07-23 | 4.1 |
| EVD-002 | CR-008 Security awareness failure, scored 16 (High) | [../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md) CR-008 | 2026-07-23 | 4.2 |
| EVD-003 | Medical Device Register — 2 of 11 sampled devices flagged unsupported | [../02-Asset-Management/024-medical_device_register.xlsx](../02-Asset-Management/024-medical_device_register.xlsx) | 2026-07-23 | 4.4 |
| EVD-004 | CR-004, CR-009, CR-011 — access, monitoring, and backup risks all High or Critical | [../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md) | 2026-07-23 | 4.4 |
| EVD-005 | Detailed control-by-control mapping (working papers) | [../07-Compliance/072-iso27001_control_mapping.xlsx](../07-Compliance/072-iso27001_control_mapping.xlsx) | 2026-07-23 | 4.1-4.4 |

## 6. Analysis

### 6.1 Findings

The theme-level conformance position mirrors the CAF assessment closely, which is expected since both frameworks are measuring the same underlying control environment through different lenses: ISO 27001 is control- and management-system-oriented, while CAF is outcome-oriented. The convergence of both assessments on the same weak areas — supplier assurance, access control, monitoring, and legacy device patching — increases confidence that these are genuine, high-priority gaps rather than framework-specific artefacts.

### 6.2 Root Cause

As with the CAF assessment, the root cause is that security control implementation has not kept pace with the growth of the digital and supplier estate. A specific ISO 27001-relevant nuance is the absence of a formally scoped Information Security Management System (Clauses 4-10): without a defined ISMS scope, management review cycle, and internal audit programme, individual controls are being implemented in isolation rather than as part of a coordinated, continuously improving system — which is the structural reason several controls sit at "Partially Implemented" rather than "Fully Implemented" despite some good underlying practice.

## 7. Risk Rating

| Risk ID | Description | Likelihood | Impact | Rating | Linked Observation |
|---|---|---|---|---|---|
| CR-006 | Third-party supplier compromise | 4 | 5 | Critical | 4.1 |
| CR-003 | Unsupported medical devices exploited | 4 | 5 | Critical | 4.4 |
| CR-004 | Excessive user access privileges | 4 | 4 | High | 4.4 |
| CR-008 | Security awareness failure | 4 | 4 | High | 4.2 |
| CR-009 | Insufficient security monitoring | 3 | 5 | High | 4.4 |
| CR-011 | Data loss due to inadequate backup protection | 3 | 5 | High | 4.4 |

## 8. Recommendations

| Recommendation ID | Recommendation | Priority | Owner | Target Timeframe |
|---|---|---|---|---|
| REC-001 | Formally scope an Information Security Management System (Clause 4) with a defined management review cycle (Clause 9.3), as the structural fix for controls stalling at "Partially Implemented" | High | CISO | Q1 2027 |
| REC-002 | Implement supplier relationship security controls (A.5.19-A.5.23) via a supplier assurance process | High | Procurement Director | Q4 2026 |
| REC-003 | Implement access rights management controls (A.8.2-A.8.5) via role-based access and periodic review | High | IAM Manager | Q1 2027 |
| REC-004 | Implement logging and monitoring controls (A.8.15-A.8.16), building on the existing Security Monitoring Platform and MSSP relationship | High | CISO / SOC Manager | Q1 2027 |
| REC-005 | Scope a dedicated physical security review to convert the provisional A.7 rating into a verified position | Medium | Infrastructure Manager | Q2 2027 |
| REC-006 | Establish a tracked security awareness and training programme with completion reporting (A.6.3) | Medium | Security Awareness Lead | Q1 2027 |

## 9. Conclusion

WHT's ISO/IEC 27001:2022 conformance position is Partially Implemented across three of four Annex A themes, with Physical controls provisionally rated Largely Implemented pending direct verification. The strong overlap with the CAF assessment findings in [022-caf_assessment](022-caf_assessment.md) — particularly around supplier assurance, access control, and monitoring — indicates these are genuine cross-framework priorities rather than assessment artefacts, and should be treated as shared inputs to the single improvement roadmap in [../14-RoadMap/](../14-RoadMap/) rather than addressed as separate ISO and CAF workstreams. Establishing a formally scoped ISMS is the key structural recommendation that would allow future control improvements to compound rather than remain isolated.
