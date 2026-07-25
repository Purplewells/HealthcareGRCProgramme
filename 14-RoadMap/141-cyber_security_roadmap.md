# Cyber Security Roadmap

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Improvement Roadmap
**Owner:** CISO (Chief Information Security Officer)
**Version:** 1.0

## 1. Introduction

### 1.1 Purpose

Every phase of this programme — the current-state assessments ([03-Current-State-Assessment](../03-Current-State-Assessment/README.md)), the risk register and its domain-specific assessments ([04-Risk-Management](../04-Risk-Management/README.md)), the internal audit ([11-Audit](../11-Audit/README.md)), and the Azure governance assessment ([12-Azure-Governance](../12-Azure-Governance/README.md)) — has raised its own recommendations. Taken individually, none of those documents tells the Trust Board *what to do first, with what resource, by when*. This roadmap does that: it consolidates the recommendations raised across the programme into a single, sequenced plan, and explains the logic behind the sequencing. [142-12_month_improvement_plan](142-12_month_improvement_plan.md) is this roadmap's quarter-by-quarter detail; [143-investment_priorities](143-investment_priorities.md) and [144-quick_wins](144-quick_wins.md) are its investment-case and near-term-action views of the same underlying plan.

### 1.2 Scope

This roadmap covers every recommendation raised in [03-Current-State-Assessment](../03-Current-State-Assessment/README.md), [04-Risk-Management](../04-Risk-Management/README.md), [07-Compliance](../07-Compliance/README.md), [10-Business-Continuity](../10-Business-Continuity/README.md), [11-Audit](../11-Audit/README.md), and [12-Azure-Governance](../12-Azure-Governance/README.md), grouped into a smaller number of underlying initiatives (§3) rather than tracked as individual recommendation IDs, because — as [111-internal_audit_report](../11-Audit/111-internal_audit_report.md) finding AUD-009 records — the same recommendation ID (e.g. REC-001) is reused with a different meaning in more than 15 documents across the programme. Individual recommendation-level tracking remains the job of [113-capa_tracker](../11-Audit/113-capa_tracker.xlsx) (AUD-REC-004); this roadmap operates one level up, at the initiative level.

## 2. How This Roadmap Was Built

### 2.1 Consolidation Method

Many recommendations across the programme are the same underlying piece of work, stated once per framework. For example, "establish a supplier security assurance process" is recommended separately in the current-state assessment, the CAF assessment, the ISO 27001 assessment, the DSPT review, and the third-party risk assessment — five documents, one initiative. This roadmap groups those into the twelve initiatives in §3, each tagged with every source recommendation it closes, so a reader can trace back from any initiative to the original finding, and confirm that delivering one initiative closes several documents' recommendations at once.

### 2.2 Sequencing Logic

Initiatives are sequenced against three factors, in order of weight:

1. **Risk severity** — initiatives that close Critical/High risks or audit findings are sequenced first (e.g. INIT-01, closing AUD-001, the Critical vulnerability with no risk linkage).
2. **Dependency** — some initiatives are prerequisites for others. Azure governance structure (INIT-06) must precede Conditional Access enforcement completing at scale (INIT-06 also covers this); a supplier assurance process (INIT-02) must exist before individual supplier gaps like SUP-005 (§ [043-third_party_risks](../04-Risk-Management/043-third_party_risks.md)) can be closed systematically rather than one at a time.
3. **Regulatory deadline** — the DSPT annual submission (INIT-09) has an external deadline the Trust does not control, so it is sequenced to complete ahead of that date regardless of its risk score alone.

## 3. Initiatives

| ID | Initiative | Closes | Priority | Owner | Target |
|---|---|---|---|---|---|
| INIT-01 | Link the unlinked Critical vulnerability (VUL-007) to a tracked risk and fix the escalation gap that let it go unlinked | AUD-REC-001 | Critical | Infrastructure Manager | Immediate |
| INIT-02 | Stand up a Trust-wide supplier security assurance process (onboarding assessment, contractual clauses, annual re-assessment) | 021-REC-004, 022-REC-001, 023-REC-002, 024-REC-002, 043-REC-001, 042-REC-004 | High | Procurement Director | Q4 2026 |
| INIT-03 | Implement role-based access control and a recurring access review cycle, Trust-wide | 021-REC-005, 022-REC-002, 023-REC-003, 024-REC-003, 054 (policy already sets requirement) | High | IAM Manager | Q1 2027 |
| INIT-04 | Enforce MFA and Conditional Access for all Entra ID accounts and complete the Azure governance structure that scopes it | 041-REC-002, AZG-REC-001, AZG-REC-002, [122-conditional_access_policies](../12-Azure-Governance/122-conditional_access_policies.md) rollout | High | Identity Security Lead / Cloud Service Owner | Q4 2026 |
| INIT-05 | Expand security monitoring and detection coverage beyond the single MSSP relationship (CAF C1/C2) | 021-REC-007, 022-REC-005, 023-REC-004, 044-REC-002, AUD-004 | High | CISO / SOC Manager | Q1 2027 |
| INIT-06 | Establish a recurring Azure/cloud configuration review and enforce policy at scale | 041-REC-001, AZG-REC-003, AZG-REC-004, AZG-REC-005, [123-secure_score_review](../12-Azure-Governance/123-secure_score_review.md) | High | Cloud Service Owner | Q4 2026 |
| INIT-07 | Complete a medical device vulnerability assessment and replacement/compensating-control plan for unsupported devices | 021-REC-003, 024-REC-001, 042-REC-001/002/003 | High | Clinical Engineering Manager | Q4 2026 |
| INIT-08 | Implement an offline/immutable backup and a recurring, evidenced backup/DR test cycle | 022-REC-003, 102-REC-001/002, 041-REC-004, AUD-002 | High | Infrastructure Manager | Q4 2026 |
| INIT-09 | Agree a formal DSPT improvement plan with NHS England/the ICB ahead of this year's submission | 024-REC-005, AUD-008 | High | CISO | Q3 2026 |
| INIT-10 | Deploy mandatory, tracked security awareness training with completion reporting | 022-REC-004, 023-REC-006, 024-REC-004 | Medium | Security Awareness Lead | Q1 2027 |
| INIT-11 | Charter a formal Internal Audit function with a defined Three Lines Model | AUD-REC-002 | Medium | Audit and Risk Committee | Q4 2026 |
| INIT-12 | Remediate uncontrolled copies of patient reports and extend data classification/lawful-basis coverage to remaining core clinical systems | 021-REC-006, 071-REC-001/003 | Medium | Data Protection Officer | Q4 2026 – Q1 2027 |

## 4. Phasing

### 4.1 Phase 1 — Immediate to Q3 2026: Stop the Bleeding

Close the one Critical finding with no compensating control (INIT-01), agree the DSPT improvement plan ahead of the annual submission deadline (INIT-09), and begin the two initiatives everything else in Phase 2 depends on — supplier assurance (INIT-02) and Azure governance structure (INIT-06, foundational half).

### 4.2 Phase 2 — Q4 2026: Close the High-Risk Gaps

Deliver the initiatives that close the programme's remaining High/Critical risks and audit findings: medical device remediation (INIT-07), backup/DR testing (INIT-08), Conditional Access enforcement (INIT-04), and the Internal Audit charter (INIT-11). By the end of this phase, every Critical and most High-severity findings from [111-internal_audit_report](../11-Audit/111-internal_audit_report.md) should have moved from "Open" to "In Progress" or "Closed."

### 4.3 Phase 3 — Q1 2027: Embed and Detect

Complete the initiatives that require the Phase 1–2 foundations to be in place first: access control (INIT-03, needs INIT-02's supplier scoping and INIT-06's Azure RBAC groundwork), security monitoring expansion (INIT-05), security awareness training (INIT-10), and data classification/lawful-basis extension (INIT-12).

### 4.4 Phase 4 — Beyond Q1 2027: Sustain

Re-run the CAF, ISO 27001, and DSPT assessments to confirm the improvement has actually moved the Trust's ratings (not just closed individual actions), and re-perform the internal audit's in-scope areas (AUD-REC-005), consistent with the review cadences already set in each source document.

## 5. Governance and Reporting

Progress against this roadmap is reported to the Cyber Security Governance Group (CSGG) monthly and to the Audit and Risk Committee quarterly, using the same severity language as the rest of the programme so a roadmap status update and a risk register status update are always directly comparable. [113-capa_tracker](../11-Audit/113-capa_tracker.xlsx) remains the authoritative record of individual recommendation status; this roadmap is reviewed against it quarterly to confirm the initiative groupings in §3 still hold as individual recommendations close.

## 6. Review and Maintenance

This roadmap is reviewed quarterly by the CISO alongside the CSGG's existing reporting cadence, and re-baselined whenever a Phase completes or a new Critical/High finding is raised that does not fit an existing initiative.
