# Digital Asset Estate

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Asset Management Overview
**Owner:** Chief Information Security Officer (CISO)
**Version:** 1.1

# 1. Purpose

This document provides a narrative overview of the Trust's asset management approach. The detailed, authoritative asset inventory is maintained in [022-master_assets_register.xlsx](022-master_assets_register.xlsx) — this document should not be treated as a second copy of that data, but as the supporting context for how it is structured, governed, and used.

The asset register supports:

- Cyber risk management.
- Information security governance.
- Regulatory compliance.
- Incident response.
- Vulnerability management.
- Business continuity planning.
- Ownership and accountability.

# 2. Asset Management Principles

The Trust applies the following principles:

- All critical assets must have an identified owner.
- Assets must be classified according to business criticality.
- Sensitive information must have appropriate protection.
- Unsupported assets must be identified and risk assessed.
- Asset information must be regularly reviewed.
- Changes to assets must follow approved change management processes.

# 3. Classification Schemes Used in the Register

## Business Criticality

| Rating | Description |
|---|---|
| Critical | Loss of asset could impact patient safety or essential healthcare services |
| High | Loss could significantly affect clinical or operational services |
| Medium | Loss could cause operational disruption |
| Low | Limited business impact |

## Information Classification

| Classification | Description |
|---|---|
| Restricted | Highly sensitive information requiring strict controls |
| Confidential | Sensitive information requiring protection |
| Internal | Information intended for Trust workforce use |
| Public | Approved information for external release |

# 4. Asset Estate Summary

The register in [022-master_assets_register.xlsx](022-master_assets_register.xlsx) records 35 assets (AST-001 to AST-035) across eight categories:

| Category | Asset Count | Examples |
|---|---:|---|
| Clinical System | 6 | EPR, LIS, RIS, PACS, Pharmacy Management System, Theatre Management System |
| Patient-Facing Service | 4 | Patient Portal, Appointment Booking, Remote Consultation, Patient Messaging |
| Corporate Application | 4 | Microsoft 365, Finance System, HR and Payroll, Learning Management Platform |
| Infrastructure | 5 | Core Network, On-Premises Data Centres, Azure Cloud Environment, Backup Infrastructure, Security Monitoring Platform |
| Medical Device | 3 | Radiology Imaging Devices, Patient Monitoring Devices, Laboratory Analysis Equipment |
| Data Asset | 6 | Patient Records Data, Medical Imaging Data, Laboratory Results Data, Research Data, Staff Records, Financial Data |
| Identity and Access | 3 | Microsoft Entra ID, Privileged Accounts, Clinical User Accounts |
| Third-Party Service | 4 | NHS Digital Services, Clinical Software Vendors, Medical Device Suppliers, Managed Security Service Provider |

The majority of clinical, patient-facing, and medical device assets are rated Restricted / Critical, reflecting their direct link to patient safety and care delivery, consistent with the Trust's risk appetite set out in [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md).

# 5. Asset Ownership Model

| Asset Category | Responsible Owner |
|---|---|
| Patient Information | Information Asset Owner |
| Clinical Systems | Clinical Service Owner |
| Infrastructure | Infrastructure Manager |
| Cloud Services | Cloud Service Owner |
| Medical Devices | Clinical Engineering Manager |
| Employee Data | HR Director |
| Security Systems | CISO |
| Supplier Services | Procurement Director |

Individual asset owners are recorded against each asset in the register rather than repeated here.

# 6. Asset Management Risks

| Risk ID | Risk | Impact |
|---|---|---|
| AM-001 | Unknown assets may remain unmanaged | Increased vulnerability exposure |
| AM-002 | Inaccurate ownership information | Delayed risk decisions and incident response |
| AM-003 | Legacy assets may remain unsupported | Increased cyber attack risk |
| AM-004 | Unclassified information assets | Poor security control selection |

# 7. Asset Review Requirements

| Activity | Frequency |
|---|---|
| Critical asset review | Quarterly |
| User access review | Quarterly |
| Medical device inventory review | Quarterly |
| Full asset register review | Annually |
| Asset changes | Following approved change processes |

# 8. Expected Outcome

A mature asset management capability will enable the Trust to:

- Understand its technology estate.
- Identify critical services.
- Assign accountability.
- Improve vulnerability management.
- Support incident response.
- Demonstrate compliance with NHS and ISO security requirements.

# 9. Relationship to Other Documents

- Authoritative asset data: [022-master_assets_register.xlsx](022-master_assets_register.xlsx).
- Critical asset summary (derived from the register): `critical_assets.md`.
- Domain-specific extracts: `application_portfolio.xlsx`, `medical_device_register.xlsx`, `supplier_register.xlsx`.
- Risk treatment of asset-related findings: `04-Risk-Management`.
