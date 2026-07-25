# Secure Score Review

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Recurring Control Review
**Owner:** Cloud Service Owner
**Version:** 1.0
**Review Period:** Q3 2026 (baseline review)

## 1. Purpose

This document establishes Microsoft Secure Score as WHT's recurring cloud configuration review mechanism, directly closing REC-001 in [../04-Risk-Management/041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §8 ("Establish a recurring cloud configuration review... reported to the Cyber Security Governance Group"), and records the Trust's baseline score and improvement actions as of this review period.

## 2. Scope

Secure Score is reviewed across Microsoft 365 (AST-011), Microsoft Entra ID (AST-029), and the Azure Cloud Environment (AST-017) — the same asset scope as [041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §1.2. Medical devices and on-premises infrastructure are out of scope, as Secure Score does not assess them.

## 3. Baseline Score

| Category | Points Achieved | Points Available | % Achieved |
|---|---|---|---|
| Identity | 28 | 92 | 30% |
| Device | 41 | 78 | 53% |
| Apps | 19 | 54 | 35% |
| Data | 12 | 36 | 33% |
| **Overall** | **100** | **260** | **38%** |

An overall score of 38% is consistent with the "Developing" maturity self-assessed in [../03-Current-State-Assessment/025-maturity_assessment](../03-Current-State-Assessment/025-maturity_assessment.md) and with CAF B2 Identity and Access Control being rated **Not Achieved** — Identity is both the lowest-scoring category here and the Trust's weakest CAF principle, corroborating [041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §4.2's finding that identity is a single point of failure across the cloud estate.

## 4. Top Improvement Actions

| Action | Score Impact | Category | Linked Recommendation |
|---|---|---|---|
| Enable MFA-enforcing Conditional Access policies for all users | +18 points | Identity | [122-conditional_access_policies](122-conditional_access_policies.md) CAP-001 |
| Enable MFA-enforcing Conditional Access for privileged/admin roles | +9 points | Identity | [122-conditional_access_policies](122-conditional_access_policies.md) CAP-002 |
| Block legacy authentication protocols | +7 points | Identity | [122-conditional_access_policies](122-conditional_access_policies.md) CAP-003 |
| Designate more than one Global Administrator with reduced standing privileged role assignments | +5 points | Identity | [121-azure_governance_assessment](121-azure_governance_assessment.md) AZG-REC-002 |
| Enable Microsoft Defender for Cloud Apps anomaly detection policies | +6 points | Apps | New — track as SSC-REC-003 |
| Enable Azure Policy compliance monitoring for Restricted-classified resources | +8 points | Data | [121-azure_governance_assessment](121-azure_governance_assessment.md) AZG-REC-003 |

The four highest-impact actions are all Identity category and are already covered by the Conditional Access rollout in [122-conditional_access_policies](122-conditional_access_policies.md) §7 — completing that rollout alone would raise the Identity category from 30% to approximately 73% and the overall score from 38% to approximately 53%.

## 5. Review Cadence

Secure Score is reviewed monthly by the Cloud Service Owner, with the trend (not just point-in-time score) reported to the Cyber Security Governance Group quarterly, alongside its existing access review and CSGG reporting cadence ([../05-Governance/054-access_control_policy](../05-Governance/054-access_control_policy.md) §4). A material score drop between reviews is treated as a potential configuration drift signal and investigated per [121-azure_governance_assessment](121-azure_governance_assessment.md) AZG-REC-005.

## 6. History

| Review Date | Overall Score | Change | Notes |
|---|---|---|---|
| 2026-07-24 | 100/260 (38%) | Baseline | First formal review; establishes recurring cadence per REC-001 |

## 7. Related Documents

- [121-azure_governance_assessment](121-azure_governance_assessment.md)
- [122-conditional_access_policies](122-conditional_access_policies.md)
- [../04-Risk-Management/041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §8 (REC-001)
- [../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) (CAF B2, B4)

## 8. Conclusion

The baseline Secure Score of 38% quantifies, rather than replaces, findings already recorded elsewhere in the programme: identity is simultaneously the lowest-scoring category and the highest-leverage one, since the four actions with the largest point impact are already scoped as the Conditional Access rollout in [122-conditional_access_policies](122-conditional_access_policies.md). Establishing this monthly review closes REC-001; the score itself should be expected to rise through Q4 2026 as that rollout and the Azure Policy actions in [121-azure_governance_assessment](121-azure_governance_assessment.md) complete, rather than through further assessment.
