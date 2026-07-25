# Internal Audit Report — Cyber Security and Information Governance

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Internal Audit Report
**Owner:** Head of Internal Audit
**Version:** 1.0



# 1. Purpose

This report presents the findings of an internal audit of WHT's cyber security and information governance arrangements, commissioned by the Audit and Risk Committee to independently verify the self-assessed positions in [../03-Current-State-Assessment/](../03-Current-State-Assessment/) and to test whether the treatment and remediation activity recorded in [../04-Risk-Management/046-risk_treatment_plans](../04-Risk-Management/046-risk_treatment_plans.md) is actually operating, not just planned. It is performed in accordance with the **Public Sector Internal Audit Standards (PSIAS)**, which apply to NHS internal audit functions, and follows the Institute of Internal Auditors' Three Lines Model: this audit constitutes the Third Line — independent assurance over the First Line (operational management, e.g. Infrastructure Manager, Clinical Engineering Manager) and Second Line (risk and compliance oversight, e.g. CISO, DPO, the Cyber Security Governance Group).



# 2. Scope

**In scope:** governance and risk management ([05-Governance](../05-Governance/README.md), [04-Risk-Management](../04-Risk-Management/README.md)), asset management ([02-Asset-Management](../02-Asset-Management/README.md)), security operations ([09-Security-Operations](../09-Security-Operations/README.md)), incident management ([08-Incident-Management](../08-Incident-Management/README.md)), and business continuity ([10-Business-Continuity](../10-Business-Continuity/README.md)) — the six phases with sufficient documented evidence to test as of this audit's fieldwork date.

**Out of scope:** live technical testing. Consistent with the constraint already recorded at [../01-Discovery/007-assumptions_and_constraints](../01-Discovery/007-assumptions_and_constraints.md) (C-007, C-008), this audit did not perform penetration testing, vulnerability scanning, or independent technical validation of any control. Audit testing was limited to documentation review, corroboration across independently maintained documents (e.g. checking that a risk closed in one document is reflected as closed everywhere it is referenced), and interview-equivalent walkthroughs of the process as described. Findings describing a control as "not evidenced" mean exactly that — absence of evidence, not confirmed absence of the control — and should be read with that distinction in mind, particularly by anyone using this report to support a regulatory return.



# 3. Audit Criteria and Methodology

Findings are assessed against the frameworks WHT already benchmarks itself to: NCSC Cyber Assessment Framework ([022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md)), ISO/IEC 27001:2022 Annex A ([023-ISO27001_assessment](../03-Current-State-Assessment/023-ISO27001_assessment.md)), and NHS DSPT ([024-dsp_toolkit_review](../03-Current-State-Assessment/024-dsp_toolkit_review.md)), plus WHT's own internal policies and plans. Testing approach:

1. Re-read each in-scope document's stated ratings, recommendations, and target dates.
2. Cross-check the same fact where it is referenced in more than one document (e.g. a risk's status in [049-risk_register](../04-Risk-Management/049-risk_register.md) versus its treatment status in [046-risk_treatment_plans](../04-Risk-Management/046-risk_treatment_plans.md)) for consistency.
3. Sample specific register entries for plausibility and completeness rather than reviewing every line (e.g. the [091-vulnerability_register](../09-Security-Operations/091-vulnerability_register.md) sample entries were individually reviewed against their stated SLA).
4. Identify findings that only become visible by looking across documents — a single document being internally consistent does not mean the underlying control is operating; §5 below records several findings of this kind.

Audit opinions use the standard four-point internal audit assurance scale: **Substantial** (controls operating effectively) / **Reasonable** (controls mostly operating, some improvement needed) / **Limited** (significant gaps, timely action required) / **No Assurance** (fundamental gaps, immediate action required).



# 4. Roles and Responsibilities

| Role | Audit Function |
|---|---|
| Head of Internal Audit | Owns this report; independent of the functions audited; reports directly to the Audit and Risk Committee |
| Audit and Risk Committee | Commissions and receives this audit; already receives CSGG quarterly reports per [052-roles_and_responsibilities](../05-Governance/052-roles_and_responsibilities.md) §2 |
| CISO / Second Line functions | Provide evidence and walkthroughs; own the corrective actions in [113-capa_tracker](113-capa_tracker.xlsx) that fall within their existing risk/treatment ownership |
| Trust Board | Receives the overall audit opinion (§6) and any Critical findings via the Audit and Risk Committee escalation path |

WHT does not currently document a standing Internal Audit function or an explicit Three Lines Model anywhere in [052-roles_and_responsibilities](../05-Governance/052-roles_and_responsibilities.md) — this audit was commissioned on an ad hoc basis by the Audit and Risk Committee rather than under a pre-existing internal audit charter. This is itself a finding (AUD-006, §5).



# 5. Findings

Findings use the same four-point severity scale as the rest of the programme ([047-risk_methodology](../04-Risk-Management/047-risk_methodology.md) §2.2), so audit severity, risk rating, and incident severity speak a common language.

| ID | Severity | Finding | Evidence | Root Cause | Linked Risk/REC |
|---|---|---|---|---|---|
| AUD-001 | Critical | The Guest Wi-Fi controller vulnerability (VUL-007: default administrative credentials, CVSS 9.8) is recorded as "Open" with no compensating control and no linked risk ID, unlike every other Critical/High entry in the same register | [091-vulnerability_register](../09-Security-Operations/091-vulnerability_register.md) §5 | A Critical-severity finding with no compensating control and no risk linkage falls outside the register's own escalation logic (§7 of that document only triggers compensating-control documentation for vendor-constrained assets) — a default-credential finding on general IT infrastructure has no equivalent forcing function | Not linked to any CR-XXX risk |
| AUD-002 | High | No offline/immutable backup copy exists, and no recurring backup/disaster recovery test has been run; recovery time objectives in [102-disaster_recovery_plan](../10-Business-Continuity/102-disaster_recovery_plan.md) §3 are therefore design targets, not demonstrated capability | [102-disaster_recovery_plan](../10-Business-Continuity/102-disaster_recovery_plan.md) §4, §8 | CR-011 treatment action ("offline/immutable backup implementation") remains Planned, not started | CR-011; CAF REC-003; DRP REC-001/REC-002 |
| AUD-003 | High | Role-based access control and a recurring access review cycle are not yet implemented; CAF B2 Identity and Access Control is rated Not Achieved | [022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) §3; [046-risk_treatment_plans](../04-Risk-Management/046-risk_treatment_plans.md) §3 | CR-004 treatment status is Planned, target Q1 2027, not yet started | CR-004; CAF REC-002; ISO REC-003; DSPT REC-003 |
| AUD-004 | High | Security monitoring depends on a single Managed Security Service Provider relationship (AST-035) with no evidenced continuous correlation capability; CAF C1 and C2 are both rated Not Achieved | [022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) §3; [091-vulnerability_register](../09-Security-Operations/091-vulnerability_register.md) §3 | CR-009 treatment (expand SOC/MSSP monitoring coverage) is Planned, not started; no evidence of a fallback if the single MSSP relationship is disrupted | CR-009; CAF REC-005 |
| AUD-005 | Medium | The unverified network switch vulnerability (VUL-002) is a direct operational consequence of the asset ownership gap tracked separately as CR-007 — the two are not currently cross-referenced as cause and effect in either document | [091-vulnerability_register](../09-Security-Operations/091-vulnerability_register.md) §5; [049-risk_register](../04-Risk-Management/049-risk_register.md) | Asset ownership records remain inaccurate in places; until CR-007 closes, new instances of this same failure mode should be expected elsewhere in the estate, not just VUL-002 | CR-007 |
| AUD-006 | Medium | No standing Internal Audit function, audit charter, or Three Lines Model is documented anywhere in the programme; this audit was commissioned without one | [052-roles_and_responsibilities](../05-Governance/052-roles_and_responsibilities.md) §2–3 | Governance documentation has focused on the Second Line (CSGG) without formally defining Third Line independence and mandate | None — governance documentation gap |
| AUD-007 | Medium | Security awareness training is not yet mandatory or tracked to completion; CAF B6 Staff Awareness and Training is rated Not Achieved | [022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) §3 | CR-008 treatment status is Planned, target Q1 2027, not yet started | CR-008; CAF REC-004; ISO REC-006; DSPT REC-004 |
| AUD-008 | High | DSPT overall assessed outcome is "Standards Not Met," and no formal improvement plan has yet been agreed with NHS England/ICB | [024-dsp_toolkit_review](../03-Current-State-Assessment/024-dsp_toolkit_review.md) | DSPT REC-005 (agree a formal improvement plan) is targeted for Q3 2026 and, as of this audit, remains open | DSPT REC-005 |
| AUD-009 | Low | Recommendation IDs (REC-XXX) are reused with different meanings across at least 25 documents in the programme, with no consolidated cross-document tracker; this creates a real risk that the Audit and Risk Committee cannot reliably confirm a specific recommendation's status without opening the source document | Programme-wide (see [112-internal_audit_checklist](112-internal_audit_checklist.xlsx)) | No single owner is accountable for recommendation-tracking consistency across documents | Addressed by [113-capa_tracker](113-capa_tracker.xlsx) (this audit) |



# 6. Overall Audit Opinion

**Limited Assurance.** WHT has established a comprehensive and internally consistent governance and risk framework — a complete asset register, a fully populated risk register with treatment plans, and now incident response and business continuity plans — which is a genuine achievement and consistent with the "Developing" overall maturity already self-assessed in [025-maturity_assessment](../03-Current-State-Assessment/025-maturity_assessment.md). However, the majority of treatment actions across the twelve tracked risks remain Planned rather than In Progress or Embedded ([046-risk_treatment_plans](../04-Risk-Management/046-risk_treatment_plans.md) §3), six CAF principles are rated Not Achieved, and DSPT's overall outcome is Standards Not Met. This audit identified one Critical and four High findings, none of which were previously flagged as audit findings in their own right — indicating that self-assessment alone, however well documented, is not yet sufficient assurance without independent testing. Governance design is ahead of operating effectiveness; the priority is delivering the treatment actions already planned, not producing further assessments.



# 7. Recommendations

| Recommendation ID | Recommendation | Priority | Owner | Target Timeframe |
|---|---|---|---|---|
| AUD-REC-001 | Link VUL-007 to a tracked risk ID and confirm remediation status against its 14-day SLA; extend the vulnerability register's escalation logic to cover any Critical finding without a compensating control, not only vendor-constrained assets | Critical | Infrastructure Manager | Immediate |
| AUD-REC-002 | Charter a formal Internal Audit function (or a co-sourced provider arrangement, as is standard NHS practice) with a documented mandate, reporting line to the Audit and Risk Committee, and a defined Three Lines Model in [052-roles_and_responsibilities](../05-Governance/052-roles_and_responsibilities.md) | Medium | Audit and Risk Committee | Q4 2026 |
| AUD-REC-003 | Add an explicit cause-and-effect cross-reference between CR-007 and any vulnerability register entry (such as VUL-002) that is a direct consequence of incomplete asset records | Low | Infrastructure Manager | Q3 2026 |
| AUD-REC-004 | Maintain [113-capa_tracker](113-capa_tracker.xlsx) as the single consolidated tracker for all open recommendations across every phase of the programme, reported to the Audit and Risk Committee quarterly alongside the existing CSGG report | Medium | Head of Internal Audit | Ongoing, quarterly |
| AUD-REC-005 | Re-perform this audit's in-scope areas within 12 months, prioritising re-testing of AUD-001 through AUD-004 given their severity | High | Head of Internal Audit | Q3 2027 |



# 8. Review and Maintenance

This report, and the corrective actions it generates in [113-capa_tracker](113-capa_tracker.xlsx), are reviewed quarterly by the Audit and Risk Committee alongside its existing CSGG report, consistent with the review cadence in [049-risk_register](../04-Risk-Management/049-risk_register.md) §7. A follow-up audit is recommended per AUD-REC-005.



# 9. Conclusion

WHT's governance and risk documentation is thorough and internally consistent, but this audit's value lies in what only becomes visible by testing across documents rather than reading any single one: a Critical vulnerability with no risk linkage, a backup capability that is a design target rather than a demonstrated one, and a governance model that has not yet formally defined the independent assurance function performing this audit. None of these findings contradict WHT's self-assessments — they extend them. The overall Limited Assurance opinion should be read as confirmation that WHT is on a credible improvement path, not as a finding that the programme's prior work was inaccurate.
