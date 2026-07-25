# Data Lineage Assessment

**Organisation:** Westbridge Hospitals Trust (WHT)  
**Document Type:** Data Lineage Assessment  
**Owner:** Data Protection Officer (DPO) / Information Governance Team  
**Version:** 1.0  



# 1. Purpose

The Data Protection Impact Assessment ([062-data_protection_impact_assessment](062-data_protection_impact_assessment.md) §9) traces data flow for a single platform — the Patient Portal and Healthcare Interoperability Platform. This Data Lineage Assessment extends that view into a full source-to-destination lineage across the Trust's wider digital estate: which system originates each category of data, which systems consume it downstream, and where it crosses into third-party hands.

The objective is to establish system-of-record clarity, so that data quality, retention, and access decisions can be traced back to an authoritative source rather than to whichever copy is most convenient.



# 2. Scope

This assessment covers data lineage across the systems recorded in the master asset register ([../02-Asset-Management/022-master_assets_register.xlsx](../02-Asset-Management/022-master_assets_register.xlsx), 35 assets) and application portfolio ([../02-Asset-Management/023-application_portfolio.xlsx](../02-Asset-Management/023-application_portfolio.xlsx), 14 applications), focusing on the core clinical and patient-facing systems already identified as Critical or Restricted elsewhere in the programme.

It does not cover lineage for corporate/administrative systems outside the clinical and patient data path, or research data governed under separate sponsor arrangements ([../01-Discovery/005-project_scope](../01-Discovery/005-project_scope.md)).



# 3. Methodology

Lineage was traced using three inputs:

- **System-of-record designation** — for each data domain, identifying the single system treated as authoritative, consistent with the Information Asset Owner model in [061-data_classification](061-data_classification.md) §11.
- **Data provenance** — where a data item is first captured or generated (e.g. patient demographics captured at EPR registration).
- **Transformation and exchange points** — where data crosses a system, application, or organisational boundary, drawing on the data flow diagrams in [Data_Flow_Diagrams/](Data_Flow_Diagrams/).

This is a desk-based lineage exercise consistent with the rest of Project SentinelCare's programme-led assessment approach ([../04-Risk-Management/047-risk_methodology](../04-Risk-Management/047-risk_methodology.md) §3) rather than an automated data-catalogue discovery exercise.



# 4. System-of-Record Register

| Data Domain | System of Record | Downstream Consumers | Classification |
|---|---|---|---|
| Patient demographics, admissions, clinical notes | Electronic Patient Record (EPR) | LIS, RIS/PACS, Pharmacy Management System, Theatre Management System, Patient Portal | Restricted |
| Laboratory test orders and results | Laboratory Information System (LIS) | EPR, Clinical Users | Restricted |
| Diagnostic imaging and reports | Radiology Information System / PACS (RIS/PACS) | EPR, Clinical Users | Restricted |
| Medication and prescribing records | Pharmacy Management System | EPR, Clinical Users | Restricted |
| Theatre scheduling and procedure records | Theatre Management System | EPR, Clinical Users | Restricted |
| Patient-facing appointments and messaging | Patient Communication Services (via FHIR API Integration Layer) | Patient Portal, EPR | Restricted |
| Cyber risk data | Cyber Risk Register ([../04-Risk-Management/risk_register](../04-Risk-Management/risk_register.md)) | CSGG, Audit and Risk Committee | Confidential |
| Employee and payroll records | HR / Payroll Systems | Finance, HR | Confidential |

The EPR is the Trust's designated system of record for patient demographics: every other clinical system receives demographic data from the EPR and returns domain-specific results to it (see [Data_Flow_Diagrams/003-core_clinical_systems_data_flow](Data_Flow_Diagrams/003-core_clinical_systems_data_flow.md)).



# 5. Data Lineage Maps

The following standalone, colour-coded diagrams together form the Trust's data lineage map. Colour is applied consistently across all four using `classDef` styling in Mermaid, based on the classification levels defined in [061-data_classification](061-data_classification.md) §4:

- 🔴 **Restricted** (red, `#f8d7da`) — patient and clinical data
- 🟠 **Confidential** (amber, `#fff3cd`) — sensitive organisational data
- 🔵 **Internal** (blue, `#cfe2ff`) — security, monitoring, and audit data
- 🟢 **Public** (green) — approved for external release (not present in these flows)
- ⚪ **External Actor** (grey, `#e2e3e5`) — outside the Trust's classification scheme (patients, suppliers)

| Diagram | Covers |
|---|---|
| [Data_Flow_Diagrams/001-patient_portal_data_flow](Data_Flow_Diagrams/001-patient_portal_data_flow.md) | Patient Portal end-to-end system flow |
| [Data_Flow_Diagrams/002-patient_portal_trust_boundary](Data_Flow_Diagrams/002-patient_portal_trust_boundary.md) | Patient Portal trust boundary / zone model |
| [Data_Flow_Diagrams/003-core_clinical_systems_data_flow](Data_Flow_Diagrams/003-core_clinical_systems_data_flow.md) | EPR ↔ LIS ↔ RIS/PACS ↔ Pharmacy ↔ Theatre Management exchange |
| [Data_Flow_Diagrams/004-third_party_data_exchange](Data_Flow_Diagrams/004-third_party_data_exchange.md) | Trust ↔ vendor and Trust ↔ MSSP data exchange |



# 6. Cross-Border / Third-Party Data Flows

Four of the Trust's core clinical systems depend on a single named third-party vendor for support and maintenance access, consistent with [../04-Risk-Management/043-third_party_risks](../04-Risk-Management/043-third_party_risks.md) §4:

| System | Vendor | Lineage Implication |
|---|---|---|
| Electronic Patient Record (EPR) | Oracle Health | Vendor holds maintenance access to the Trust's system of record for patient demographics |
| Laboratory Information System (LIS) | InterSystems | Vendor holds maintenance access to laboratory result data |
| Radiology Information System / PACS | Sectra | Vendor holds maintenance access to diagnostic imaging data |
| Theatre Management System | Bluespier International (SUP-005) | Vendor holds maintenance access to theatre scheduling and procedure data; assurance status "Approaching Renewal" while the application itself is on legacy vendor-extended support ([../04-Risk-Management/043-third_party_risks](../04-Risk-Management/043-third_party_risks.md) TPR-001) |

See [Data_Flow_Diagrams/004-third_party_data_exchange](Data_Flow_Diagrams/004-third_party_data_exchange.md) for the visual representation of these flows.



# 7. Risks

| Risk ID | Risk | Impact |
|---|---|---|
| DL-001 | No system formally designated as system of record outside the EPR/clinical estate (e.g. cyber risk data, HR data), risking divergent copies | Data quality and accountability gaps |
| DL-002 | Lineage across vendor maintenance access points is not independently monitored, relying on vendor-reported activity | Reduced visibility of third-party data handling |
| DL-003 | Domain-specific data lineage (this document) is not yet reconciled with the master asset register on a routine cycle | Lineage map may become stale as the digital estate changes |



# 8. Compliance Alignment

This assessment supports:

| Requirement | Alignment |
|---|---|
| UK GDPR | Demonstrates accountability for the origin and movement of personal data (Article 5(2)) |
| NHS DSP Toolkit | Evidences understanding of data flows into and out of the Trust |
| ISO/IEC 27001 | Supports asset and information flow documentation controls |
| NCSC CAF | Data protection and governance principles (A3) |



# 9. Review and Maintenance

This assessment is reviewed annually by the DPO, or sooner following a significant change to the digital estate (new system onboarding, vendor change, or system decommissioning). Updates must be reflected consistently in the diagrams under [Data_Flow_Diagrams/](Data_Flow_Diagrams/) and cross-checked against the master asset register.
