# Third-Party Risk Assessment

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Domain Risk Assessment — Third-Party / Supplier
**Owner:** Procurement Director
**Version:** 1.0

## 1. Introduction

### 1.1 Purpose

This assessment provides a focused, supplier-level view of cyber risk arising from WHT's third-party relationships, expanding on the single register-level entry CR-006 in [risk_register](risk_register.md). It answers: *which supplier relationships carry the highest cyber risk, and what assurance exists over them today?*

### 1.2 Scope

This assessment covers the 11 suppliers recorded in [../02-Asset-Management/025-supplier_register.xlsx](../02-Asset-Management/025-supplier_register.xlsx) (SUP-001 to SUP-011), spanning NHS Digital services, clinical software vendors, medical device suppliers, the Managed Security Service Provider, and Microsoft as cloud service provider. It does not cover contract commercial terms or procurement value-for-money considerations, which are managed through the Trust's standard procurement governance.

## 2. Assessment Criteria

### 2.1 Framework(s) Applied

This assessment uses the Trust's standard risk methodology defined in [047-risk_methodology](047-risk_methodology.md). It is also informed by NHS DSPT Standard 10 (Accountable Suppliers), assessed in [../03-Current-State-Assessment/024-dsp_toolkit_review](../03-Current-State-Assessment/024-dsp_toolkit_review.md), CAF principle A4 (Supply Chain), and ISO/IEC 27001:2022 controls A.5.19-A.5.23, all assessed as gaps in [../03-Current-State-Assessment/](../03-Current-State-Assessment/).

### 2.2 Rating Scale

Likelihood and Impact are each scored 1-5 per [risk_register](risk_register.md) §3; Risk Score = Likelihood × Impact, banded Low (1-4) / Medium (5-9) / High (10-16) / Critical (17-25).

## 3. Current State

WHT depends on more than 150 external suppliers Trust-wide ([../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.5), of which the 11 sampled in the supplier register represent the highest-criticality relationships: national NHS connectivity, the EPR and imaging platform vendors, medical device manufacturers, the MSSP, and Microsoft. Most sampled suppliers hold recognised security certifications (ISO 27001, DSPT "Standards Met", SOC 2 Type II), but there is no Trust-wide process that consistently requires, verifies, or re-checks this assurance on a defined cycle — assurance status is currently a by-product of individual relationship management rather than a governed control.

## 4. Observations

### 4.1 No Central Supplier Security Assurance Process Exists

There is no Trust-wide process for onboarding assessment, contractual security requirements, or periodic re-assessment of supplier security posture, despite the scale of third-party dependency. (Ref: [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.5)

### 4.2 One Sampled Supplier's Assurance Status is Approaching Renewal Without a Documented Successor Position

Bluespier International (SUP-005), which supports the Theatre Management System, is recorded with DSPT status "Approaching Renewal" and no documented contingency if renewal lapses, and the underlying application (Theatre Management System) is separately flagged as running on legacy vendor extended support. (Ref: [../02-Asset-Management/025-supplier_register.xlsx](../02-Asset-Management/025-supplier_register.xlsx) SUP-005; [../02-Asset-Management/023-application_portfolio.xlsx](../02-Asset-Management/023-application_portfolio.xlsx) APP-006)

### 4.3 Concentration Risk Exists Across Clinical Software Vendors

Four of the Trust's most critical clinical systems (EPR, LIS, RIS/PACS, Theatre Management) each depend on a single named vendor (Oracle Health, InterSystems, Sectra, Bluespier) with no documented fallback or business continuity position specific to vendor failure or extended vendor-side outage.

### 4.4 Medical Device Suppliers Carry Restricted Device Telemetry Without a Documented Data Processing Agreement Review Cycle

Siemens Healthineers, GE HealthCare, Philips, and Roche Diagnostics (SUP-006 to SUP-009) all have access to device telemetry classified Restricted, but no evidence was identified of a recurring data processing agreement or access review specific to this telemetry channel.

## 5. Evidence

| Evidence ID | Description | Source | Date | Linked Observation |
|---|---|---|---|---|
| EVD-001 | Supplier Register — 11 sampled suppliers, no central assurance process documented | [../02-Asset-Management/025-supplier_register.xlsx](../02-Asset-Management/025-supplier_register.xlsx) | 2026-07-23 | 4.1 |
| EVD-002 | SUP-005 Bluespier International — "Approaching Renewal" | [../02-Asset-Management/025-supplier_register.xlsx](../02-Asset-Management/025-supplier_register.xlsx) SUP-005 | 2026-07-23 | 4.2 |
| EVD-003 | APP-006 Theatre Management System — "Legacy - Vendor Extended Support" | [../02-Asset-Management/023-application_portfolio.xlsx](../02-Asset-Management/023-application_portfolio.xlsx) APP-006 | 2026-07-23 | 4.2 |
| EVD-004 | DSPT Standard 10 (Accountable Suppliers) — Not Met | [../03-Current-State-Assessment/024-dsp_toolkit_review](../03-Current-State-Assessment/024-dsp_toolkit_review.md) §3 | 2026-07-23 | 4.1 |
| EVD-005 | CAF A4 Supply Chain — Not Achieved | [../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) §3 | 2026-07-23 | 4.1 |

## 6. Analysis

### 6.1 Findings

The most acute finding is the compounding of two separate weaknesses in a single relationship: SUP-005 (Bluespier) has an approaching-renewal assurance status at the same time as its underlying application is on legacy vendor extended support. This is a materially higher-risk position than either weakness in isolation, and illustrates why supplier risk and asset/application risk need to be reviewed together rather than as separate registers.

### 6.2 Root Cause

The root cause mirrors the Trust-wide finding in [../03-Current-State-Assessment/021-current_state_assessment](../03-Current-State-Assessment/021-current_state_assessment.md) §6.2: suppliers were onboarded individually to meet operational and clinical need, with security assurance handled informally by the relevant relationship owner (e.g. Radiology Director, Pathology Director) rather than through a central, consistently-applied procurement security function.

## 7. Risk Rating

| Risk ID | Description | Likelihood | Impact | Rating | Linked Observation |
|---|---|---|---|---|---|
| CR-006 | Third-party supplier compromise | 4 | 5 | Critical | 4.1 |
| TPR-001 | Loss of Theatre Management System vendor support coinciding with assurance lapse | 3 | 4 | High | 4.2 |
| TPR-002 | Single-vendor concentration risk for critical clinical systems | 2 | 5 | Medium | 4.3 |
| TPR-003 | Unreviewed medical device telemetry data processing agreements | 2 | 4 | Medium | 4.4 |

## 8. Recommendations

| Recommendation ID | Recommendation | Priority | Owner | Target Timeframe |
|---|---|---|---|---|
| REC-001 | Establish a Trust-wide supplier security assurance process: onboarding assessment, contractual security clauses, and annual re-assessment | High | Procurement Director | Q4 2026 |
| REC-002 | Resolve SUP-005's assurance renewal and confirm a documented contingency position for the Theatre Management System | High | Theatre Manager / Procurement Director | Q3 2026 |
| REC-003 | Document business continuity fallback positions for single-vendor-dependent clinical systems (EPR, LIS, RIS/PACS) | Medium | CDIO | Q1 2027 |
| REC-004 | Introduce a recurring data processing agreement review cycle for medical device suppliers with telemetry access | Medium | Data Protection Officer / Clinical Engineering Manager | Q1 2027 |

## 9. Conclusion

Third-party risk at WHT is driven less by any single supplier's weakness than by the absence of a Trust-wide process to consistently assess and monitor supplier assurance over time — the same structural gap independently confirmed by CAF, ISO 27001, and DSPT. The most urgent, concrete action is resolving the compounded SUP-005/Theatre Management System position (REC-002), while REC-001 addresses the systemic gap that allowed this position to go unmanaged in the first place.
