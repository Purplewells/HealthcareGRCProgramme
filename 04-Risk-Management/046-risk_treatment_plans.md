# Risk Treatment Plans

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Risk Treatment Plans
**Owner:** Chief Information Security Officer (CISO)
**Version:** 1.0

## 1. Introduction

### 1.1 Purpose

This document expands the single-line treatment status recorded in [risk_register](risk_register.md) §6 into a full treatment plan per risk — specific actions, owners, target dates, and expected residual risk — so that risk owners and the Cyber Security Governance Group can track delivery rather than only status labels.

### 1.2 Scope

This document covers treatment plans for all 12 risks in [risk_register](risk_register.md) §4 (CR-001 to CR-012). It does not cover the domain-specific sub-risks identified in [041-cloud_risk](041-cloud_risk.md), [042-medical_device_risk](042-medical_device_risk.md), and [043-third_party_risks](043-third_party_risks.md) (e.g. MDR-001, TPR-001) — those are tracked by their respective domain owners pending incorporation into a future register update.

## 2. Assessment Criteria

### 2.1 Framework(s) Applied

Treatment prioritisation follows the Trust's standard risk methodology in [047-risk_methodology](047-risk_methodology.md): Critical-rated risks require immediate action, High-rated risks require treatment, Medium-rated risks are managed through normal process.

### 2.2 Rating Scale

| Status | Description |
|---|---|
| Planned | Treatment actions defined but not yet started |
| In Progress | Treatment actions actively underway |
| Embedded | Treatment actions complete and operating as business-as-usual |

## 3. Current State

Of the 12 risks in the register, 2 are currently In Progress (CR-001, CR-005) and 1 (CR-007) is In Progress per [risk_register](risk_register.md) §6; the remaining 9 are Planned. No risk has yet reached Embedded status. The full treatment plan for each risk is set out below.

| Risk ID | Description | Treatment Actions | Owner | Target Date | Status | Expected Residual Rating |
|---|---|---|---|---|---|---|
| CR-001 | Ransomware affecting clinical services | Network segmentation; endpoint protection uplift; privileged access review; ransomware exercises; offline backup validation | CDIO | Q4 2026 | In Progress | High |
| CR-002 | Compromise of Microsoft 365 accounts | Enforce MFA and Conditional Access Trust-wide; review legacy authentication protocols; identity governance uplift | Identity Security Lead | Q3 2026 | Planned | Medium |
| CR-003 | Unsupported medical devices exploited | Complete device inventory; vulnerability assessment; network segmentation for unsupported devices; replacement roadmap | Clinical Engineering Manager | Q4 2026 | Planned | High |
| CR-004 | Excessive user access privileges | Implement role-based access control; recurring access review cycle; segregation of duties review | IAM Manager | Q1 2027 | Planned | Medium |
| CR-005 | Patient data exposure | Data classification remediation; DLP controls; uncontrolled copy remediation | Data Protection Officer | Q1 2027 | In Progress | Medium |
| CR-006 | Third-party supplier compromise | Supplier security assurance process; contractual security clauses; annual supplier review | Procurement Director | Q4 2026 | Planned | Medium |
| CR-007 | Incomplete asset inventory | Master asset register maintenance; ownership assignment; periodic review cadence | IT Asset Manager | Q3 2026 | In Progress | Low |
| CR-008 | Security awareness failure | Mandatory tracked training; completion reporting to governance forum | Security Awareness Lead | Q1 2027 | Planned | Medium |
| CR-009 | Insufficient security monitoring | Expand SOC/MSSP monitoring coverage; define and report security metrics | SOC Manager | Q1 2027 | Planned | High |
| CR-010 | Clinical service disruption | Resilience testing programme; recovery time objective validation | Business Continuity Manager | Q2 2027 | Planned | Medium |
| CR-011 | Data loss due to inadequate backup protection | Recurring backup/restore test schedule; offline/immutable backup implementation | Backup Service Owner | Q4 2026 | Planned | Medium |
| CR-012 | Cloud security misconfiguration | Recurring cloud configuration review; Secure Score / CIS Azure Benchmark adoption | Cloud Security Engineer | Q4 2026 | Planned | Medium |

## 4. Observations

### 4.1 Only One Risk (CR-007) is Approaching an Embedded State

CR-007's treatment (asset inventory) has benefited directly from the completed work in [../02-Asset-Management/](../02-Asset-Management/), and is the only risk on a credible path to Low residual risk, again demonstrating the "focused investment works" pattern identified in [../03-Current-State-Assessment/025-maturity_assessment](../03-Current-State-Assessment/025-maturity_assessment.md) §4.4.

### 4.2 The Highest-Scored Risk (CR-001) Has an Ambitious Residual Target That May Still Land at High

Even with treatment actions in progress, CR-001's expected residual rating is High, not Low or Medium — ransomware risk to clinical services cannot be fully eliminated through the planned actions alone, and continued monitoring and re-assessment will be needed after Q4 2026.

### 4.3 Nine of Twelve Risks Remain Planned, Not Started

The majority of treatment actions have not yet begun, meaning the risk register's current scores in [risk_register](risk_register.md) §4 remain an accurate reflection of today's actual exposure — the residual ratings in this document are targets, not current state.

### 4.4 Treatment Ownership is Distributed Across the Organisation, Not Centralised in the CISO Function

Treatment owners span IT, clinical engineering, procurement, HR, and business continuity functions, which is appropriate given the risk ownership model in [risk_register](risk_register.md) §2, but requires active cross-functional coordination — a role the Cyber Security Governance Group (recommended in [../03-Current-State-Assessment/021-current_state_assessment](../03-Current-State-Assessment/021-current_state_assessment.md) REC-001) is intended to fill.

## 5. Evidence

| Evidence ID | Description | Source | Date | Linked Observation |
|---|---|---|---|---|
| EVD-001 | Risk Treatment Status table | [risk_register](risk_register.md) §6 | 2026-07-23 | 4.3 |
| EVD-002 | Master Asset Register completion | [../02-Asset-Management/022-master_assets_register.xlsx](../02-Asset-Management/022-master_assets_register.xlsx) | 2026-07-23 | 4.1 |
| EVD-003 | Recommendation to establish a Cyber Security Governance Group | [../03-Current-State-Assessment/021-current_state_assessment](../03-Current-State-Assessment/021-current_state_assessment.md) §8 REC-001 | 2026-07-23 | 4.4 |

## 6. Analysis

### 6.1 Findings

Treatment planning is well-defined in terms of actions and ownership, but weak in terms of actual progress: only 3 of 12 risks show any movement beyond "Planned". This mirrors the wider programme finding that the Trust has good documentation but limited execution rhythm — treatment plans exist on paper for all 12 risks, but the cross-functional governance forum needed to drive them to completion is itself still a recommendation rather than an operating reality.

### 6.2 Root Cause

The root cause is sequencing: treatment cannot meaningfully accelerate across 9 Planned risks until the Cyber Security Governance Group (REC-001 in [../03-Current-State-Assessment/021-current_state_assessment](../03-Current-State-Assessment/021-current_state_assessment.md)) exists to hold owners to the target dates in this document. Without that forum, treatment progress depends on individual owner initiative rather than programme-level accountability.

## 7. Risk Rating

| Risk ID | Description | Likelihood | Impact | Rating | Linked Observation |
|---|---|---|---|---|---|
| CR-001 | Ransomware affecting clinical services | 5 | 5 | Critical | 4.2 |
| CR-009 | Insufficient security monitoring | 3 | 5 | High | 4.3 |
| CR-010 | Clinical service disruption | 3 | 5 | High | 4.3 |

## 8. Recommendations

| Recommendation ID | Recommendation | Priority | Owner | Target Timeframe |
|---|---|---|---|---|
| REC-001 | Stand up the Cyber Security Governance Group and make treatment plan progress a standing agenda item | High | CISO | Q3 2026 |
| REC-002 | Move at least 3 of the 9 "Planned" risks to "In Progress" within the next quarter, prioritising CR-002, CR-006, and CR-012 given their achievable near-term actions | High | CISO | Q4 2026 |
| REC-003 | Re-assess CR-001's residual rating after Q4 2026 treatment actions complete, rather than assuming the High target is final | Medium | CDIO | Q1 2027 |
| REC-004 | Formally track this document alongside [risk_register](risk_register.md) §6 at each quarterly risk review, updating status and residual ratings | Medium | CISO | Ongoing, quarterly |

## 9. Conclusion

WHT has a treatment plan defined for every risk in its register, but delivery is still early: only a quarter of risks show active progress, and none are yet embedded. The single highest-leverage action is establishing the Cyber Security Governance Group, since treatment progress across a distributed set of owners depends on a central forum holding them to these target dates — without it, this document risks remaining an accurate plan that is never fully executed.
