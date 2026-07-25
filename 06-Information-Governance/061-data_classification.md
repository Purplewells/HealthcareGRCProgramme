# Data Classification Framework

**Organisation:** Westbridge Hospitals Trust (WHT)  
**Document Type:** Data Classification Framework  
**Owner:** Data Protection Officer (DPO) / Information Governance Team  
**Version:** 1.0  



# 1. Purpose

The Data Classification Framework establishes how Westbridge Hospitals Trust identifies, categorises, and protects information based on its sensitivity, business value, and potential impact if disclosed, altered, or unavailable.

The framework supports:

- UK GDPR compliance.
- NHS Data Security and Protection Toolkit (DSPT) requirements.
- Information governance.
- Risk management.
- Access control decisions.
- Data handling practices.
- Security control selection.

The objective is to ensure that sensitive information receives appropriate protection throughout its lifecycle.



# 2. Scope

This framework applies to all information created, received, stored, processed, or shared by the Trust, including:

- Patient information.
- Staff information.
- Research data.
- Financial information.
- Operational records.
- Clinical system data.
- Digital communications.
- Third-party supplied information.

The framework applies to:

- Permanent employees.
- Contractors.
- Students.
- Researchers.
- Suppliers with access to Trust information.



# 3. Classification Principles

Information classification is based on three security principles:

## Confidentiality

Protecting information from unauthorised disclosure.

Examples:

- Patient records.
- Staff personal information.
- Research data.



## Integrity

Ensuring information remains accurate and is protected from unauthorised modification.

Examples:

- Medication records.
- Laboratory results.
- Clinical documentation.



## Availability

Ensuring information is accessible when required.

Examples:

- Electronic Patient Records.
- Emergency care systems.
- Diagnostic systems.



# 4. Data Classification Levels

The Trust uses four information classification levels.

| Classification | Description | Examples | Required Protection |
|---|---|---|---|
| Restricted | Highly sensitive information where unauthorised access could cause serious harm | Patient records, passwords, clinical research data | Strong access controls, encryption, monitoring |
| Confidential | Sensitive information requiring protection | Staff records, financial information, supplier contracts | Controlled access, secure storage |
| Internal | Information intended for Trust workforce use | Internal procedures, operational documents | Standard organisational controls |
| Public | Information approved for external release | Public reports, published guidance | Normal publication controls |



# 5. Restricted Information

## Definition

Restricted information is information where unauthorised access, disclosure, alteration, or loss could result in significant harm to individuals, patients, the Trust, or healthcare operations.

## Examples

- Electronic Patient Records (EPR).
- Medical diagnoses.
- Medication records.
- Laboratory results.
- Medical imaging.
- Mental health records.
- Genetic information.
- Clinical trial participant data.
- Authentication credentials.
- Security configurations.

## Security Requirements

Restricted information requires:

- Role-based access control.
- Multi-factor authentication where applicable.
- Encryption in transit and at rest.
- Audit logging.
- Regular access reviews.
- Secure disposal.
- Data sharing agreements.



# 6. Confidential Information

## Definition

Confidential information contains sensitive organisational or personal information where unauthorised disclosure could negatively affect individuals or Trust operations.

## Examples

- Employee records.
- Payroll information.
- HR documentation.
- Procurement information.
- Supplier contracts.
- Internal financial reports.
- Security assessments.

## Security Requirements

Confidential information requires:

- Controlled access.
- Approved storage locations.
- Secure transmission.
- Appropriate retention periods.
- Access monitoring.



# 7. Internal Information

## Definition

Internal information is intended for use by Trust employees and authorised partners but does not normally create significant harm if disclosed.

## Examples

- Internal procedures.
- Operational guidance.
- Staff communications.
- Training materials.
- Meeting documentation.

## Security Requirements

Internal information requires:

- Standard authentication.
- Appropriate sharing permissions.
- Protection from unauthorised external access.



# 8. Public Information

## Definition

Public information has been approved for external distribution.

## Examples

- Public website content.
- Annual reports.
- Published research.
- Patient information leaflets.

## Security Requirements

Public information requires:

- Approval before release.
- Accuracy verification.
- Version control.



# 9. Information Classification Examples

| Information Asset | Classification | Owner |
|---|---|---|
| Electronic Patient Records | Restricted | Clinical Information Asset Owner |
| Medical Images | Restricted | Radiology Director |
| Laboratory Results | Restricted | Pathology Director |
| Research Data | Confidential / Restricted | Research Director |
| Staff Records | Confidential | HR Director |
| Payroll Data | Confidential | Finance Director |
| Cyber Risk Register | Confidential | CISO |
| Security Policies | Internal | CISO |
| Public Website Content | Public | Communications Team |



# 10. Data Handling Requirements

## Storage

| Classification | Storage Requirements |
|---|---|
| Restricted | Approved clinical systems, encrypted storage, access controls |
| Confidential | Approved Trust systems and managed services |
| Internal | Trust-approved collaboration platforms |
| Public | Approved external publishing platforms |



## Sharing

Before sharing information:

- Confirm the recipient is authorised.
- Verify the purpose of sharing.
- Apply appropriate access restrictions.
- Use secure transfer methods.
- Maintain audit records where required.



## Printing

Sensitive information should:

- Only be printed when necessary.
- Be collected immediately from printers.
- Be securely disposed of.



## Disposal

Information must be disposed of using approved methods:

- Secure deletion.
- Confidential waste disposal.
- Certified destruction where required.



# 11. Data Ownership Responsibilities

| Role | Responsibility |
|---|---|
| Information Asset Owner (IAO) | Determines classification and acceptable use |
| Data Protection Officer | Provides privacy and regulatory guidance |
| System Owner | Implements technical controls |
| Cyber Security Team | Advises on protection requirements |
| Users | Handle information according to classification |



# 12. Relationship to Access Control

Information classification determines access requirements.

The Trust applies:

## Least Privilege

Users receive only the access required to perform their role.

## Need-to-Know

Access is granted based on legitimate business requirements.

## Role-Based Access Control (RBAC)

Permissions are aligned with job responsibilities.

Examples:

| Role | Access |
|---|---|
| Consultant Doctor | Assigned patient records |
| Nurse | Relevant patient care information |
| Administrator | Approved operational information |
| Researcher | Approved research datasets |
| IT Administrator | Technical systems, not clinical data by default |



# 13. Data Classification Risks

| Risk ID | Risk | Impact |
|---|---|---|
| DC-001 | Patient information incorrectly classified | Inadequate protection of sensitive data |
| DC-002 | Uncontrolled copies of reports | Increased data leakage risk |
| DC-003 | Excessive access to sensitive information | Confidentiality breach |
| DC-004 | Lack of ownership accountability | Poor governance |

---

# 14. Compliance Alignment

This framework supports:

| Requirement | Alignment |
|---|---|
| UK GDPR | Protection of personal and special category data |
| Data Protection Act 2018 | Lawful handling of personal information |
| NHS DSP Toolkit | Confidentiality, integrity, availability controls |
| ISO/IEC 27001 | Information classification and handling controls |
| NCSC CAF | Data protection and governance principles |



# 15. Review and Maintenance

The framework will be reviewed:

- Annually.
- Following major system changes.
- Following significant security incidents.
- Following regulatory changes.

Information owners are responsible for ensuring classifications remain accurate.



# 16. Expected Outcome

A mature data classification capability will enable the Trust to:

- Protect sensitive healthcare information.
- Apply appropriate security controls.
- Improve access management.
- Support compliance evidence.
- Reduce the likelihood of data breaches.
- Improve confidence in information governance.