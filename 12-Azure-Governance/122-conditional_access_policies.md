# Conditional Access Policies

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Standard — Identity Control Configuration
**Owner:** Identity Security Lead
**Version:** 1.0
**Effective Date:** 2026-07-24
**Review Date:** 2027-07-24

## 1. Purpose

This standard records the Microsoft Entra ID (AST-029) Conditional Access policy set that implements [054-access_control_policy](../05-Governance/054-access_control_policy.md) §3.3 (enhanced controls for privileged and administrative access) and directly closes REC-002 in [../04-Risk-Management/041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §8 ("Enforce MFA and Conditional Access for all Entra ID accounts, prioritising privileged and clinical accounts"). It exists because Entra ID is the Trust's single identity control point across Microsoft 365, the Azure Cloud Environment, and all four Restricted-classified patient-facing services ([../04-Risk-Management/041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §4.2), and CAF B2 Identity and Access Control is currently rated **Not Achieved** ([../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) §3).

## 2. Scope

This standard applies to all Microsoft Entra ID accounts authenticating to Microsoft 365, the Azure Cloud Environment (AST-017), and the four patient-facing applications (Patient Portal AST-007, Appointment Booking Platform AST-008, Remote Consultation Platform AST-009, Patient Messaging Service AST-010). It does not cover on-premises Active Directory authentication, which remains out of scope until the Trust's planned Entra Connect consolidation.

## 3. Current Coverage

Conditional Access is not yet enforced Trust-wide. The policies in §4 are designed to close this gap but, as of this review, only CAP-001 and CAP-002 are enabled in Report-only mode; the remainder are documented as the target design and are not yet enforcing. This partial state is the direct cause of CR-002 (Compromise of Microsoft 365 accounts, rated Critical) remaining open in [049-risk_register](../04-Risk-Management/049-risk_register.md).

## 4. Policy Set

| Policy ID | Name | Assignment | Conditions | Grant Control | Status |
|---|---|---|---|---|---|
| CAP-001 | Require MFA for all users | All users, all cloud apps | Any location | Require multi-factor authentication | Report-only |
| CAP-002 | Require MFA for privileged roles | Global Administrator, Privileged Role Administrator, and other Entra ID built-in privileged roles | Any location | Require multi-factor authentication + require compliant device | Report-only |
| CAP-003 | Block legacy authentication | All users, all cloud apps | Legacy authentication clients (POP, IMAP, older Office clients) | Block access | Not yet enabled |
| CAP-004 | Require compliant device for clinical applications | All users accessing Remote Consultation Platform (AST-009) and Patient Messaging Service (AST-010) | Any location | Require Microsoft Entra hybrid joined or compliant device | Not yet enabled |
| CAP-005 | Require MFA for Azure management | All users, Microsoft Azure Management | Any location | Require multi-factor authentication | Not yet enabled |
| CAP-006 | Block access from unknown/unmanaged locations for admin roles | Privileged roles (as CAP-002) | Location not in named trusted locations | Block access | Not yet enabled |
| CAP-007 | Sign-in risk-based policy | All users | Sign-in risk: Medium or High (Entra ID Protection) | Require multi-factor authentication | Not yet enabled — dependent on Entra ID Protection licensing confirmation |

## 5. Exceptions

Break-glass emergency access accounts (two accounts, per Microsoft best practice) are excluded from CAP-001–CAP-007 by design, are excluded from all Conditional Access policies, use high-complexity passwords with no MFA registered on any device, and are stored in a sealed, access-logged process consistent with [054-access_control_policy](../05-Governance/054-access_control_policy.md) §8. Any other exclusion from a policy in §4 must be time-boxed, documented, and approved by the CISO, per [054-access_control_policy](../05-Governance/054-access_control_policy.md) §8.

## 6. Roles and Responsibilities

The Identity Security Lead owns policy configuration and the Report-only-to-enforced rollout in §7. The CISO approves any exception under §5. The Cyber Security Governance Group (CSGG) receives monthly reporting on policy enforcement status, consistent with its existing access review oversight under [054-access_control_policy](../05-Governance/054-access_control_policy.md) §4.

## 7. Rollout Plan

| Milestone | Policies | Target Date |
|---|---|---|
| Report-only validation complete, sign-in log review for false positives | CAP-001, CAP-002 | Q3 2026 |
| Enforce for privileged roles first | CAP-002, CAP-006 | Q3 2026 |
| Enforce Trust-wide MFA and legacy auth block | CAP-001, CAP-003 | Q4 2026 |
| Enforce for Azure management plane and clinical applications | CAP-004, CAP-005 | Q4 2026 |
| Enable risk-based policy, subject to licensing confirmation | CAP-007 | Q1 2027 |

This rollout plan is the mechanism by which REC-002 in [../04-Risk-Management/041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §8 is closed; completion should be reported to the CSGG and reflected as a status change on that recommendation.

## 8. Related Documents

- [121-azure_governance_assessment](121-azure_governance_assessment.md) — identifies the absent RBAC/policy scope this Conditional Access rollout depends on (AZG-REC-002)
- [054-access_control_policy](../05-Governance/054-access_control_policy.md)
- [041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §4.2, §8 (REC-002)
- [022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) (CAF B2)
- [049-risk_register](../04-Risk-Management/049-risk_register.md) (CR-002, CR-004)

## 9. Review

This standard is reviewed quarterly by the Identity Security Lead while the rollout plan (§7) is in progress, and annually thereafter, or sooner following an identity-related security incident or a material change to the Entra ID licensing tier available to the Trust.
