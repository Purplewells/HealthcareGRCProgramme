# Threat Assessment

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Cyber Threat Assessment
**Owner:** Chief Information Security Officer (CISO)
**Version:** 1.0

## 1. Introduction

### 1.1 Purpose

This assessment describes the external cyber threat landscape facing WHT and provides the threat-actor and likelihood context that underpins the scoring of risks in [risk_register](risk_register.md) and the domain-specific assessments in this folder. It answers: *who is likely to target the Trust, how, and why?*

### 1.2 Scope

This assessment covers threat actors and attack techniques relevant to UK healthcare providers generally and WHT's specific digital estate (recorded in [../02-Asset-Management/022-master_assets_register.xlsx](../02-Asset-Management/022-master_assets_register.xlsx)). It does not cover physical security threats or clinical safety incidents unrelated to cyber activity.

## 2. Assessment Criteria

### 2.1 Framework(s) Applied

This assessment draws on publicly reported UK healthcare sector threat trends (NCSC and NHS England advisories) and feeds likelihood inputs into the Trust's standard risk methodology defined in [047-risk_methodology](047-risk_methodology.md).

### 2.2 Rating Scale

Threat actors are rated by Capability and Intent (Low / Medium / High), consistent with standard threat-intelligence practice; the combination of Capability and Intent informs the Likelihood score applied to related risks in [risk_register](risk_register.md).

## 3. Current State

UK healthcare providers have been a consistently reported target for ransomware and data-extortion groups, reflecting the sector's low tolerance for service disruption and the high value of health data. Publicly reported incidents affecting the NHS — including the WannaCry ransomware outbreak in 2017, which disrupted services across dozens of NHS organisations, and more recent ransomware attacks on pathology and diagnostic service providers — illustrate that both direct attacks on a Trust and attacks on its clinical supply chain carry equivalent operational impact. WHT's own risk register reflects this: 4 of its 12 recorded risks (CR-001, CR-002, CR-005, CR-006) are directly attributable to the threat actor categories described below.

## 4. Observations

### 4.1 Ransomware and Data-Extortion Groups are the Highest-Priority Threat Category

Financially motivated ransomware groups routinely target healthcare providers directly and via third-party clinical service suppliers, using phishing, exposed remote access, and unpatched vulnerabilities as primary access vectors. Capability: High. Intent: High.

### 4.2 Credential Theft and Phishing Actors Target Cloud Identity

Actors specifically targeting Microsoft 365 and cloud identity platforms via phishing and MFA-fatigue attacks represent a distinct, high-frequency threat category, consistent with CR-002 in [risk_register](risk_register.md). Capability: Medium-High. Intent: High.

### 4.3 Supply Chain Compromise is an Increasingly Common Attack Path Into Healthcare

Rather than attacking Trusts directly, actors increasingly compromise shared clinical software vendors or managed service providers to reach multiple healthcare organisations simultaneously, consistent with the concentration risk identified in [043-third_party_risks](043-third_party_risks.md) §4.3. Capability: High. Intent: Medium-High.

### 4.4 Opportunistic Exploitation of Unsupported Systems

Automated scanning and exploitation of known vulnerabilities in unsupported operating systems (including legacy medical devices) is a low-cost, high-frequency threat vector requiring no specific targeting of WHT, consistent with CR-003 and [042-medical_device_risk](042-medical_device_risk.md). Capability: Low-Medium. Intent: N/A (opportunistic, not targeted).

### 4.5 Insider Risk is Present but Lower Capability Than External Actors

Excessive access privileges (CR-004) create a credible insider misuse pathway, though this is assessed as lower likelihood and capability than the external threat categories above, since it depends on an existing trusted position being misused rather than an external compromise.

## 5. Evidence

| Evidence ID | Description | Source | Date | Linked Observation |
|---|---|---|---|---|
| EVD-001 | CR-001 Ransomware affecting clinical services, scored 25 (Critical) | [risk_register](risk_register.md) | 2026-07-23 | 4.1 |
| EVD-002 | CR-002 Compromise of Microsoft 365 accounts, scored 20 (Critical) | [risk_register](risk_register.md) | 2026-07-23 | 4.2 |
| EVD-003 | Third-party concentration risk in critical clinical systems | [043-third_party_risks](043-third_party_risks.md) §4.3 | 2026-07-23 | 4.3 |
| EVD-004 | 25 devices identified running unsupported operating systems | [../01-Discovery/003-business-context](../01-Discovery/003-business-context.md) §3.4 | 2026-07-23 | 4.4 |
| EVD-005 | CR-004 Excessive user access privileges, scored 16 (High) | [risk_register](risk_register.md) | 2026-07-23 | 4.5 |

## 6. Analysis

### 6.1 Findings

The threat landscape facing WHT is dominated by financially motivated actors (ransomware, credential theft, supply chain) rather than nation-state or ideologically motivated actors, which is consistent with the general pattern reported across the UK healthcare sector. This matters for prioritisation: financially motivated actors are opportunistic and will pursue the path of least resistance, which means the Trust's own control gaps (unsupported devices, weak access management, immature supplier assurance) determine exposure more than any specific targeting decision by an attacker.

### 6.2 Root Cause

There is no single root cause for external threat activity — it is an environmental condition rather than an internal Trust weakness. The relevant root-cause question is not why these threats exist, but why the Trust's defensive posture (detection capability rated Not Achieved in [../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) §3) is not yet matched to a threat landscape that is well understood and well documented across the sector.

## 7. Risk Rating

| Risk ID | Description | Likelihood | Impact | Rating | Linked Observation |
|---|---|---|---|---|---|
| CR-001 | Ransomware affecting clinical services | 5 | 5 | Critical | 4.1 |
| CR-002 | Compromise of Microsoft 365 accounts | 4 | 5 | Critical | 4.2 |
| CR-006 | Third-party supplier compromise | 4 | 5 | Critical | 4.3 |
| CR-003 | Unsupported medical devices exploited | 4 | 5 | Critical | 4.4 |
| CR-004 | Excessive user access privileges | 4 | 4 | High | 4.5 |

## 8. Recommendations

| Recommendation ID | Recommendation | Priority | Owner | Target Timeframe |
|---|---|---|---|---|
| REC-001 | Subscribe to NHS England and NCSC sector-specific threat intelligence feeds and formally review them at each Cyber Security Governance Group meeting | High | CISO | Q3 2026 |
| REC-002 | Prioritise detection capability uplift (CAF C1/C2) given the confirmed prevalence of ransomware and credential-theft actors targeting the sector | High | CISO / SOC Manager | Q1 2027 |
| REC-003 | Use this threat assessment's Capability/Intent ratings as a standing input when re-scoring Likelihood in future risk register reviews | Medium | CISO | Ongoing, at each quarterly review |

## 9. Conclusion

WHT faces a threat landscape typical of UK healthcare providers, dominated by financially motivated ransomware, credential-theft, and supply-chain actors rather than sophisticated targeted campaigns. Because these threats are opportunistic, the Trust's own control maturity — not attacker sophistication — is the primary determinant of realised risk, reinforcing the priority already established across [../03-Current-State-Assessment/](../03-Current-State-Assessment/) and this folder's domain risk assessments: close the known gaps in detection, access management, supplier assurance, and legacy device exposure before the threat landscape exploits them.
