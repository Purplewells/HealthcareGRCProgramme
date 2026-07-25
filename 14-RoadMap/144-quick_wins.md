# Quick Wins

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Near-Term Action List
**Owner:** CISO (Chief Information Security Officer)
**Version:** 1.0

## 1. Purpose

The initiatives in [141-cyber_security_roadmap](141-cyber_security_roadmap.md) are mostly multi-quarter programmes of work. This document pulls out the specific actions inside them that need little or no additional funding and can realistically be completed within 90 days — the actions a new CISO or Trust Board member could point to as visible progress while the larger initiatives are still being scoped and funded. A quick win here is not a substitute for the initiative it sits under; it is the first, fastest slice of it.

## 2. Criteria

An action qualifies as a quick win if it meets all three:

1. **Low cost** — no new licensing, headcount, or capital spend required
2. **Short duration** — deliverable within 90 days by the named owner using existing resource
3. **Visible outcome** — closes a specific, named finding or moves a specific metric, not a vague improvement

## 3. Quick Wins

| Action | Closes | Owner | Why It Qualifies |
|---|---|---|---|
| Link VUL-007 to a tracked risk ID (CR-XXX) and confirm remediation status against its 14-day SLA | AUD-001 | Infrastructure Manager | Single record update in the vulnerability register; no new tooling |
| Extend the vulnerability register's escalation logic to cover any Critical finding without a compensating control | AUD-001 | Infrastructure Manager | Documentation/process change to an existing register |
| Enable Conditional Access policies CAP-001 and CAP-002 in Report-only mode and begin sign-in log review | Part of INIT-04, 041-REC-002 | Identity Security Lead | Configuration of already-licensed Microsoft Entra ID capability |
| Add the Business Continuity Manager to CSGG membership | 101-REC-002 | CISO | Governance membership change; no cost |
| Add an explicit cause-and-effect cross-reference between CR-007 and VUL-002 in the risk register | AUD-REC-003 | Infrastructure Manager | Documentation cross-reference between two existing records |
| Establish the monthly Secure Score review and report the baseline score to the CSGG | 041-REC-001 | Cloud Service Owner | Secure Score is already available in the Trust's existing Microsoft 365/Azure licensing; see [123-secure_score_review](../12-Azure-Governance/123-secure_score_review.md) |
| Designate a second Global Administrator and reduce standing privileged role assignments in Entra ID | Secure Score Identity category | Identity Security Lead | Configuration change with no licensing cost; immediate Secure Score improvement |
| Block legacy authentication protocols (CAP-003) | Secure Score Identity category, 041-REC-002 | Identity Security Lead | Single Conditional Access policy; low disruption once validated in Report-only mode |
| Draft the DSPT improvement plan for agreement with NHS England/the ICB | 024-REC-005 | CISO | Documentation exercise using evidence already gathered in [024-dsp_toolkit_review](../03-Current-State-Assessment/024-dsp_toolkit_review.md) |
| Re-validate risk register Likelihood scores against the threat assessment's Capability/Intent ratings | 047-REC-004 | CISO | Desk-based review of two existing documents |
| Formally document the Trust Board escalation threshold for accepting any Impact-5 risk | 047-REC-002 | CISO | Policy documentation; no new capability required |
| Charter the CSGG's existing quarterly reporting to explicitly include the AUD-REC-004 consolidated tracker | AUD-REC-004 | Head of Internal Audit | Adds one item to an already-scheduled quarterly report |

## 4. What This List Deliberately Excludes

Medical device replacement, RBAC implementation, security monitoring expansion, and immutable backup infrastructure are not on this list — not because they are unimportant, but because none of them can genuinely be completed in 90 days without either capital spend or new headcount. Presenting them as quick wins would misrepresent their actual delivery timeline to the Board; they are tracked instead in [141-cyber_security_roadmap](141-cyber_security_roadmap.md) and costed in [143-investment_priorities](143-investment_priorities.md).

## 5. Tracking

Quick wins are reported monthly to the CSGG as a standing agenda item, separate from the quarterly roadmap update, since their value is in visible near-term momentum rather than long-range planning. A quick win not delivered within its 90-day window is moved to the relevant initiative in [141-cyber_security_roadmap](141-cyber_security_roadmap.md) rather than left open indefinitely on this list.

## 6. Review and Maintenance

This list is refreshed each quarter as items complete, pulling the next 90-day slice out of whichever roadmap initiative is currently active.
