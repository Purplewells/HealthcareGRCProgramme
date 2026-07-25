# 12-Month Improvement Plan

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Improvement Plan
**Owner:** CISO (Chief Information Security Officer)
**Version:** 1.0
**Period Covered:** Q3 2026 – Q3 2027

## 1. Purpose

This plan puts the twelve initiatives from [141-cyber_security_roadmap](141-cyber_security_roadmap.md) §3 on a quarter-by-quarter timeline, so progress can be tracked against a specific reporting period rather than only an initiative's overall target quarter. It is the operational detail behind the roadmap's phasing (§4 of that document).

## 2. Q3 2026 (Jul–Sep 2026)

| Initiative | Action This Quarter | Owner |
|---|---|---|
| INIT-01 | Link VUL-007 to a risk ID; confirm remediation against its 14-day SLA; extend escalation logic | Infrastructure Manager |
| INIT-09 | Agree DSPT improvement plan with NHS England/ICB ahead of annual submission | CISO |
| INIT-02 | Draft supplier assurance process design (onboarding assessment template, contractual security clause set) | Procurement Director |
| INIT-06 | Establish Azure management group hierarchy (foundation for RBAC/policy work in Q4) | Cloud Service Owner |
| INIT-04 | Complete Conditional Access Report-only validation (CAP-001, CAP-002); begin enforcement for privileged roles | Identity Security Lead |
| — | Resolve SUP-005 assurance renewal and confirm Theatre Management System contingency position | Theatre Manager / Procurement Director |

**Quarter-end checkpoint:** the one Critical audit finding (AUD-001) should be closed; the DSPT submission position should be "Standards Not Met (Plan Agreed)" rather than "Standards Not Met."

## 3. Q4 2026 (Oct–Dec 2026)

| Initiative | Action This Quarter | Owner |
|---|---|---|
| INIT-02 | Launch supplier assurance process; complete initial assessment for suppliers holding Restricted-classified data | Procurement Director |
| INIT-07 | Complete medical device vulnerability assessment; publish prioritised replacement/compensating-control plan | Clinical Engineering Manager |
| INIT-08 | Implement offline/immutable backup copy; run first full restore test against a Tier 1 system | Infrastructure Manager |
| INIT-04 | Enforce Trust-wide MFA and legacy authentication block (CAP-001, CAP-003); re-model Azure RBAC (AZG-REC-002) | Identity Security Lead |
| INIT-06 | Establish monthly Azure/Secure Score governance review reported to CSGG | Cloud Service Owner |
| INIT-11 | Charter formal Internal Audit function / co-sourced provider with Three Lines Model | Audit and Risk Committee |
| INIT-12 | Remediate uncontrolled copies of patient reports identified in internal audit | Data Protection Officer |

**Quarter-end checkpoint:** all four High-severity audit findings (AUD-002, AUD-003, AUD-004, AUD-008) should have moved from "Open" to "In Progress," per [141-cyber_security_roadmap](141-cyber_security_roadmap.md) §4.2.

## 4. Q1 2027 (Jan–Mar 2027)

| Initiative | Action This Quarter | Owner |
|---|---|---|
| INIT-03 | Implement Trust-wide role-based access control and recurring access review cycle | IAM Manager |
| INIT-05 | Expand security monitoring/detection coverage beyond the single MSSP relationship | CISO / SOC Manager |
| INIT-06 | Assign Azure Policy initiatives (Microsoft Cloud Security Benchmark) at management group scope; enforce mandatory tagging | Cloud Service Owner |
| INIT-10 | Deploy mandatory, tracked security awareness training with completion reporting | Security Awareness Lead |
| INIT-12 | Extend lawful basis documentation and data classification to remaining core clinical systems (LIS, RIS/PACS, Pharmacy, Theatre) | Data Protection Officer |
| — | Formally scope an Information Security Management System (ISO Clause 4) with a management review cycle | CISO |

**Quarter-end checkpoint:** CAF principles B2 (Identity and Access Control) and C1/C2 (Detection) should move from Not Achieved to at least Partially Achieved when [022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) is next re-run.

## 5. Q2–Q3 2027 (Apr–Sep 2027)

| Initiative | Action This Quarter | Owner |
|---|---|---|
| — | Scope a dedicated physical security review to convert the provisional ISO A.7 rating into a verified position | Infrastructure Manager |
| — | Establish a secondary/failover site or environment for Tier 1/2 on-premises systems | Infrastructure Manager |
| Phase 4 | Re-run CAF, ISO 27001, and DSPT assessments to confirm rating movement | CISO |
| Phase 4 | Re-perform internal audit in-scope areas, prioritising re-testing of AUD-001 through AUD-004 | Head of Internal Audit |

## 6. Tracking

Each quarter's actions are reported against actual delivery at the following quarter's CSGG meeting; any action not delivered on schedule is carried forward with a stated reason, rather than silently dropped, and reflected in the next update to [113-capa_tracker](../11-Audit/113-capa_tracker.xlsx). Quarter-end checkpoints (§2–4) are the pass/fail criteria this plan is measured against, not the individual actions in isolation.

## 7. Review and Maintenance

This plan is re-baselined quarterly alongside [141-cyber_security_roadmap](141-cyber_security_roadmap.md), and immediately if a new Critical/High finding is raised that changes the sequencing logic in that document §2.2.
