# Critical Asset Summary

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Critical Asset Summary (Derived Extract)
**Owner:** Chief Information Security Officer (CISO)
**Version:** 1.0

# 1. Purpose

This document summarises the assets rated **Critical** business criticality in the authoritative asset inventory, [022-master_assets_register.xlsx](022-master_assets_register.xlsx). It is a derived extract for quick reference in risk, resilience, and incident response discussions — not a second source of truth. Any discrepancy between this summary and the register should be resolved in favour of the register.

18 of the 35 assets in the register (AST-001 to AST-035) are rated Critical, reflecting their direct link to patient safety, clinical service continuity, or the confidentiality of highly sensitive information, consistent with the Trust's risk appetite set out in [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md).

# 2. Critical Assets by Category

## Clinical Systems

| Asset ID | Asset Name | Owner | Information Classification |
|---|---|---|---|
| AST-001 | Electronic Patient Record (EPR) | Chief Medical Officer | Restricted |
| AST-002 | Laboratory Information System (LIS) | Pathology Director | Restricted |
| AST-003 | Radiology Information System (RIS) | Radiology Director | Restricted |
| AST-004 | Picture Archiving and Communication System (PACS) | Radiology Director | Restricted |
| AST-005 | Pharmacy Management System | Pharmacy Director | Restricted |

## Infrastructure

| Asset ID | Asset Name | Owner | Information Classification |
|---|---|---|---|
| AST-015 | Core Network Infrastructure | Infrastructure Manager | Internal |
| AST-016 | On-Premises Data Centres | Infrastructure Manager | Confidential |
| AST-017 | Azure Cloud Environment | Cloud Service Owner | Confidential |
| AST-018 | Backup Infrastructure | Infrastructure Manager | Confidential |

## Medical Devices

| Asset ID | Asset Name | Owner | Information Classification |
|---|---|---|---|
| AST-020 | Radiology Imaging Devices | Clinical Engineering Manager | Restricted |
| AST-021 | Patient Monitoring Devices | Clinical Engineering Manager | Restricted |
| AST-022 | Laboratory Analysis Equipment | Clinical Engineering Manager | Restricted |

## Data Assets

| Asset ID | Asset Name | Owner | Information Classification |
|---|---|---|---|
| AST-023 | Electronic Patient Records Data | Information Asset Owner | Restricted |
| AST-024 | Medical Imaging Data | Radiology Director | Restricted |
| AST-025 | Laboratory Results Data | Pathology Director | Restricted |

## Identity and Access

| Asset ID | Asset Name | Owner | Information Classification |
|---|---|---|---|
| AST-029 | Microsoft Entra ID | Identity Manager | Confidential |
| AST-030 | Privileged Accounts | CISO | Restricted |

## Third-Party Service

| Asset ID | Asset Name | Owner | Information Classification |
|---|---|---|---|
| AST-032 | NHS Digital Services | CDIO | Restricted |

# 3. Why These Assets Matter

- **Clinical systems** (AST-001 to AST-005) directly support diagnosis, treatment, and medication safety — loss of availability has an immediate patient safety impact.
- **Infrastructure** (AST-015 to AST-018) underpins every other system in the estate; compromise or outage has the broadest blast radius across the Trust.
- **Medical devices** (AST-020 to AST-022) are connected to clinical networks and directly involved in patient diagnosis and monitoring, and include devices identified as running unsupported operating systems (see [024-medical_device_register.xlsx](024-medical_device_register.xlsx)).
- **Data assets** (AST-023 to AST-025) represent the highly sensitive patient information the Trust is obligated to protect under UK GDPR, the NHS Data Security and Protection Toolkit (DSPT), and its duty of confidentiality to patients.
- **Identity and access** (AST-029, AST-030) are the control point for all other access in the estate — compromise of Entra ID or privileged accounts would enable broad, cross-system impact.
- **NHS Digital Services** (AST-032) provides national connectivity (e.g. Spine, PDS, e-Referral Service) that clinical workflows depend on and that the Trust does not directly control.

# 4. Relationship to Other Documents

- Authoritative asset data: [022-master_assets_register.xlsx](022-master_assets_register.xlsx).
- Narrative context and classification schemes: [021-digital_asset_estate](021-digital_asset_estate.md).
- Domain-specific extracts: [023-application_portfolio.xlsx](023-application_portfolio.xlsx), [024-medical_device_register.xlsx](024-medical_device_register.xlsx), [025-supplier_register.xlsx](025-supplier_register.xlsx).
- Risk treatment of asset-related findings: `04-Risk-Management`.
