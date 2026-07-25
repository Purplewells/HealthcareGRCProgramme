# Azure Governance Assessment

**Project:** Project SentinelCare – Cyber Security Governance, Risk and Compliance Improvement Programme
**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Assessment
**Owner:** Cloud Service Owner
**Version:** 1.0

## 1. Introduction

### 1.1 Purpose

This assessment examines how well WHT's Azure environment is governed — subscription and management group structure, role-based access control, policy enforcement, and tagging/cost discipline — as distinct from [041-cloud_risk](../04-Risk-Management/041-cloud_risk.md), which assesses cloud risk at the register level, and [093-secure_baseline](../09-Security-Operations/093-secure_baseline.md), which addresses technical configuration hardening. It answers: *is the Azure estate structured and administered in a way that lets WHT's existing policies (access control, data classification) actually be enforced, or does the platform's own governance undermine them?* This assessment, together with [122-conditional_access_policies](122-conditional_access_policies.md) and [123-secure_score_review](123-secure_score_review.md), closes out REC-001 and REC-002 in [041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §8.

### 1.2 Scope

**In scope:** the Azure Cloud Environment (AST-017) and Microsoft Entra ID (AST-029) as recorded in [../02-Asset-Management/022-master_assets_register.xlsx](../02-Asset-Management/022-master_assets_register.xlsx), including subscription/management group hierarchy, Azure RBAC, Azure Policy, and tagging standards. It covers the governance surface underneath the four Azure-hosted patient-facing applications — Patient Portal (AST-007), Appointment Booking Platform (AST-008), Remote Consultation Platform (AST-009), Patient Messaging Service (AST-010) — without re-assessing those applications individually.

**Out of scope:** Conditional Access policy content (covered in [122-conditional_access_policies](122-conditional_access_policies.md)), Microsoft Secure Score control-by-control detail (covered in [123-secure_score_review](123-secure_score_review.md)), and Microsoft 365 workload-specific configuration (SharePoint, Exchange Online), which sits outside the Azure subscription boundary this assessment covers.

## 2. Assessment Criteria

### 2.1 Framework(s) Applied

This assessment is measured against the **Microsoft Cloud Security Benchmark (MCSB)** control domains for Governance, Identity Management, and Privileged Access, cross-referenced to the NCSC Cyber Assessment Framework principles already scored in [../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) — principally B2 (Identity and Access Control), B4 (System Security), and A1 (Board Direction / governance ownership).

### 2.2 Rating Scale

Each governance area is rated **Achieved / Partially Achieved / Not Achieved**, consistent with the scale used in the CAF assessment, so findings here can be read directly alongside that document without translation. Risks identified are scored using the Trust's standard Likelihood × Impact methodology ([../04-Risk-Management/047-risk_methodology](../04-Risk-Management/047-risk_methodology.md)).

## 3. Current State

WHT's Azure environment underpins four Restricted-classified, patient-facing services and sits behind Microsoft Entra ID, which [041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §4.2 already identifies as a single point of failure across the Trust's cloud estate. Azure adoption has, consistent with that assessment's root cause finding (§6.2), proceeded service-by-service without a corresponding management group/subscription structure, RBAC model, or policy set being defined centrally. A single flat subscription is in use for all four patient-facing applications, with no management group hierarchy separating production from non-production workloads, and no Azure Policy assignments enforcing the Trust's existing data classification or configuration standards at the platform level. This is not a case of no governance controls existing — the Trust's [054-access_control_policy](../05-Governance/054-access_control_policy.md) and [093-secure_baseline](../09-Security-Operations/093-secure_baseline.md) both set clear requirements — but of the Azure platform's own governance tooling (Management Groups, Azure Policy, RBAC scoping) not yet being configured to enforce them.

## 4. Observations

### 4.1 No Management Group Hierarchy Separates Environments or Enforces Policy at Scale

All Azure resources sit in a single subscription with no management group structure, meaning there is no platform-level boundary between production patient-facing services and any non-production/test workloads, and no scope at which an Azure Policy could be assigned once and inherited Trust-wide.

### 4.2 Azure RBAC is Not Modelled on the Trust's Access Control Policy

Role assignments in the Azure environment are made ad hoc at the subscription level rather than scoped to resource groups per application (AST-007–AST-010), which is inconsistent with the least-privilege and role-based principles set out in [054-access_control_policy](../05-Governance/054-access_control_policy.md) §3.1, and with CR-004 (Excessive user access privileges) in [049-risk_register](../04-Risk-Management/049-risk_register.md).

### 4.3 No Azure Policy Assignments Enforce Existing Standards

No Azure Policy definitions or initiatives are assigned at subscription or management group scope to enforce the secure configuration baseline already defined for cloud services in [093-secure_baseline](../09-Security-Operations/093-secure_baseline.md) §4, meaning that standard's "Not yet formally assessed" status for Azure/cloud services reflects an absence of the enforcement mechanism, not just an absence of assessment.

### 4.4 No Consistent Resource Tagging for Ownership or Data Classification

Resources are not consistently tagged with an owning application, Information Asset Owner, or data classification (Restricted/Confidential/Internal per [../06-Information-Governance/041-data_classification](../06-Information-Governance/041-data_classification.md)), which limits the Trust's ability to confirm — at the platform level — that Restricted-classified resources are receiving the controls their classification requires.

### 4.5 No Recurring Governance Review Cadence Exists for the Azure Estate

Unlike the CSGG's monthly access-review oversight ([054-access_control_policy](../05-Governance/054-access_control_policy.md) §4), no equivalent recurring review of Azure subscription structure, RBAC assignments, or policy compliance has been established, consistent with the general absence of a cloud configuration review process already flagged in [041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §4.1.

## 5. Evidence

| Evidence ID | Description | Source | Date | Linked Observation |
|---|---|---|---|---|
| EVD-001 | Single flat subscription hosting AST-007–AST-010 with no management group hierarchy | Azure environment (AST-017) subscription structure | 2026-07-24 | 4.1 |
| EVD-002 | CR-004 Excessive user access privileges, scored in master risk register | [../04-Risk-Management/049-risk_register.md](../04-Risk-Management/049-risk_register.md) | 2026-07-24 | 4.2 |
| EVD-003 | Azure/cloud services baseline coverage status: "Not yet formally assessed" | [../09-Security-Operations/093-secure_baseline.md](../09-Security-Operations/093-secure_baseline.md) §4 | 2026-07-24 | 4.3 |
| EVD-004 | No cloud-specific data protection control set documented (encryption, key management, residency) | [../04-Risk-Management/041-cloud_risk.md](../04-Risk-Management/041-cloud_risk.md) §4.3 | 2026-07-24 | 4.4 |
| EVD-005 | No dedicated, recurring configuration review process for the Azure environment | [../04-Risk-Management/041-cloud_risk.md](../04-Risk-Management/041-cloud_risk.md) §4.1 | 2026-07-24 | 4.5 |

## 6. Analysis

### 6.1 Findings

The Azure environment's governance gaps are structural rather than incidental: without a management group hierarchy, there is no scope at which the Trust could assign a policy or RBAC model Trust-wide even if one were defined today. This means REC-002 in [041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) (enforce MFA/Conditional Access) and REC-003 (document a cloud data protection control set) both depend on this assessment's findings being remediated first — enforcing a control at the identity layer or documenting a data protection standard has limited effect if there is no policy mechanism to apply it consistently across the estate.

### 6.2 Root Cause

Azure services were provisioned to meet individual application delivery timelines (Patient Portal, Appointment Booking, Remote Consultation, Patient Messaging) without a Cloud Landing Zone or equivalent governance foundation being established first — the same adoption pattern already identified as the root cause of cloud risk generally in [041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §6.2, here manifesting specifically as an absent management group/policy/RBAC structure rather than a specific misconfiguration.

## 7. Risk Rating

| Risk ID | Description | Likelihood | Impact | Rating | Linked Observation |
|---|---|---|---|---|---|
| CR-012 | Cloud security misconfiguration | 3 | 5 | High | 4.1, 4.3 |
| CR-004 | Excessive user access privileges | 4 | 4 | High | 4.2 |
| AZG-001 | Absence of Azure Policy enforcement allows Restricted-classified resources to be provisioned without required controls | 3 | 4 | High | 4.3, 4.4 |
| AZG-002 | No recurring Azure governance review allows drift to persist undetected between assessments | 3 | 3 | Medium | 4.5 |

## 8. Recommendations

| Recommendation ID | Recommendation | Priority | Owner | Target Timeframe |
|---|---|---|---|---|
| AZG-REC-001 | Establish a management group hierarchy separating production patient-facing workloads from non-production, as the scope for Trust-wide policy and RBAC assignment | High | Cloud Service Owner | Q4 2026 |
| AZG-REC-002 | Re-model Azure RBAC on the Trust's access control policy, scoping role assignments to resource groups per application (AST-007–AST-010) rather than subscription-wide | High | Identity Security Lead | Q4 2026 |
| AZG-REC-003 | Assign Azure Policy initiatives (Microsoft Cloud Security Benchmark) at management group scope to enforce the existing secure baseline for cloud services | High | Cloud Service Owner | Q1 2027 |
| AZG-REC-004 | Implement a mandatory tagging standard (owning application, Information Asset Owner, data classification) enforced via Azure Policy | Medium | Cloud Service Owner | Q1 2027 |
| AZG-REC-005 | Establish a monthly Azure governance review (subscription structure, RBAC, policy compliance) reported to the CSGG alongside existing access review reporting | Medium | Cloud Service Owner | Q4 2026 |

## 9. Conclusion

WHT's Azure environment has adequate underlying platform capability but no governance structure configured to direct it — the same "capability exists, configuration doesn't enforce it" pattern already identified for cloud risk generally in [041-cloud_risk](../04-Risk-Management/041-cloud_risk.md). Because a management group hierarchy is the prerequisite scope for both RBAC remodelling and policy enforcement, AZG-REC-001 should be sequenced first; [122-conditional_access_policies](122-conditional_access_policies.md) and [123-secure_score_review](123-secure_score_review.md) extend this assessment into identity-layer and control-scoring detail respectively.
