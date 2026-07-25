# Security Strategy

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Security Strategy
**Owner:** Chief Information Security Officer (CISO)
**Version:** 1.0

## 1. Introduction

### 1.1 Purpose

This document sets out WHT's cyber security strategy: the vision, strategic objectives, and governance structure through which the Trust will close the gaps identified across Project SentinelCare's discovery, current-state, and risk management phases. It is the mechanism by which the programme's most significant open recommendation — establishing a standing governance forum — is formally actioned.

### 1.2 Scope

This strategy covers cyber security governance, strategic prioritisation, and the operating structure needed to sustain risk management, compliance, and control effectiveness across WHT on an ongoing basis. It does not restate the detailed findings of the current-state or risk assessments — it responds to them. Operational roles and RACI detail are set out separately in [052-roles_and_responsibilities](052-roles_and_responsibilities.md); policy-level control requirements are set out in [053-information_security_policy](053-information_security_policy.md) and its companion policies.

## 2. Strategic Context

WHT has undergone rapid digital transformation over the past five years without a corresponding scale-up in cyber security governance, risk management, and compliance capability (see [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md)). The cross-framework maturity roll-up in [../03-Current-State-Assessment/025-maturity_assessment](../03-Current-State-Assessment/025-maturity_assessment.md) confirms this pattern consistently: the Trust has the *documentation and structural foundations* for good governance (registers, policies, ownership models) but lacks the *operating rhythm* — measured, reviewed, board-reported activity — that would move it from "Established" to "Managed" maturity.

The single most consequential gap identified across every current-state and risk document produced so far is the absence of a standing governance forum. [021-current_state_assessment](../03-Current-State-Assessment/021-current_state_assessment.md) §4.1 and §6.2 identifies this as the Trust-wide root cause of fragmented governance; [047-risk_methodology](../04-Risk-Management/047-risk_methodology.md) §6.2 identifies it as the reason risk methodology is not continuously applied; and [046-risk_treatment_plans](../04-Risk-Management/046-risk_treatment_plans.md) identifies it as the reason risk treatment progress has stalled. This strategy exists primarily to close that gap.

## 3. Vision & Strategic Objectives

**Vision:** WHT's digital services are trusted, resilient, and secure by design, enabling safe patient care without cyber risk becoming a barrier to clinical innovation.

Strategic objectives, aligned to the CAF outcome mapping in [../01-Discovery/004-project_objectives](../01-Discovery/004-project_objectives.md):

| Objective | Description | Primary Framework Driver |
|---|---|---|
| SO-1 | Establish continuous, board-reported cyber security governance | CAF A1 Governance |
| SO-2 | Move risk management from periodic to continuous operating rhythm | CAF A2/A3; risk methodology REC-001 |
| SO-3 | Close identity and access control gaps, particularly in cloud and clinical systems | CAF B2 |
| SO-4 | Establish centralised, risk-based third-party supplier assurance | CAF A4; ISO 27001 Annex A.15 |
| SO-5 | Build sustained staff security awareness and training | CAF B6 |
| SO-6 | Expand security monitoring and incident detection capability | CAF C1/C2 |

## 4. Governance Structure

### 4.1 The Cyber Security Governance Group

This strategy formally establishes the **Cyber Security Governance Group (CSGG)**, closing [021-current_state_assessment](../03-Current-State-Assessment/021-current_state_assessment.md) REC-001 ("Establish a Cyber Security Governance Group with a standing mandate to review policy application and control effectiveness Trust-wide"). The CSGG is the standing forum already assumed to exist by the risk register's reporting cadence and by multiple domain risk assessments — this section is its charter.

**Mandate:** The CSGG is accountable for Trust-wide oversight of cyber security policy application, control effectiveness, risk treatment progress, and compliance posture. It is the single governance forum through which cyber risk is escalated, reviewed, and reported.

**Membership:**

| Role | Source |
|---|---|
| Chief Information Security Officer (CISO) — **Chair** | [006-stakeholders](../01-Discovery/006-stakeholders.md) §2 |
| Senior Information Risk Owner (SIRO) | [006-stakeholders](../01-Discovery/006-stakeholders.md) §2 |
| Caldicott Guardian | [006-stakeholders](../01-Discovery/006-stakeholders.md) §2 |
| Chief Digital Information Officer (CDIO) | [006-stakeholders](../01-Discovery/006-stakeholders.md) §2 |
| Data Protection Officer (DPO) | [006-stakeholders](../01-Discovery/006-stakeholders.md) §5 |
| Cyber Security Team (representative) | [006-stakeholders](../01-Discovery/006-stakeholders.md) §4 |
| Risk Management Team (representative) | [006-stakeholders](../01-Discovery/006-stakeholders.md) §5 |

Full terms of reference (quorum, escalation path, standing agenda) are set out in [052-roles_and_responsibilities](052-roles_and_responsibilities.md) §3.

**Cadence:** Monthly meetings, consistent with the reporting cadence already assumed by [risk_register](../04-Risk-Management/risk_register.md), with a quarterly cycle for heat map republication ([045-risk_heat_map](../04-Risk-Management/045-risk_heat_map.md)) and cross-framework maturity re-assessment.

**Reporting line:** The CSGG reports quarterly to the Audit and Risk Committee, which in turn provides assurance to the Trust Board, consistent with the escalation structure described in [006-stakeholders](../01-Discovery/006-stakeholders.md) §2.

### 4.2 Standing Agenda

1. Risk register review and treatment plan progress ([risk_register](../04-Risk-Management/risk_register.md), [046-risk_treatment_plans](../04-Risk-Management/046-risk_treatment_plans.md))
2. Policy application and control effectiveness review
3. Domain risk escalations (cloud, medical device, third-party — [041-cloud_risk](../04-Risk-Management/041-cloud_risk.md), [042-medical_device_risk](../04-Risk-Management/042-medical_device_risk.md), [043-third_party_risks](../04-Risk-Management/043-third_party_risks.md))
4. Compliance status (CAF, ISO 27001, DSPT)
5. Open recommendations tracking, across all programme phases

## 5. Strategic Priorities

Priorities are drawn from the highest-priority open recommendations across the programme to date:

| Priority | Recommendation | Source | Owner | Target |
|---|---|---|---|---|
| P1 | Establish the Cyber Security Governance Group (this document) | [021-current_state_assessment](../03-Current-State-Assessment/021-current_state_assessment.md) REC-001 | CISO | Q3 2026 |
| P2 | Move Critical-rated risk treatments from "Planned" to "In Progress" | [021-current_state_assessment](../03-Current-State-Assessment/021-current_state_assessment.md) REC-002 | CISO / CDIO | Q3 2026 |
| P3 | Establish centralised supplier security assurance process | [021-current_state_assessment](../03-Current-State-Assessment/021-current_state_assessment.md) REC-004 | Procurement Director | Q4 2026 |
| P4 | Formally document Trust Board escalation threshold for Impact-5 risk acceptance | [047-risk_methodology](../04-Risk-Management/047-risk_methodology.md) REC-002 | CISO | Q3 2026 |
| P5 | Establish continuous risk intake route into the central register | [047-risk_methodology](../04-Risk-Management/047-risk_methodology.md) REC-001 | CISO | Q4 2026 |

## 6. Governance, Risk & Compliance Alignment

This strategy is the connective layer between the programme's assessment phases (03) and risk management phase (04) and its forward-looking phases: the CSGG chartered here is the forum that will operationalise treatment plans (04), review compliance mapping (07), oversee incident response governance (08), and receive security metrics reporting (13). Establishing it now — rather than deferring it to a later phase — directly addresses the root cause identified independently by [021-current_state_assessment](../03-Current-State-Assessment/021-current_state_assessment.md), [022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md), and [047-risk_methodology](../04-Risk-Management/047-risk_methodology.md): the absence of a standing operating rhythm.

## 7. Review & Next Steps

This strategy will be reviewed annually by the CSGG, or sooner if a material change in the Trust's risk profile or regulatory environment occurs. Immediate next steps: convene the first CSGG meeting within Q3 2026; ratify [052-roles_and_responsibilities](052-roles_and_responsibilities.md) and the three policies ([053-information_security_policy](053-information_security_policy.md), [054-access_control_policy](054-access_control_policy.md), [055-supplier_security_policy](055-supplier_security_policy.md)); and adopt the standing agenda in §4.2 from the first meeting onward.
