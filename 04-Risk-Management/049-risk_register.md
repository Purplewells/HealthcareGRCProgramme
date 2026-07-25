# Cyber Risk Register
**Organisation:** Westbridge Hospitals Trust (WHT)  
**Document Type:** Cyber Risk Register  
**Owner:** Chief Information Security Officer (CISO)  
**Version:** 1.0  

---

# 1. Purpose

The Cyber Risk Register provides a structured approach for identifying, assessing, treating, and monitoring cybersecurity risks affecting Westbridge Hospitals Trust.

The register supports:

- Executive risk reporting.
- Regulatory compliance.
- Cybersecurity governance.
- Risk treatment planning.
- Audit assurance.
- Continuous improvement.

---

# 2. Risk Ownership Model

Cyber risk ownership follows the principle that:

> "The person accountable for the business service or information asset owns the associated risk."

The Cyber Security Team provides:

- Risk assessment expertise.
- Security recommendations.
- Threat intelligence.
- Control guidance.
- Risk monitoring.

However, business and clinical owners remain accountable for accepting and managing risks affecting their services.

---

# 3. Risk Rating Methodology

## Likelihood Scale

| Score | Rating | Description |
|---|---|---|
| 1 | Rare | Unlikely to occur |
| 2 | Unlikely | Could occur occasionally |
| 3 | Possible | Realistic possibility |
| 4 | Likely | Expected to occur |
| 5 | Almost Certain | Highly probable |

---

## Impact Scale

| Score | Rating | Description |
|---|---|---|
| 1 | Insignificant | Minimal operational impact |
| 2 | Minor | Limited disruption |
| 3 | Moderate | Service impact requiring management attention |
| 4 | Major | Significant operational or regulatory impact |
| 5 | Severe | Patient safety or major organisational impact |

---

## Risk Score

Risk Score = Likelihood × Impact

| Score | Risk Level | Action |
|---|---|---|
| 1-4 | Low | Monitor |
| 5-9 | Medium | Manage through normal processes |
| 10-16 | High | Treatment required |
| 17-25 | Critical | Immediate action required |

---

# 4. Cyber Risk Register

| ID | Risk | Asset / Service | Threat | Vulnerability | Likelihood | Impact | Score | Rating | Risk Owner | Treatment Owner |
|---|---|---|---|---|---:|---:|---:|---|---|---|
| CR-001 | Ransomware affecting clinical services | EPR, servers, clinical systems | Cyber criminals | Phishing, privilege escalation, insufficient segmentation | 5 | 5 | 25 | Critical | CDIO | CISO |
| CR-002 | Compromise of Microsoft 365 accounts | Microsoft 365 | Credential theft | Phishing and MFA fatigue attacks | 4 | 5 | 20 | Critical | CDIO | Identity Security Lead |
| CR-003 | Unsupported medical devices exploited | Medical devices | Malware exploitation | Legacy operating systems and limited patching | 4 | 5 | 20 | Critical | Clinical Engineering Manager | CISO |
| CR-004 | Excessive user access privileges | Patient systems | Insider misuse / account compromise | Poor access reviews | 4 | 4 | 16 | High | Information Asset Owners | IAM Manager |
| CR-005 | Patient data exposure | EPR and reporting platforms | Data leakage | Poor classification and uncontrolled copies | 4 | 5 | 20 | Critical | Data Protection Officer | Information Governance Team |
| CR-006 | Third-party supplier compromise | Supplier connections | Supply chain attack | Limited supplier assurance process | 4 | 5 | 20 | Critical | Procurement Director | Supplier Security Manager |
| CR-007 | Incomplete asset inventory | IT infrastructure | Unknown vulnerabilities | Inaccurate asset ownership records | 4 | 4 | 16 | High | Infrastructure Manager | IT Asset Manager |
| CR-008 | Security awareness failure | Workforce | Phishing attacks | Low training completion | 4 | 4 | 16 | High | HR Director | Security Awareness Lead |
| CR-009 | Insufficient security monitoring | Security operations | Undetected attack activity | Limited security metrics and monitoring capability | 3 | 5 | 15 | High | CISO | SOC Manager |
| CR-010 | Clinical service disruption | Critical healthcare services | System outage | Weak resilience and recovery testing | 3 | 5 | 15 | High | Chief Operating Officer | Business Continuity Manager |
| CR-011 | Data loss due to inadequate backup protection | Critical systems | Ransomware/destructive attack | Backup testing and resilience gaps | 3 | 5 | 15 | High | Infrastructure Manager | Backup Service Owner |
| CR-012 | Cloud security misconfiguration | Azure services | Unauthorised access | Incorrect configuration and insufficient governance | 3 | 5 | 15 | High | Cloud Service Owner | Cloud Security Engineer |

---

# 5. Priority Risks Requiring Immediate Attention

## CR-001: Ransomware Risk

**Risk Statement**

There is a risk that ransomware could disrupt critical healthcare services due to phishing attacks, insufficient segmentation, and privileged account compromise.

**Potential Impact**

- Patient safety impact.
- Loss of access to clinical systems.
- Emergency operational disruption.
- Regulatory reporting requirements.

**Owner**

Chief Digital Information Officer (CDIO)

**Treatment Actions**

- Implement stronger network segmentation.
- Improve endpoint protection.
- Review privileged access.
- Conduct ransomware exercises.
- Validate offline backups.

---

## CR-003: Legacy Medical Device Security

**Risk Statement**

There is a risk that unsupported medical devices could be exploited because vendor patching options are limited.

**Potential Impact**

- Clinical service disruption.
- Patient safety concerns.
- Malware propagation.

**Owner**

Clinical Engineering Manager

**Treatment Actions**

- Complete medical device inventory.
- Assign asset owners.
- Conduct vulnerability assessments.
- Develop replacement roadmap.
- Implement network controls.

---

## CR-006: Third-Party Supplier Risk

**Risk Statement**

There is a risk that supplier compromise could impact Trust systems due to insufficient supplier security assurance.

**Potential Impact**

- Unauthorised access.
- Data exposure.
- Service interruption.

**Owner**

Procurement Director

**Treatment Actions**

- Establish supplier risk assessment process.
- Introduce security requirements into contracts.
- Review supplier access privileges.
- Perform annual supplier reviews.

---

# 6. Risk Treatment Status

| Risk ID | Treatment | Status |
|---|---|---|
| CR-001 | Ransomware resilience improvement programme | In Progress |
| CR-002 | MFA and identity governance improvements | Planned |
| CR-003 | Medical device security improvement plan | Planned |
| CR-004 | Access review programme | Planned |
| CR-005 | Data governance improvement programme | In Progress |
| CR-006 | Supplier assurance framework | Planned |
| CR-007 | Asset management improvement | In Progress |
| CR-008 | Security awareness programme | In Progress |
| CR-009 | Security monitoring improvements | Planned |
| CR-010 | Business continuity testing | Planned |

---

# 7. Risk Governance

The Cyber Risk Register will be reviewed:

- Monthly by the Cyber Security Governance Group.
- Quarterly by the Audit and Risk Committee.
- Annually as part of the Trust risk management process.

Risk reviews will consider:

- Changes to threat landscape.
- New technology deployments.
- Regulatory changes.
- Audit findings.
- Security incidents.

---

# 8. Expected Outcome

A mature cyber risk management process will enable WHT to:

- Understand its cyber exposure.
- Prioritise security investments.
- Assign accountability.
- Demonstrate regulatory readiness.
- Improve resilience of healthcare services.