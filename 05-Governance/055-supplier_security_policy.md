# Supplier Security Policy

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Policy
**Owner:** Procurement Director
**Version:** 1.0
**Effective Date:** 2026-07-23
**Review Date:** 2027-07-23

## 1. Purpose

This policy sets out WHT's requirements for assessing, contracting, and monitoring the security posture of third-party suppliers. It exists to close the systemic gap identified in [../04-Risk-Management/043-third_party_risks](../04-Risk-Management/043-third_party_risks.md): the Trust depends on more than 150 external suppliers but has no central process for assessing supplier security posture, embedding security requirements into contracts, or monitoring ongoing supplier risk ([../03-Current-State-Assessment/021-current_state_assessment](../03-Current-State-Assessment/021-current_state_assessment.md) §4.5).

## 2. Scope

This policy applies to all third-party suppliers, vendors, and service providers with access to WHT information, systems, or clinical infrastructure, including clinical software vendors, medical device manufacturers, cloud and productivity providers, and managed service providers, as recorded in the supplier register ([../02-Asset-Management/025-supplier_register.xlsx](../02-Asset-Management/025-supplier_register.xlsx)).

## 3. Policy Statements

1. All new suppliers with access to Trust information or systems must undergo a security assurance assessment before onboarding, proportionate to the criticality and data classification of the systems or information involved.
2. Contracts with suppliers handling Restricted or High-criticality information or systems must include defined security requirements and audit/assurance rights.
3. Supplier security assurance must be re-assessed at least annually, and status recorded and maintained in the supplier register.
4. Where a critical clinical system depends on a single named vendor with no documented fallback (e.g. the EPR, LIS, RIS/PACS, and Theatre Management System dependencies identified in [../04-Risk-Management/043-third_party_risks](../04-Risk-Management/043-third_party_risks.md) §4), a documented contingency or business continuity position must be established and reviewed as part of that supplier's assurance cycle.
5. Suppliers whose assurance status lapses or is not renewed on schedule (e.g. an "Approaching Renewal" or lapsed status) must be escalated to the CSGG and remediated before continued reliance is accepted, particularly where an underlying application is also on legacy or vendor-extended support.
6. Supplier-related risks must be recorded in the central [risk_register](../04-Risk-Management/risk_register.md) and, where applicable, the domain-specific view in [../04-Risk-Management/043-third_party_risks](../04-Risk-Management/043-third_party_risks.md).
7. Supplier security incidents or breaches affecting Trust data or systems must be reported immediately under the Trust's incident management process.

## 4. Roles & Responsibilities

Roles and accountabilities are defined in [052-roles_and_responsibilities](052-roles_and_responsibilities.md). The Procurement Director owns this policy and the supplier assurance process; the CISO provides risk assessment expertise and reviews supplier-related risk escalations; the CSGG reviews supplier assurance status and open supplier-related recommendations as a standing agenda item.

## 5. Compliance, Exceptions & Enforcement

Non-compliance is managed as set out in [053-information_security_policy](053-information_security_policy.md) §5. Continued reliance on a supplier with a lapsed or unresolved assurance status requires explicit, time-boxed approval from the CISO and Procurement Director, with the position and remediation plan reported to the CSGG until resolved — this directly applies to positions such as SUP-005 (Bluespier) / the Theatre Management System, per [../04-Risk-Management/043-third_party_risks](../04-Risk-Management/043-third_party_risks.md) REC-002.

## 6. Related Documents

- [053-information_security_policy](053-information_security_policy.md)
- [052-roles_and_responsibilities](052-roles_and_responsibilities.md)
- [043-third_party_risks](../04-Risk-Management/043-third_party_risks.md) (REC-001, REC-002)
- [025-supplier_register.xlsx](../02-Asset-Management/025-supplier_register.xlsx)
- [risk_register](../04-Risk-Management/risk_register.md) (CR-006)

## 7. Review

This policy is reviewed annually by the Procurement Director and ratified by the CSGG, or sooner following a supplier-related security incident or a material change to the Trust's supplier base.
