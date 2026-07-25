# Access Control Policy

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Policy
**Owner:** Chief Information Security Officer (CISO)
**Version:** 1.0
**Effective Date:** 2026-07-23
**Review Date:** 2027-07-23

## 1. Purpose

This policy sets out WHT's requirements for granting, reviewing, and revoking access to information systems. It exists to directly address two related findings: CAF B2 Identity and Access Control, currently rated **Not Achieved** ([../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md)), and the identity single-point-of-failure observation in [../04-Risk-Management/041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §4.2, where Microsoft Entra ID underpins authentication for Microsoft 365, the Azure Cloud Environment, and all four patient-facing services rated Restricted/High criticality.

## 2. Scope

This policy applies to all access to WHT information systems, applications, and cloud services — clinical, corporate, and patient-facing — by staff, contractors, students, researchers, and third parties, across on-premises and cloud (Azure, Microsoft 365) environments.

## 3. Policy Statements

1. Access must be granted on the principle of least privilege and role-based access control, proportionate to the classification of the information or system involved ([../06-Information-Governance/041-data_classification](../06-Information-Governance/041-data_classification.md)).
2. All user accounts must be uniquely attributable to an individual; shared or generic accounts are prohibited except where formally risk-assessed and approved by the CISO.
3. Privileged and administrative access to Microsoft Entra ID, Microsoft 365, and the Azure Cloud Environment must be subject to enhanced controls (multi-factor authentication, conditional access, and privileged access review), reflecting Entra ID's role as the Trust's single control point for Restricted/High-criticality cloud services.
4. Access reviews must be conducted on a defined cycle for all clinical and corporate systems; excessive or unused privileges identified during review must be revoked, directly addressing CR-004 (Excessive user access privileges) in [risk_register](../04-Risk-Management/risk_register.md).
5. Access must be revoked or reviewed immediately upon a change of role, contract end, or departure, coordinated between the Service Desk and Information Asset Owners.
6. Segregation of duties must be enforced for high-risk functions (e.g. clinical system administration, financial systems, identity administration).
7. All access grants, reviews, and revocations must be logged and available for audit.
8. Any deviation from this policy required for clinical safety or operational continuity must be time-boxed, documented, and approved by the CISO or SIRO.

## 4. Roles & Responsibilities

Roles and accountabilities are defined in [052-roles_and_responsibilities](052-roles_and_responsibilities.md). Information Asset Owners are accountable for access decisions on their assets; the Service Desk executes access provisioning and revocation; the Cyber Security Team monitors for anomalous access; the CSGG reviews access review completion and outstanding privilege exposure monthly.

## 5. Compliance, Exceptions & Enforcement

Non-compliance is managed as set out in [053-information_security_policy](053-information_security_policy.md) §5. Given the criticality of identity as a single point of failure across the cloud estate, any exception affecting privileged or administrative access to Entra ID, Microsoft 365, or Azure must be approved by the CISO and reported to the CSGG at its next meeting.

## 6. Related Documents

- [053-information_security_policy](053-information_security_policy.md)
- [052-roles_and_responsibilities](052-roles_and_responsibilities.md)
- [022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) (CAF B2)
- [041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §4.2
- [risk_register](../04-Risk-Management/risk_register.md) (CR-002, CR-004)

## 7. Review

This policy is reviewed annually by the CISO and ratified by the CSGG, or sooner if an access-related security incident or a material change to the Trust's identity infrastructure occurs.
