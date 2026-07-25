# Medical Device Risk Assessment

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Domain Risk Assessment — Medical Devices
**Owner:** Clinical Engineering Manager
**Version:** 1.0

## 1. Introduction

### 1.1 Purpose

This assessment provides a focused, device-level view of cyber risk in the Trust's connected medical device estate, expanding on the single register-level entry CR-003 in [risk_register](risk_register.md). It answers: *which medical devices carry the highest cyber risk, and why?*

### 1.2 Scope

This assessment covers the 11 representative devices recorded in [../02-Asset-Management/024-medical_device_register.xlsx](../02-Asset-Management/024-medical_device_register.xlsx) (MD-001 to MD-011), spanning Radiology Imaging Devices (AST-020), Patient Monitoring Devices (AST-021), and Laboratory Analysis Equipment (AST-022). It does not cover the clinical safety or regulatory (MHRA) aspects of medical devices, which follow the Trust's separate medical device management process.

## 2. Assessment Criteria

### 2.1 Framework(s) Applied

This assessment uses the Trust's standard risk methodology defined in [047-risk_methodology](047-risk_methodology.md). It is also informed by NHS DSPT Standard 8 (Unsupported Systems), assessed in [../03-Current-State-Assessment/024-dsp_toolkit_review](../03-Current-State-Assessment/024-dsp_toolkit_review.md), and CAF principle B4 (System Security).

### 2.2 Rating Scale

Likelihood and Impact are each scored 1-5 per [risk_register](risk_register.md) §3; Risk Score = Likelihood × Impact, banded Low (1-4) / Medium (5-9) / High (10-16) / Critical (17-25).

## 3. Current State

Of the 11 devices sampled in the medical device register, 2 (MD-004 Legacy Mobile X-Ray Unit, MD-011 Legacy Microbiology Analyser) run vendor-unsupported operating systems (Windows 7 Embedded), and the Trust's business context records 25 such devices across the wider estate ([../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.4). All sampled devices are networked onto clinical or laboratory VLANs, meaning a compromise of any one device has a plausible path to other connected clinical systems unless network segmentation is robust. Devices rated Critical business criticality (MD-001, MD-002, MD-005, MD-006, MD-009, MD-010) are concentrated in radiology, critical care, and pathology — areas where an availability loss has the most direct patient safety consequence.

## 4. Observations

### 4.1 Unsupported Operating Systems Remain in Active Clinical Use

MD-004 and MD-011 run Windows 7 Embedded, for which the vendor no longer provides security patches, and both remain in active use in the Emergency Department and a pathology laboratory respectively. (Ref: [../02-Asset-Management/024-medical_device_register.xlsx](../02-Asset-Management/024-medical_device_register.xlsx) MD-004, MD-011)

### 4.2 Vendor Patching Dependency Limits the Trust's Own Remediation Options

Every device in the register depends on the manufacturer (Siemens Healthineers, GE HealthCare, Philips, B. Braun, Sysmex, Roche Diagnostics, bioMerieux) for firmware or OS updates — the Trust cannot independently patch clinical devices, meaning risk treatment is constrained to compensating network and access controls rather than direct remediation. (Ref: [../02-Asset-Management/025-supplier_register.xlsx](../02-Asset-Management/025-supplier_register.xlsx) SUP-006 to SUP-009)

### 4.3 Wireless-Connected Infusion Pumps Introduce a Distinct Attack Surface

MD-007 (Infusomat Space infusion pumps) connect over Wi-Fi to the clinical VLAN, which is a materially different and typically higher-risk connectivity pattern than the wired connections used by imaging and monitoring equipment, and warrants its own compensating controls (e.g. dedicated wireless segmentation, rogue access point detection).

### 4.4 Critical-Rated Devices Are Concentrated in Areas with Direct Patient Safety Impact

Six of eleven sampled devices are rated Critical business criticality, all located in radiology, critical care, and pathology — the same clinical areas the Trust's risk appetite statement identifies as Low tolerance for availability loss. (Ref: [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §2.4)

## 5. Evidence

| Evidence ID | Description | Source | Date | Linked Observation |
|---|---|---|---|---|
| EVD-001 | MD-004, MD-011 flagged "Unsupported - Risk Accepted" | [../02-Asset-Management/024-medical_device_register.xlsx](../02-Asset-Management/024-medical_device_register.xlsx) | 2026-07-23 | 4.1 |
| EVD-002 | 25 devices Trust-wide identified running unsupported operating systems | [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.4 | 2026-07-23 | 4.1 |
| EVD-003 | Supplier Register — medical device suppliers and assurance status | [../02-Asset-Management/025-supplier_register.xlsx](../02-Asset-Management/025-supplier_register.xlsx) | 2026-07-23 | 4.2 |
| EVD-004 | MD-007 Wi-Fi connected infusion pump | [../02-Asset-Management/024-medical_device_register.xlsx](../02-Asset-Management/024-medical_device_register.xlsx) MD-007 | 2026-07-23 | 4.3 |
| EVD-005 | DSPT Standard 8 (Unsupported Systems) — Not Met | [../03-Current-State-Assessment/024-dsp_toolkit_review](../03-Current-State-Assessment/024-dsp_toolkit_review.md) §3 | 2026-07-23 | 4.1 |

## 6. Analysis

### 6.1 Findings

Medical device risk at WHT is structurally different from general IT risk because remediation is vendor-gated rather than Trust-controlled. This means the standard treatment options available elsewhere in the estate (patch, upgrade, replace on a Trust-driven timeline) are not directly available here — risk treatment must rely on network segmentation, access control, and monitoring as compensating controls until device replacement is financially and operationally feasible.

### 6.2 Root Cause

The root cause is the long operational lifecycle of clinical equipment relative to IT refresh cycles: medical devices are procured and depreciated over 7-15 year horizons, while the security support lifecycle of their embedded operating systems is typically 5-10 years, creating a structural window where devices remain clinically serviceable but technically unsupported. This is compounded by incomplete historical ownership records, which the Trust's asset management improvement work ([../02-Asset-Management/](../02-Asset-Management/)) has now substantially addressed for the sampled devices.

## 7. Risk Rating

| Risk ID | Description | Likelihood | Impact | Rating | Linked Observation |
|---|---|---|---|---|---|
| CR-003 | Unsupported medical devices exploited | 4 | 5 | Critical | 4.1 |
| MDR-001 | Wireless infusion pump compromise via clinical Wi-Fi | 3 | 5 | High | 4.3 |
| MDR-002 | Vendor patching delay leaves known vulnerabilities unremediated | 3 | 4 | High | 4.2 |

## 8. Recommendations

| Recommendation ID | Recommendation | Priority | Owner | Target Timeframe |
|---|---|---|---|---|
| REC-001 | Complete a Trust-wide vulnerability assessment of all 25 unsupported devices and produce a prioritised replacement/compensating-control plan | High | Clinical Engineering Manager | Q4 2026 |
| REC-002 | Implement dedicated network segmentation isolating MD-004 and MD-011 from the general clinical VLAN pending replacement | High | Infrastructure Manager | Q3 2026 |
| REC-003 | Deploy dedicated wireless segmentation and rogue access point monitoring for Wi-Fi-connected devices such as MD-007 | Medium | Infrastructure Manager | Q1 2027 |
| REC-004 | Embed a security clause requiring timely vulnerability disclosure and patch commitments into medical device supplier contracts | Medium | Procurement Director / Clinical Engineering Manager | Q4 2026 |

## 9. Conclusion

Medical device risk at WHT is concentrated in two named legacy devices (MD-004, MD-011) but reflects a structural, Trust-wide pattern of 25 unsupported devices whose remediation is vendor-gated. Since direct patching is not available, network segmentation (REC-002) is the highest-priority compensating control and should be implemented ahead of the longer device replacement programme. This assessment's findings feed directly into DSPT Standard 8 evidence requirements ([../03-Current-State-Assessment/024-dsp_toolkit_review](../03-Current-State-Assessment/024-dsp_toolkit_review.md)) and the Trust-wide risk register entry CR-003.
