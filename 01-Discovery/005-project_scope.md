# Project Scope

**Project:** Project SentinelCare - Cyber Security Governance, Risk and Compliance Improvement Programme
**Document Type:** Project Scope
**Version:** 1.0

# 1. Purpose

This document defines the boundaries of the Project SentinelCare Discovery phase: what is assessed, what is not, and against which frameworks. It exists to prevent scope ambiguity between this Discovery phase and any later remediation or implementation phase.

# 2. In Scope

## 2.1 Organisational Scope

- Westbridge Hospitals Trust (WHT) corporate, clinical, and digital functions as described in [002-organisation_profile](002-organisation_profile.md).
- All Trust sites: two acute hospitals, three community healthcare centres, and associated diagnostic, pharmacy, and research facilities.
- Staff groups covered by the assessment's governance and awareness elements: clinical staff, administrative employees, contractors, students and researchers.

## 2.2 Technology and System Scope

Drawing on the digital environment inventory in [002-organisation_profile](002-organisation_profile.md):

- Clinical systems: EPR, LIS, RIS, PACS, Pharmacy Management System, Theatre Management System.
- Patient-facing services: online patient portal, appointment booking platform, remote consultation services, patient messaging.
- Corporate systems: Microsoft 365, finance and procurement, HR and payroll, learning management platform.
- Infrastructure: hybrid cloud environment (including Azure workloads), on-premises data centres, clinical network infrastructure, medical devices connected to clinical networks.
- Third-party healthcare applications, to the extent the Trust holds security or contractual responsibility for their configuration and access.

## 2.3 Framework Scope

The assessment evaluates current practice against:

- NCSC Cyber Assessment Framework (CAF) — full set of Objectives A–D.
- ISO/IEC 27001:2022 — control mapping at Annex A level, not a certification audit.
- NHS Data Security and Protection Toolkit (DSPT) — evidence areas mapped for readiness, not submitted.

## 2.4 Governance Domains

Governance, risk management, asset management, identity and access management, data protection, incident response, supplier security, security monitoring, business continuity, and security culture — consistent with the assessment approach in [001-executive_brief](001-executive_brief.md), Section 9.

# 3. Out of Scope

- **Live technical testing.** No penetration testing, vulnerability scanning, or red-team activity is performed as part of this Discovery phase (see constraint C-007/C-008 in [007-assumptions_and_constraints](007-assumptions_and_constraints.md)).
- **Remediation delivery.** Implementation of controls, policy rollout, and technical fixes are addressed in a subsequent delivery phase, not Discovery.
- **Third-party-hosted systems where the Trust is not the data controller.** Systems wholly owned and operated by external partners, where WHT has no security or configuration responsibility, are excluded, though supplier assurance of these relationships (O-05 in [004-project_objectives](004-project_objectives.md)) is in scope.
- **Formal DSPT submission or ISO 27001 certification.** The assessment informs readiness for both but does not constitute either.
- **Clinical research systems operating under separate sponsor governance**, where WHT acts as a host rather than data controller.

# 4. Time Boundary

This document governs the Discovery phase only. Discovery establishes the current-state baseline, risk register, and governance documentation set; it does not extend into ongoing operational security management, which would be governed under business-as-usual security operations once the programme's initial improvements are embedded.

# 5. Relationship to Other Documents

- Objectives assessed within this scope are set out in [004-project_objectives](004-project_objectives.md).
- Assumptions and constraints affecting how this scope is assessed are set out in [007-assumptions_and_constraints](007-assumptions_and_constraints.md).
- Stakeholders engaged within this scope are set out in [006-stakeholders](006-stakeholders.md).
