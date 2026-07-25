# Cloud Risk Assessment

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Domain Risk Assessment — Cloud
**Owner:** Cloud Service Owner
**Version:** 1.0

## 1. Introduction

### 1.1 Purpose

This assessment provides a focused, domain-specific view of cyber risk arising from WHT's use of cloud services, expanding on the single register-level entry CR-012 in [risk_register](risk_register.md). It answers: *what could go wrong in the Trust's cloud estate specifically, and how well controlled is it today?*

### 1.2 Scope

This assessment covers the Azure Cloud Environment (AST-017), Microsoft 365 (AST-011), Microsoft Entra ID (AST-029), and the Azure-hosted patient-facing services — Patient Portal (AST-007), Appointment Booking Platform (AST-008), Remote Consultation Platform (AST-009), and Patient Messaging Service (AST-010) — as recorded in [../02-Asset-Management/022-master_assets_register.xlsx](../02-Asset-Management/022-master_assets_register.xlsx) and [../02-Asset-Management/023-application_portfolio.xlsx](../02-Asset-Management/023-application_portfolio.xlsx). It excludes on-premises infrastructure (AST-015, AST-016), which is covered by the Trust's wider infrastructure risk management rather than this cloud-specific assessment.

## 2. Assessment Criteria

### 2.1 Framework(s) Applied

This assessment uses the Trust's standard risk methodology defined in [047-risk_methodology](047-risk_methodology.md) (Likelihood × Impact, 1-5 scale each). It is also informed by the cloud-relevant control themes in the CAF assessment ([../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md), principle B4 System Security) and the Trust's Azure-specific governance work in [../12-Azure-Governance/](../12-Azure-Governance/).

### 2.2 Rating Scale

Likelihood and Impact are each scored 1-5 per [risk_register](risk_register.md) §3; Risk Score = Likelihood × Impact, banded Low (1-4) / Medium (5-9) / High (10-16) / Critical (17-25).

## 3. Current State

WHT's cloud footprint has grown quickly as part of its digital transformation programme (see [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §2.2) and now hosts several Restricted-classified, patient-facing services. Cloud security misconfiguration is already recorded as a High risk (CR-012, scored 15) in the master register, reflecting incomplete governance rather than a specific known incident. Identity is the control plane for the entire cloud estate — Microsoft Entra ID (AST-029) — and its compromise or misconfiguration would have Trust-wide consequences, consistent with the CAF finding that Identity and Access Control (B2) is Not Achieved ([../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) §4.2).

## 4. Observations

### 4.1 Cloud Configuration Governance is Immature

There is no dedicated, recurring configuration review process for the Azure environment distinct from general infrastructure change management, increasing the risk that permissive default configurations persist undetected. (Ref: CR-012 in [risk_register](risk_register.md))

### 4.2 Identity is a Single Point of Failure Across Cloud Services

Microsoft Entra ID (AST-029) underpins authentication for Microsoft 365, the Azure Cloud Environment, and all four patient-facing services. Weak identity governance — already flagged Trust-wide (CR-004, Excessive user access privileges) — has an amplified impact in the cloud estate because it is the single control point for services rated Restricted/High criticality.

### 4.3 Patient-Facing Cloud Services Carry Restricted Data Without a Documented Cloud-Specific Data Protection Control Set

The Patient Portal (AST-007), Remote Consultation Platform (AST-009), and Patient Messaging Service (AST-010) are all rated Restricted, but no cloud-specific data security control set (encryption standards, key management ownership, data residency) is currently documented in this programme.

### 4.4 Backup and Recovery Testing for Cloud Workloads is Not Evidenced

Backup Infrastructure (AST-018) covers Trust workloads generally, but no cloud-specific backup/restore test evidence for Azure-hosted services was identified, consistent with the wider gap recorded in CR-011.

## 5. Evidence

| Evidence ID | Description | Source | Date | Linked Observation |
|---|---|---|---|---|
| EVD-001 | CR-012 Cloud security misconfiguration, scored 15 (High) | [risk_register](risk_register.md) | 2026-07-23 | 4.1 |
| EVD-002 | CAF B2 Identity and Access Control — Not Achieved | [../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) §3 | 2026-07-23 | 4.2 |
| EVD-003 | Application Portfolio — 4 Azure-hosted, Restricted-classified patient-facing services | [../02-Asset-Management/023-application_portfolio.xlsx](../02-Asset-Management/023-application_portfolio.xlsx) | 2026-07-23 | 4.3 |
| EVD-004 | CR-011 Data loss due to inadequate backup protection, scored 15 (High) | [risk_register](risk_register.md) | 2026-07-23 | 4.4 |

## 6. Analysis

### 6.1 Findings

Cloud risk at WHT is not a matter of an absent control set — Azure and Microsoft 365 provide mature native security capability — but of governance not yet being configured to use it consistently. The identity single-point-of-failure observation (4.2) is the most consequential finding, since it means the Trust's weakest CAF/ISO area (access control) sits directly at the centre of its most exposed, patient-facing cloud services.

### 6.2 Root Cause

Cloud services were adopted service-by-service to meet specific clinical or patient-experience needs, without a corresponding Trust-wide cloud security governance function being stood up to define baseline configurations, identity standards, and review cadence across the whole estate — the same root cause identified for the Trust generally in [../03-Current-State-Assessment/021-current_state_assessment](../03-Current-State-Assessment/021-current_state_assessment.md) §6.2, manifesting here in a cloud-specific way.

## 7. Risk Rating

| Risk ID | Description | Likelihood | Impact | Rating | Linked Observation |
|---|---|---|---|---|---|
| CR-012 | Cloud security misconfiguration | 3 | 5 | High | 4.1 |
| CR-002 | Compromise of Microsoft 365 accounts | 4 | 5 | Critical | 4.2 |
| CR-004 | Excessive user access privileges | 4 | 4 | High | 4.2 |
| CR-011 | Data loss due to inadequate backup protection | 3 | 5 | High | 4.4 |

## 8. Recommendations

| Recommendation ID | Recommendation | Priority | Owner | Target Timeframe |
|---|---|---|---|---|
| REC-001 | Establish a recurring cloud configuration review (e.g. Microsoft Secure Score / CIS Azure Benchmark) reported to the Cyber Security Governance Group | High | Cloud Service Owner | Q4 2026 |
| REC-002 | Enforce MFA and Conditional Access for all Entra ID accounts, prioritising privileged and clinical accounts | High | Identity Security Lead | Q3 2026 |
| REC-003 | Document a cloud data protection control set (encryption, key management, residency) for Restricted-classified cloud services | Medium | CISO / Data Protection Officer | Q1 2027 |
| REC-004 | Implement and evidence a recurring backup/restore test cycle for Azure-hosted workloads | Medium | Infrastructure Manager | Q4 2026 |

## 9. Conclusion

Cloud risk at WHT is concentrated around identity governance and configuration oversight rather than a gap in the underlying platform's security capability. Because Entra ID sits at the centre of both the Trust's most exposed patient-facing services and its weakest CAF principle (B2), closing REC-002 should be treated as the single highest-leverage action in this assessment, with the remaining recommendations tracked through [../12-Azure-Governance/](../12-Azure-Governance/) and the wider improvement roadmap in [../14-RoadMap/](../14-RoadMap/).
