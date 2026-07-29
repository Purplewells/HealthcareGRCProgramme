# Cyber Security Governance, Risk and Compliance Assessment

## Project SentinelCare

### Cyber Security Governance, Risk and Compliance Assessment and Improvement Programme**

# 1. Organisation Overview

### Organisation Name : **Westbridge Hospitals Trust (WHT)** *(Fictional)*

## Organisation Profile

Westbridge Hospitals Trust is a large NHS healthcare provider delivering acute and specialist healthcare services across the West Midlands region.

The Trust operates:

* Two acute hospitals
* Three community healthcare centres
* Specialist cancer treatment services
* Emergency department
* Diagnostic imaging services
* Pathology laboratories
* Pharmacy services
* Research and clinical trials facilities

The Trust employs approximately:

* 8,500 staff
* 1,200 clinicians
* 1,000 administrative employees
* 300 contractors
* 400 students and researchers

The organisation provides healthcare services to approximately:

* 850,000 patients annually
* 2.5 million outpatient appointments
* 180,000 emergency admissions


# 2. Digital Environment

The Trust has undergone significant digital transformation over the past five years.

Its technology environment includes:

## Clinical Systems

* Electronic Patient Record (EPR)
* Laboratory Information System (LIS)
* Radiology Information System (RIS)
* Picture Archiving and Communication System (PACS)
* Pharmacy Management System
* Theatre Management System

## Patient-Facing Services

* Online patient portal
* Appointment booking platform
* Remote consultation services
* Patient messaging system

## Corporate Systems

* Microsoft 365
* Finance and procurement systems
* HR and payroll systems
* Learning management platform

## Infrastructure

* Hybrid cloud environment
* Azure workloads
* On-premises data centres
* Medical devices connected to clinical networks
* Third-party healthcare applications


# 3. Current Cybersecurity Situation

The Trust Board has become increasingly concerned about cybersecurity risks following several incidents affecting healthcare organisations nationally.

Recent events include:

### Incident 1 — Phishing Attack

A senior clinician received a sophisticated phishing email appearing to come from Microsoft.

The attacker attempted to obtain:

* Microsoft 365 credentials
* Multi-factor authentication approval

The attack was detected by the security team, but investigation revealed that:

* Security awareness training completion was below target.
* Some staff had not completed phishing simulation exercises.


### Incident 2 — Legacy Medical Systems

A security review identified:

* 25 medical devices running unsupported operating systems.
* Limited vendor patching capability.
* Inconsistent asset ownership records.

The devices support:

* Radiology imaging
* Patient monitoring
* Laboratory analysis


### Incident 3 — Third-Party Supplier Risk

The Trust uses more than 150 external suppliers.

A recent review identified:

* No central supplier security assessment process.
* Inconsistent contract security requirements.
* Limited visibility of supplier access privileges.


### Incident 4 — Data Governance Concern

An internal audit identified:

* Excessive access permissions.
* Inconsistent patient data classification.
* Multiple copies of patient reports stored outside approved systems.


# 4. Cybersecurity Maturity Assessment

An initial assessment against the **NCSC Cyber Assessment Framework (CAF)** identified weaknesses:

| Area                | Current State                           |
| ------------------- | --------------------------------------- |
| Governance          | Policies exist but are inconsistent     |
| Risk Management     | No central cyber risk register          |
| Asset Management    | Incomplete asset inventory              |
| Identity Management | Excessive user privileges               |
| Incident Response   | Plan exists but not regularly tested    |
| Supplier Security   | Limited assurance process               |
| Security Culture    | Awareness training requires improvement |
| Monitoring          | Limited security metrics                |

Taken together, these findings indicate the Trust sits at an early/developing level of maturity (broadly Level 1–2 on the maturity scale in Section 10) across most CAF outcomes, with no area yet at a consistently Defined or Managed level. This is a starting-point assessment rather than a final position — the Discovery phase exists to establish an evidenced baseline before target maturity levels are agreed with the Board.

## Incident-to-CAF Mapping

| Incident | Primary CAF Objective Affected |
| --- | --- |
| 1 — Phishing Attack | C. Detecting Cyber Security Events; A. Managing Security Risk (security culture) |
| 2 — Legacy Medical Systems | A. Managing Security Risk (asset management) |
| 3 — Third-Party Supplier Risk | A. Managing Security Risk (supply chain) |
| 4 — Data Governance Concern | B. Protecting Against Cyber Attack (data security) |

## Risk Appetite

The Trust's risk appetite is defined in [003-business-context](003-business-context.md) and should be read alongside this maturity assessment: broadly, the Trust has low tolerance for risks affecting patient safety or clinical service availability, and comparatively greater tolerance for risk in non-critical corporate functions.


# 5. Regulatory and Compliance Context

The Trust must demonstrate compliance with:

## Mandatory Requirements

### UK GDPR

Protecting:

* Patient information
* Staff records
* Research data

### Data Protection Act 2018

Ensuring lawful processing of health information.

### NHS Data Security and Protection Toolkit (DSPT)

The Trust must demonstrate appropriate controls around:

* Confidentiality
* Integrity
* Availability
* Staff awareness
* Incident management

### NIS Regulations 2018

Acute NHS Trusts are typically designated Operators of Essential Services (OES) under the NIS Regulations given the criticality of the services they provide; the NCSC CAF is the assessment methodology used to demonstrate NIS compliance, rather than a separate, unrelated framework (see also [007-assumptions_and_constraints](007-assumptions_and_constraints.md)).

### Digital Technology Assessment Criteria (DTAC) and Cyber Essentials Plus

Where the Trust procures new digital health technologies, DTAC provides the assurance criteria expected of suppliers. Cyber Essentials Plus is referenced as a baseline technical control standard commonly expected of suppliers and, in some cases, of the Trust itself as part of NHS contractual requirements. Both are supplier/procurement-facing rather than a blanket Trust-wide obligation.


# 6. Business Challenge

The Chief Information Security Officer (CISO) has requested a cybersecurity governance improvement programme.

The Trust requires:

* Better visibility of cyber risks.
* Improved regulatory compliance.
* Stronger security governance.
* Improved incident preparedness.
* Better reporting to senior leadership.

The Board wants assurance that:

> "The organisation understands its cybersecurity risks and has appropriate controls in place to protect patients, clinical services, and sensitive information."

This assurance is provided jointly with the Trust's statutory information governance roles — the Senior Information Risk Owner (SIRO) and Caldicott Guardian — alongside the CISO. Full stakeholder responsibilities are set out in [006-stakeholders](006-stakeholders.md).

The legacy medical devices identified in Incident 2 also raise clinical safety considerations, not only technical ones: changes to how these devices are managed should have regard to the clinical safety standards DCB0129 and DCB0160 and relevant MHRA medical device cybersecurity guidance, in addition to standard IT asset and patch management practice.


# 7. Required Deliverables

### 1. Perform a Cybersecurity Gap Assessment

Assess current maturity against:

* NCSC CAF
* ISO/IEC 27001
* NHS DSP Toolkit


### 2. Develop a Cyber Risk Management Framework

Create:

* Asset register
* Risk register
* Risk scoring methodology
* Risk treatment plans


### 3. Improve Governance Documentation

Develop:

* Information Security Policy
* Access Control Policy
* Incident Response Plan
* Supplier Security Policy
* Data Classification Policy


### 4. Strengthen Compliance Management

Create:

* Compliance matrix
* Control mapping
* Evidence register
* Audit tracker


### 5. Improve Incident Preparedness

Review:

* Incident Response Plan
* Escalation procedures
* Communication process
* Lessons learned process


### 6. Develop Security Reporting

Create dashboards showing:

* Cyber risk exposure
* Compliance status
* Vulnerability trends
* Security awareness completion
* Incident statistics



# 8. Indicative Programme Phasing

The programme is expected to progress through the following broad phases, without committing to fixed dates at this Discovery stage:

1. **Discovery** — establish the current-state baseline, risk register, and governance documentation (this phase; see [004-project_objectives](004-project_objectives.md) and [005-project_scope](005-project_scope.md)).
2. **Risk treatment planning** — agree target maturity levels and prioritised remediation with the Board.
3. **Assurance embedding** — implement, test, and embed controls into business-as-usual operations, with regular reporting against the objectives set out in this brief.



# 9. Project Objectives

The full set of programme objectives, baselines, and CAF outcome mapping is defined in [004-project_objectives](004-project_objectives.md). In summary, the programme aims to improve governance, reduce cyber risk, improve regulatory compliance, strengthen resilience, improve executive visibility, and increase workforce awareness.



# 10. Expected Deliverables

Your portfolio will contain:

```
Project SentinelCare

├── Cyber Security Assessment Report
├── NCSC CAF Gap Analysis
├── ISO27001 Control Mapping
├── NHS DSP Toolkit Compliance Matrix
├── Cyber Risk Register
├── Asset Register
├── Data Classification Framework
├── DPIA Assessment
├── Incident Response Plan
├── Business Continuity Assessment
├── Security Policies
├── Audit Report
├── Power BI Risk Dashboard
└── Executive Presentation
```

## Assessment Methodology

The assessment evaluates Westbridge Hospitals Trust
against recognised cybersecurity frameworks:

### Frameworks

- NCSC Cyber Assessment Framework (CAF)
- ISO/IEC 27001:2022
- NHS Data Security and Protection Toolkit

### Assessment Approach

The assessment considers:

1. Governance
2. Risk Management
3. Asset Management
4. Identity and Access Management
5. Data Protection
6. Incident Response
7. Supplier Security
8. Security Monitoring
9. Business Continuity
10. Security Culture

### Maturity Scale

| Level | Description |
|-|-|
| 1 | Initial |
| 2 | Developing |
| 3 | Defined |
| 4 | Managed |
| 5 | Optimised |

## Why this makes a strong portfolio project

This scenario demonstrates that you understand:

✅ NHS cybersecurity challenges
✅ GRC responsibilities
✅ Risk management
✅ Regulatory compliance
✅ Information governance
✅ Incident response
✅ Business communication
✅ Executive reporting

It also aligns very closely with the type of work performed by **Cyber Security Analyst, GRC Analyst, Information Security Analyst, and NHS Digital Security roles**.
