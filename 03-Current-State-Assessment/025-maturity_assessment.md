# Cyber Security Maturity Assessment

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Cyber Security Maturity Roll-Up
**Owner:** Chief Information Security Officer (CISO)
**Version:** 1.0

## 1. Introduction

### 1.1 Purpose

This document consolidates the findings of [021-current_state_assessment](021-current_state_assessment.md), [022-caf_assessment](022-caf_assessment.md), [023-ISO27001_assessment](023-ISO27001_assessment.md), and [024-dsp_toolkit_review](024-dsp_toolkit_review.md) into a single overall maturity position, expressed on the domain-level scale used throughout this folder. It answers the question the Trust Board will ask after reviewing the individual assessments: *what is our overall maturity, and where should investment go first?* It is the primary input to the improvement roadmap in [../14-RoadMap/](../14-RoadMap/).

### 1.2 Scope

This assessment covers the same nine domains assessed in [021-current_state_assessment](021-current_state_assessment.md) — Governance, Risk Management, Asset Management, Medical Device Security, Third-Party/Supplier Assurance, Identity and Access Management, Data Governance, Security Monitoring, and Incident Response & Business Continuity — rolling up the CAF, ISO 27001, and DSPT positions for each rather than introducing new evidence.

## 2. Assessment Criteria

### 2.1 Framework(s) Applied

This is a cross-framework synthesis of NCSC CAF ([022-caf_assessment](022-caf_assessment.md)), ISO/IEC 27001:2022 ([023-ISO27001_assessment](023-ISO27001_assessment.md)), and NHS DSPT ([024-dsp_toolkit_review](024-dsp_toolkit_review.md)), rather than an assessment against a single named external framework.

### 2.2 Rating Scale

The five-level maturity scale defined in [021-current_state_assessment](021-current_state_assessment.md) §2.2 is used: Initial, Developing, Established, Managed, Optimised.

## 3. Current State

Consolidating the three framework-specific assessments produces a consistent picture: no domain has yet reached "Established" in a fully evidenced sense, one domain (Asset Management) is approaching it, and three domains (Third-Party/Supplier Assurance, Identity and Access Management, Security Monitoring) remain at Initial. This is consistent with all three frameworks independently flagging the same four priority gaps: unsupported medical devices, supplier assurance, access management, and security monitoring.

| Domain | Overall Maturity | CAF Reference | ISO 27001 Reference | DSPT Reference |
|---|---|---|---|---|
| Governance | Developing | A1 Partially Achieved | Organizational Partially Implemented | Standard 2 Partially Met |
| Risk Management | Developing | A2 Partially Achieved | Organizational Partially Implemented | Standard 5 Partially Met |
| Asset Management | Established | A3 Partially Achieved | Technological Partially Implemented | Standard 9 Partially Met |
| Medical Device Security | Developing | B4 Partially Achieved | Technological Partially Implemented | Standard 8 Not Met |
| Third-Party / Supplier Assurance | Initial | A4 Not Achieved | Organizational Partially Implemented | Standard 10 Not Met |
| Identity and Access Management | Initial | B2 Not Achieved | Technological Partially Implemented | Standard 4 Not Met |
| Data Governance | Developing | B3 Partially Achieved | Organizational Partially Implemented | Standard 1 Partially Met |
| Security Monitoring | Initial | C1/C2 Not Achieved | Technological Partially Implemented | Standard 9 Partially Met |
| Incident Response & Business Continuity | Developing | D1/D2 Partially Achieved | Organizational Partially Implemented | Standards 6/7 Partially Met |

## 4. Observations

### 4.1 Overall Maturity is "Developing", with No Domain Yet Fully "Established"

The Trust-wide average sits at Developing (level 2 of 5). Asset Management is the closest to Established, reflecting recent focused investment; every other domain is at Developing or Initial.

### 4.2 Three Domains Remain at "Initial" Maturity

Third-Party/Supplier Assurance, Identity and Access Management, and Security Monitoring are rated Initial across all three frameworks consistently, making them the clearest, most defensible investment priorities.

### 4.3 Cross-Framework Convergence Increases Confidence in Priorities

CAF, ISO 27001, and DSPT — three independently structured frameworks — all identify the same four leading gaps (medical devices, suppliers, access, monitoring), which is strong evidence these are genuine priorities rather than artefacts of a single assessment method. (Ref: [022-caf_assessment](022-caf_assessment.md) §6.1, [023-ISO27001_assessment](023-ISO27001_assessment.md) §6.1, [024-dsp_toolkit_review](024-dsp_toolkit_review.md) §6.1)

### 4.4 Asset Management Demonstrates What Focused Investment Achieves

Asset Management improved from an undocumented state to a structured, owned register within this engagement, and is now the Trust's most mature domain. This is the clearest evidence that the same focused approach, applied to the three Initial-rated domains, would produce comparable improvement.

## 5. Evidence

| Evidence ID | Description | Source | Date | Linked Observation |
|---|---|---|---|---|
| EVD-001 | CAF principle-level achievement table | [022-caf_assessment](022-caf_assessment.md) §3 | 2026-07-23 | 4.1, 4.2 |
| EVD-002 | ISO 27001 theme-level conformance table | [023-ISO27001_assessment](023-ISO27001_assessment.md) §3 | 2026-07-23 | 4.1, 4.2 |
| EVD-003 | DSPT standard-level status table | [024-dsp_toolkit_review](024-dsp_toolkit_review.md) §3 | 2026-07-23 | 4.1, 4.2 |
| EVD-004 | Master Asset Register and domain-specific extracts | [../02-Asset-Management/](../02-Asset-Management/) | 2026-07-23 | 4.4 |

## 6. Analysis

### 6.1 Findings

The consolidated maturity position confirms the programme's initial hypothesis in [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md): WHT's cyber security capability has not scaled with its digital transformation. However, the picture is not uniformly weak — it is unevenly distributed, with Asset Management as a proof point that targeted investment produces measurable maturity gains within a single programme cycle. This reframes the programme's task from "fix everything" to "replicate the Asset Management approach for the three Initial-rated domains."

### 6.2 Root Cause

The root cause is consistent across all three underlying framework assessments: cyber security governance and specialist capability (supplier assurance, IAM, monitoring) were not resourced centrally as the digital and third-party estate grew, leaving domains dependent on ad hoc, local practice rather than a managed, Trust-wide function. Asset Management's comparatively strong maturity is the exception that proves this rule — it received dedicated programme resource, and the other domains have not yet.

## 7. Risk Rating

| Risk ID | Description | Likelihood | Impact | Rating | Linked Observation |
|---|---|---|---|---|---|
| CR-006 | Third-party supplier compromise | 4 | 5 | Critical | 4.2 |
| CR-003 | Unsupported medical devices exploited | 4 | 5 | Critical | 4.2 |
| CR-004 | Excessive user access privileges | 4 | 4 | High | 4.2 |
| CR-009 | Insufficient security monitoring | 3 | 5 | High | 4.2 |

## 8. Recommendations

| Recommendation ID | Recommendation | Priority | Owner | Target Timeframe |
|---|---|---|---|---|
| REC-001 | Sequence the improvement roadmap to bring Third-Party/Supplier Assurance, IAM, and Security Monitoring to at least "Developing" within the next programme cycle, using the Asset Management workstream as the delivery template | High | CISO | Q4 2026 |
| REC-002 | Set a Trust Board-approved target maturity of "Managed" for all domains within 18 months, with quarterly re-assessment against this document | High | CISO | Q3 2026 (target set), ongoing quarterly review |
| REC-003 | Re-run this maturity roll-up at the next major programme milestone to track movement domain-by-domain | Medium | CISO | Q1 2027 |
| REC-004 | Feed this maturity position directly into the prioritisation logic of the improvement roadmap | High | Programme Lead | Q3 2026 |

## 9. Conclusion

WHT's overall cyber security maturity is assessed at **Developing**, with Asset Management the sole domain approaching Established and three domains — Third-Party/Supplier Assurance, Identity and Access Management, and Security Monitoring — still at Initial. The consistency of this picture across three independently structured frameworks (CAF, ISO 27001, DSPT) gives the Trust Board a defensible, well-evidenced basis for prioritisation. The recommended target is to bring every domain to at least "Managed" within 18 months, using the demonstrated success of the Asset Management workstream as the template, with progress tracked through the improvement roadmap in [../14-RoadMap/](../14-RoadMap/).
