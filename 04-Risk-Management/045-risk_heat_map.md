# Risk Heat Map

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Risk Heat Map
**Owner:** Chief Information Security Officer (CISO)
**Version:** 1.0

## 1. Introduction

### 1.1 Purpose

This document presents the Trust's 12 recorded cyber risks (CR-001 to CR-012) as a Likelihood × Impact heat map, for use in executive and Cyber Security Governance Group reporting where a single-page visual is more useful than the full [risk_register](risk_register.md) table.

### 1.2 Scope

This heat map covers all risks currently recorded in [risk_register](risk_register.md) §4. It is a derived visualisation, not a second source of truth — any discrepancy should be resolved in favour of the register.

## 2. Assessment Criteria

### 2.1 Framework(s) Applied

This heat map uses the Trust's standard risk methodology defined in [047-risk_methodology](047-risk_methodology.md): Likelihood (1-5) × Impact (1-5) = Risk Score, banded Low (1-4) / Medium (5-9) / High (10-16) / Critical (17-25).

### 2.2 Rating Scale

Cells are shaded by band: 🟩 Low, 🟨 Medium, 🟧 High, 🟥 Critical.

## 3. Current State

Every one of the Trust's 12 recorded risks sits at Impact 4 or 5 — reflecting that all currently tracked risks have a plausible path to patient safety, clinical service, or major regulatory consequence (per the Impact scale in [risk_register](risk_register.md) §3). The heat map is therefore concentrated in the top two rows, with variation driven almost entirely by Likelihood.

| Impact ↓ / Likelihood → | 1 (Rare) | 2 (Unlikely) | 3 (Possible) | 4 (Likely) | 5 (Almost Certain) |
|---|---|---|---|---|---|
| **5 (Severe)** | | | 🟧 CR-009, CR-010, CR-011, CR-012 | 🟥 CR-002, CR-003, CR-005, CR-006 | 🟥 CR-001 |
| **4 (Major)** | | | | 🟧 CR-004, CR-007, CR-008 | |
| **3 (Moderate)** | | | | | |
| **2 (Minor)** | | | | | |
| **1 (Insignificant)** | | | | | |

## 4. Observations

### 4.1 All Recorded Risks Cluster at High or Critical

No currently recorded risk falls below "High" — there are no Low or Medium entries on the heat map at all, which reflects the Trust's current practice of registering risks only once they reach a materially significant level, rather than maintaining a full-spectrum register including lower-rated risks.

### 4.2 One Risk Sits at the Extreme Corner of the Map

CR-001 (Ransomware affecting clinical services) is the only risk scored 5×5 (25), the maximum possible score, and is visually isolated in the top-right cell — the clearest single signal on the heat map for where to focus immediate attention.

### 4.3 The Critical Band is Dominated by External-Actor-Driven Risks

All four risks in the 🟥 Likelihood-4/Impact-5 cell (CR-002, CR-003, CR-005, CR-006) map directly to the threat actor categories described in [044-threat_assessment](044-threat_assessment.md) — credential theft, opportunistic exploitation, data leakage, and supply chain compromise.

### 4.4 The High Band (Likelihood-3/Impact-5) is Dominated by Control-Maturity Risks Rather Than Active Threats

CR-009, CR-010, CR-011, and CR-012 are lower Likelihood not because they are less severe, but because they describe capability gaps (monitoring, resilience, backup, cloud configuration) rather than a specific active threat vector — their Likelihood would rise quickly if a Critical-band risk in the same row were realised.

## 5. Evidence

| Evidence ID | Description | Source | Date | Linked Observation |
|---|---|---|---|---|
| EVD-001 | Full risk scoring table (CR-001 to CR-012) | [risk_register](risk_register.md) §4 | 2026-07-23 | 4.1, 4.2 |
| EVD-002 | Threat actor Capability/Intent ratings | [044-threat_assessment](044-threat_assessment.md) §4 | 2026-07-23 | 4.3 |

## 6. Analysis

### 6.1 Findings

The heat map's concentration in the top-right quadrant is not a scoring artefact — it reflects a genuinely under-controlled environment being assessed against a genuinely severe potential impact (patient safety and critical service disruption). The absence of any Low/Medium entries suggests the register would benefit from also tracking lower-rated risks, both for completeness and so that future risk movement (upward or downward) is visible on this map rather than only appearing when a risk first crosses the High threshold.

### 6.2 Root Cause

The clustering pattern is explained by the same root cause identified across this folder and [../03-Current-State-Assessment/](../03-Current-State-Assessment/): control maturity has not kept pace with the inherent severity of impact in a healthcare environment, so nearly every plausible risk scenario currently scores in the upper bands.

## 7. Risk Rating

| Risk ID | Description | Likelihood | Impact | Rating | Linked Observation |
|---|---|---|---|---|---|
| CR-001 | Ransomware affecting clinical services | 5 | 5 | Critical | 4.2 |
| CR-002 | Compromise of Microsoft 365 accounts | 4 | 5 | Critical | 4.3 |
| CR-003 | Unsupported medical devices exploited | 4 | 5 | Critical | 4.3 |
| CR-005 | Patient data exposure | 4 | 5 | Critical | 4.3 |
| CR-006 | Third-party supplier compromise | 4 | 5 | Critical | 4.3 |

## 8. Recommendations

| Recommendation ID | Recommendation | Priority | Owner | Target Timeframe |
|---|---|---|---|---|
| REC-001 | Treat CR-001 as the single highest-priority risk Trust-wide until its treatment plan moves from "In Progress" to embedded, given its unique 25/25 score | High | CDIO | Q3 2026 |
| REC-002 | Extend the risk register to include Low/Medium-rated risks so future heat maps show the full risk distribution, not only High/Critical entries | Medium | CISO | Q1 2027 |
| REC-003 | Re-publish this heat map at each quarterly Cyber Security Governance Group meeting to track movement | Medium | CISO | Ongoing, quarterly |

## 9. Conclusion

The heat map confirms visually what the risk register shows in tabular form: WHT's risk profile is currently concentrated at High and Critical, anchored by a single maximum-severity risk (CR-001, ransomware). This visualisation is intended for executive reporting; the detailed treatment status for each risk is maintained in [046-risk_treatment_plans](046-risk_treatment_plans.md), and the underlying scoring methodology in [047-risk_methodology](047-risk_methodology.md).
