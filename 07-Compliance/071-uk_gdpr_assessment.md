# UK GDPR Assessment

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** UK GDPR Compliance Assessment
**Owner:** Data Protection Officer (DPO)
**Version:** 1.0

## 1. Introduction

### 1.1 Purpose

This assessment evaluates WHT's compliance posture against the UK General Data Protection Regulation (UK GDPR) and the Data Protection Act 2018. It draws together data protection evidence already produced elsewhere in the programme — the data classification framework ([../06-Information-Governance/061-data_classification](../06-Information-Governance/061-data_classification.md)), the DPIA for the Patient Portal and Healthcare Interoperability Platform ([../06-Information-Governance/062-data_protection_impact_assessment](../06-Information-Governance/062-data_protection_impact_assessment.md)), the data lineage assessment ([../06-Information-Governance/063-data_lineage_assessment](../06-Information-Governance/063-data_lineage_assessment.md)), and the records retention schedule ([../06-Information-Governance/064-records_retention_schedule](../06-Information-Governance/064-records_retention_schedule.md)) — into a single UK GDPR-specific compliance position, consistent with the regulatory obligations set out in [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §2.3.

### 1.2 Scope

This assessment covers the Trust's processing of personal and special category data across clinical and corporate systems, evaluated against the UK GDPR's core principles (Article 5), lawful basis requirements (Article 6/9), and accountability obligations (Article 5(2), Article 30). It does not repeat the platform-specific DPIA findings already documented in `062-data_protection_impact_assessment.md` in full — it references them and assesses whether the wider information governance foundation (classification, lineage, retention) is sufficient to support UK GDPR compliance Trust-wide, not just for the one platform already assessed in detail.

## 2. Assessment Criteria

### 2.1 Framework(s) Applied

UK General Data Protection Regulation (retained EU law as amended) and the Data Protection Act 2018, assessed against the Article 5 data protection principles: lawfulness, fairness and transparency; purpose limitation; data minimisation; accuracy; storage limitation; integrity and confidentiality; and accountability.

### 2.2 Rating Scale

| Rating | Description |
|---|---|
| Not Compliant | No meaningful evidence of the principle or obligation being met |
| Partially Compliant | Evidence exists but is inconsistent, undocumented, or not applied Trust-wide |
| Compliant | Consistently applied, owned, and evidenced across the Trust |

## 3. Current State

WHT has recently established the core information governance building blocks a UK GDPR compliance position depends on: a data classification framework (`061`), a completed DPIA for its highest-risk patient-facing platform (`062`), a data lineage assessment tracing personal data across the clinical estate (`063`), and a records retention schedule (`064`). This mirrors the pattern seen across the CAF ([022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md)) and ISO 27001 ([023-ISO27001_assessment](../03-Current-State-Assessment/023-ISO27001_assessment.md)) assessments: the documentation and structural foundations exist, but consistent, board-reviewed application across the whole Trust — rather than the one platform already assessed in depth — has not yet been demonstrated.

The Trust Board's risk appetite statement ([../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §2.4) sets a **Low appetite** for non-compliance with UK GDPR, reflecting the Trust's public accountability, which frames every gap identified below as a priority rather than a tolerable residual risk.

## 4. Observations

### 4.1 Lawful Basis is Documented for the Assessed Platform, Not Yet Trust-Wide

The DPIA establishes lawful basis (public task, legal obligation, public interest) for Patient Portal processing activities ([../06-Information-Governance/062-data_protection_impact_assessment](../06-Information-Governance/062-data_protection_impact_assessment.md) §8), but no equivalent lawful basis register exists for other clinical systems (LIS, RIS/PACS, Pharmacy Management System, Theatre Management System) processing the same categories of special category data.

### 4.2 Data Minimisation and Storage Limitation Now Have a Documented Basis, Pending Trust-Wide Application

The records retention schedule ([../06-Information-Governance/064-records_retention_schedule](../06-Information-Governance/064-records_retention_schedule.md)) establishes retention periods aligned to the UK GDPR storage limitation principle for the first time in the programme, but as a newly-created document its application across existing records (rather than only new records going forward) has not yet been evidenced.

### 4.3 Accountability (Article 5(2)) is Strengthened by the Data Lineage Assessment but Depends on Its Ongoing Maintenance

The data lineage assessment ([../06-Information-Governance/063-data_lineage_assessment](../06-Information-Governance/063-data_lineage_assessment.md)) demonstrates, for the first time, an explicit system-of-record register for personal data. Its own risk DL-003 notes this lineage map is not yet reconciled with the master asset register on a routine cycle — meaning the accountability evidence it provides will decay unless that reconciliation is established.

### 4.4 Uncontrolled Copies of Patient Data Remain an Open Integrity and Confidentiality Gap

An internal audit identified inconsistent data classification and uncontrolled copies of patient reports stored outside approved systems ([../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.6), a direct Article 5(1)(f) (integrity and confidentiality) concern that predates and is not yet resolved by the classification framework in `061`.

### 4.5 Excessive Access Privileges Undermine the Data Minimisation Principle in Practice

CR-004 (Excessive user access privileges), already rated High across the CAF, ISO 27001, and DSPT assessments, has a direct UK GDPR dimension: access broader than necessary for a user's role is inconsistent with data minimisation applied to access, not just to collection. (Ref: [../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md) CR-004)

## 5. Evidence

| Evidence ID | Description | Source | Date | Linked Observation |
|---|---|---|---|---|
| EVD-001 | DPIA establishing lawful basis for Patient Portal processing | [../06-Information-Governance/062-data_protection_impact_assessment](../06-Information-Governance/062-data_protection_impact_assessment.md) §8 | 2026-07-23 | 4.1 |
| EVD-002 | Records Retention Schedule | [../06-Information-Governance/064-records_retention_schedule](../06-Information-Governance/064-records_retention_schedule.md) | 2026-07-23 | 4.2 |
| EVD-003 | Data Lineage Assessment, including open risk DL-003 | [../06-Information-Governance/063-data_lineage_assessment](../06-Information-Governance/063-data_lineage_assessment.md) §7 | 2026-07-23 | 4.3 |
| EVD-004 | Internal audit findings on uncontrolled copies of patient reports | [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.6 | 2026-07-23 | 4.4 |
| EVD-005 | CR-004 Excessive user access privileges, scored 16 (High) | [../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md) CR-004 | 2026-07-23 | 4.5 |

## 6. Analysis

### 6.1 Findings

WHT's UK GDPR position has materially strengthened through this programme — the Trust now has, for the first time, a classification framework, a completed DPIA for its highest-risk platform, a lineage assessment, and a retention schedule. The consistent pattern across all five observations, however, is that these foundations were built for or are proven on one platform (the Patient Portal) or as newly-created documents, and have not yet been demonstrated as applied consistently across the whole clinical and corporate estate. This is the same "documentation exists, operating rhythm doesn't yet" pattern identified in every other framework assessment in this programme.

### 6.2 Root Cause

The root cause is the same one identified Trust-wide in [021-current_state_assessment](../03-Current-State-Assessment/021-current_state_assessment.md) §6.2: cyber and information governance capability was not resourced or scaled alongside the pace of digital transformation. The Cyber Security Governance Group chartered in [../05-Governance/051-security_strategy](../05-Governance/051-security_strategy.md) §4 is the forum through which Trust-wide, rather than single-platform, UK GDPR compliance evidence should now be driven and reviewed.

## 7. Risk Rating

| Risk ID | Description | Likelihood | Impact | Rating | Linked Observation |
|---|---|---|---|---|---|
| GDPR-001 | Lawful basis not formally documented for clinical systems outside the assessed Patient Portal | 3 | 4 | High | 4.1 |
| DPIA-005 | Patient information stored outside approved systems | 3 | 4 | High | 4.4 |
| CR-004 | Excessive user access privileges | 4 | 4 | High | 4.5 |

## 8. Recommendations

| Recommendation ID | Recommendation | Priority | Owner | Target Timeframe |
|---|---|---|---|---|
| REC-001 | Extend lawful basis documentation from the Patient Portal DPIA to the Trust's other core clinical systems (LIS, RIS/PACS, Pharmacy Management System, Theatre Management System) | High | DPO | Q4 2026 |
| REC-002 | Establish a routine reconciliation cycle between the data lineage assessment and the master asset register, closing DL-003 | Medium | DPO | Q1 2027 |
| REC-003 | Remediate uncontrolled copies of patient reports identified in the internal audit, applying the classification and retention frameworks now in place | High | DPO | Q4 2026 |
| REC-004 | Report UK GDPR compliance evidence (lawful basis coverage, retention application, access review completion) to the Cyber Security Governance Group as a standing agenda item | Medium | DPO | Q3 2026 |

## 9. Conclusion

WHT's UK GDPR compliance position has a materially stronger evidence base than it did before this programme, but that evidence base is still concentrated on a single platform and a set of newly-created documents rather than demonstrated Trust-wide. Given the Trust Board's Low risk appetite for non-compliance, the priority is extending the lawful basis, classification, lineage, and retention work already completed for the Patient Portal to the rest of the clinical estate, and routing that evidence through the Cyber Security Governance Group so it is reviewed on the same standing cycle as the Trust's other compliance obligations.
