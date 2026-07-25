# Investment Priorities

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Investment Case
**Owner:** CISO (Chief Information Security Officer)
**Version:** 1.0

## 1. Purpose

[141-cyber_security_roadmap](141-cyber_security_roadmap.md) sequences twelve initiatives by risk and dependency. This document re-views the same twelve initiatives through the lens the Trust Board and Finance Committee actually need for a funding decision: what type of investment each one is (people, process, or technology), roughly how large an undertaking it is, and what happens if it is not funded. No specific costs are stated here — this programme's documentation does not hold a costed business case for any initiative — so figures should be obtained from the relevant budget owner before this document is used to support a funding submission.

## 2. Investment Categories

Each initiative is classified by the type of investment it primarily requires:

- **People** — new roles, headcount, or a named individual's dedicated time
- **Process** — governance, policy, or ways-of-working change with limited direct spend
- **Technology** — licensing, tooling, or infrastructure spend

Most initiatives require more than one category; the classification below reflects the dominant one.

## 3. Investment Priorities

| Initiative | Category | Relative Size | Rationale | Cost of Inaction |
|---|---|---|---|---|
| INIT-01 Link VUL-007 / fix escalation gap | Process | Small | Closing a documentation and process gap on an already-identified vulnerability | A Critical, internet-reachable vulnerability remains untracked and unprioritised |
| INIT-02 Supplier security assurance process | People + Process | Medium | Needs a named process owner and a recurring assessment cycle across 150+ suppliers | Weak supplier security remains the Trust's most consistently cited gap across CAF (A4), ISO (A.5.19–23), and DSPT (Standard 10) |
| INIT-03 RBAC and access review cycle | Technology + Process | Large | Requires Identity and Access Management tooling investment and a recurring review process across clinical and corporate systems Trust-wide | CAF B2 remains Not Achieved; CR-004 (excessive privileges) stays open; identity remains the single point of failure flagged in [041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §4.2 |
| INIT-04 Conditional Access / Azure RBAC enforcement | Technology | Medium | Primarily configuration of already-licensed Microsoft Entra ID capability, not new spend, but requires dedicated identity engineering time | CR-002 (compromise of Microsoft 365 accounts) remains the Trust's single Critical-rated risk in [041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §7 |
| INIT-05 Security monitoring expansion (CAF C1/C2) | Technology + People | Large | Likely requires expanded MSSP contract scope or additional SOC capability; the single-MSSP dependency is itself an audit finding (AUD-004) | The Trust has no continuous detection capability beyond one vendor relationship; both CAF Objective C principles remain Not Achieved |
| INIT-06 Azure governance and recurring cloud review | Process + Technology | Medium | Primarily configuration of existing Azure capability (Policy, management groups) plus a recurring review cadence | Configuration drift persists undetected in an estate hosting four Restricted-classified patient-facing services |
| INIT-07 Medical device remediation | Technology + People | Large | Replacement or compensating controls for a fleet of legacy/unsupported clinical devices is typically the most capital-intensive item in a programme like this | CR-003 remains open; unsupported medical devices are a recurring theme across the current-state assessment, DSPT (Standard 8), and the device-specific risk assessment |
| INIT-08 Immutable backup and DR testing | Technology | Medium | Offline/immutable backup infrastructure and a recurring test programme | CR-011 remains open; recovery time objectives remain design targets rather than demonstrated capability (AUD-002) |
| INIT-09 DSPT improvement plan | Process | Small | Primarily a governance and documentation exercise with an external deadline | Continued "Standards Not Met" outcome can restrict the Trust's access to shared national NHS systems |
| INIT-10 Security awareness training | Process + Technology | Small | Training platform (likely already licensed as part of Microsoft 365) plus mandatory completion tracking | Most successful attacks begin with a person, not a system; CAF B6 remains Not Achieved |
| INIT-11 Internal Audit charter | People | Small | Formalising an existing ad hoc arrangement, or contracting a co-sourced provider | Independent assurance over the programme continues on an ad hoc basis with no standing mandate (AUD-006) |
| INIT-12 Data classification / lawful basis extension | Process | Medium | Extends work already completed for the Patient Portal to the Trust's other core clinical systems | Uncontrolled copies of patient reports and incomplete lawful basis documentation remain unaddressed for LIS, RIS/PACS, Pharmacy, and Theatre systems |

## 4. Highest-Leverage Investments

Three initiatives stand out as disproportionately high-leverage relative to their size:

- **INIT-04 (Conditional Access enforcement)** is largely a configuration exercise against capability the Trust already licenses, yet it closes the Trust's single Critical-rated risk (CR-002) and is the single highest-leverage action identified in [041-cloud_risk](../04-Risk-Management/041-cloud_risk.md) §9.
- **INIT-01 (link VUL-007)** is a near-zero-cost process fix that closes the audit's only Critical finding.
- **INIT-09 (DSPT improvement plan)** is a documentation exercise with an external deadline and a direct, practical consequence (access to shared national systems) if missed.

Where funding is constrained, these three should be prioritised ahead of the larger technology investments (INIT-05, INIT-07), which — while ultimately necessary — take longer to scope, approve, and deliver regardless of funding availability.

## 5. Review and Maintenance

This document is reviewed alongside [141-cyber_security_roadmap](141-cyber_security_roadmap.md) whenever a funding decision is being prepared, and updated with actual costed figures once the Finance Committee has reviewed each initiative's business case — at which point this document should be treated as superseded for that initiative, not authoritative.
