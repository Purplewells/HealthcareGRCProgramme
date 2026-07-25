# Risk Methodology

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Risk Methodology (Authoritative)
**Owner:** Chief Information Security Officer (CISO)
**Version:** 1.0

## 1. Introduction

### 1.1 Purpose

This document is the authoritative definition of how WHT identifies, assesses, scores, treats, and reviews cyber risk. [risk_register](risk_register.md) §2-§3 summarises this methodology for readability within the register itself; where the two differ, this document governs. Every domain-specific risk assessment in this folder ([041-cloud_risk](041-cloud_risk.md), [042-medical_device_risk](042-medical_device_risk.md), [043-third_party_risks](043-third_party_risks.md), [044-threat_assessment](044-threat_assessment.md)) and the heat map and treatment plans ([045-risk_heat_map](045-risk_heat_map.md), [046-risk_treatment_plans](046-risk_treatment_plans.md)) apply this same methodology.

### 1.2 Scope

This methodology applies to all cyber security risk identification, assessment, and treatment activity across WHT, covering clinical, corporate, infrastructure, medical device, and third-party risk. It does not cover general enterprise risk (financial, clinical safety, workforce) managed through the Trust's separate corporate risk process, except where a cyber risk has a direct clinical safety consequence requiring escalation to that process.

## 2. Assessment Criteria

### 2.1 Framework(s) Applied

This methodology is a Likelihood × Impact model consistent with ISO 31000 risk management principles and calibrated to the Trust's risk appetite statement in [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §2.4.

### 2.2 Rating Scale

**Likelihood Scale**

| Score | Rating | Description |
|---|---|---|
| 1 | Rare | Unlikely to occur |
| 2 | Unlikely | Could occur occasionally |
| 3 | Possible | Realistic possibility |
| 4 | Likely | Expected to occur |
| 5 | Almost Certain | Highly probable |

**Impact Scale**

| Score | Rating | Description |
|---|---|---|
| 1 | Insignificant | Minimal operational impact |
| 2 | Minor | Limited disruption |
| 3 | Moderate | Service impact requiring management attention |
| 4 | Major | Significant operational or regulatory impact |
| 5 | Severe | Patient safety or major organisational impact |

**Risk Score** = Likelihood × Impact

| Score | Risk Level | Action |
|---|---|---|
| 1-4 | Low | Monitor |
| 5-9 | Medium | Manage through normal processes |
| 10-16 | High | Treatment required |
| 17-25 | Critical | Immediate action required |

## 3. Current State

The methodology is consistently applied within the central register ([risk_register](risk_register.md)) and has now been extended to four domain-specific assessments in this folder. Risk identification currently occurs primarily through programme-led review (this engagement) rather than a continuous, business-as-usual identification process — new risks are not yet systematically captured between formal review cycles. Risk ownership follows the principle that the person accountable for the business service or information asset owns the associated risk, with the Cyber Security Team providing assessment expertise, threat intelligence, and control guidance rather than owning risk acceptance decisions themselves.

## 4. Observations

### 4.1 Likelihood Inputs Should Draw on the Threat Assessment, Not Be Estimated in Isolation

Likelihood scoring is most defensible when informed by the threat actor Capability/Intent ratings in [044-threat_assessment](044-threat_assessment.md), rather than being estimated independently for each risk — this is now formalised as the intended process, but has not yet been applied retrospectively to re-validate the Likelihood scores already in [risk_register](risk_register.md).

### 4.2 Risk Appetite Directly Constrains Acceptance Decisions

The Trust's Low appetite for patient safety, clinical availability, and confidentiality risk ([../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §2.4) means Impact-5 risks cannot be formally "accepted" by a risk owner without Trust Board sign-off — this escalation threshold is implied by the risk appetite statement but not yet explicitly documented as a governance rule until this document.

### 4.3 No Continuous Risk Identification Process Exists Outside Formal Review Cycles

Risks are currently identified through periodic, programme-driven assessment rather than a standing process (e.g. a risk intake route from incident reports, vulnerability scans, or supplier notifications feeding directly into the register).

### 4.4 Domain-Specific Risk IDs (e.g. MDR-001, TPR-001) Are Not Yet Reconciled Into the Central Register

The domain assessments in this folder introduce sub-risk identifiers that provide useful granularity but currently exist alongside, rather than formally within, [risk_register](risk_register.md) — a reconciliation step is needed so the central register remains the single source of truth.

## 5. Evidence

| Evidence ID | Description | Source | Date | Linked Observation |
|---|---|---|---|---|
| EVD-001 | Risk appetite statement | [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §2.4 | 2026-07-23 | 4.2 |
| EVD-002 | Threat actor Capability/Intent ratings | [044-threat_assessment](044-threat_assessment.md) §4 | 2026-07-23 | 4.1 |
| EVD-003 | Domain-specific sub-risk identifiers | [042-medical_device_risk](042-medical_device_risk.md) §7, [043-third_party_risks](043-third_party_risks.md) §7 | 2026-07-23 | 4.4 |

## 6. Analysis

### 6.1 Findings

The methodology itself is sound and consistent with recognised risk management practice, but its application is currently periodic rather than continuous, and its outputs (the central register and the newer domain assessments) are not yet fully reconciled into one coherent structure. This is a governance execution gap rather than a methodology design gap.

### 6.2 Root Cause

The root cause is the same one identified Trust-wide in [../03-Current-State-Assessment/021-current_state_assessment](../03-Current-State-Assessment/021-current_state_assessment.md) §6.2: without a standing governance forum (the recommended Cyber Security Governance Group) meeting on a defined cycle, methodology exists as a documented standard but lacks the operational rhythm to be continuously applied and reconciled.

## 7. Risk Rating

| Risk ID | Description | Likelihood | Impact | Rating | Linked Observation |
|---|---|---|---|---|---|
| METH-001 | Risk register becomes stale between periodic reviews, understating actual exposure | 3 | 4 | High | 4.3 |
| METH-002 | Domain-specific and central risk views diverge over time without reconciliation | 3 | 3 | Medium | 4.4 |

## 8. Recommendations

| Recommendation ID | Recommendation | Priority | Owner | Target Timeframe |
|---|---|---|---|---|
| REC-001 | Establish a continuous risk intake route (incident reports, vulnerability scan results, supplier notifications) feeding directly into [risk_register](risk_register.md) | High | CISO | Q4 2026 |
| REC-002 | Formally document the Trust Board escalation threshold for accepting any Impact-5 risk, referencing the risk appetite statement | High | CISO | Q3 2026 |
| REC-003 | Reconcile domain-specific sub-risk identifiers (MDR-, TPR-) into the central register at the next scheduled review | Medium | CISO | Q1 2027 |
| REC-004 | Re-validate existing Likelihood scores in [risk_register](risk_register.md) against the Capability/Intent ratings in [044-threat_assessment](044-threat_assessment.md) | Medium | CISO | Q4 2026 |

## 9. Conclusion

WHT's risk methodology is fit for purpose and now consistently documented as the authoritative reference for every risk document in this programme. The priority is not to redesign the methodology but to operationalise it: moving from periodic, programme-driven risk assessment to a continuous process with a standing governance forum, and reconciling the newer domain-specific risk views into the single central register this document is intended to govern.
