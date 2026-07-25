# Diagrams

Standalone Mermaid diagrams that make visible what would otherwise only be described in text across the programme, following the same convention as [../../06-Information-Governance/Data_Flow_Diagrams/](../../06-Information-Governance/Data_Flow_Diagrams/) (data classification colour coding, one diagram per file, referenced from the assessment documents that rely on it rather than duplicated into them).

| Diagram | Covers | Referenced By |
|---|---|---|
| [001-network_infrastructure_architecture](001-network_infrastructure_architecture.md) | On-premises, Azure, and clinical network topology; identity as a single control point; single-site backup dependency | [041-cloud_risk](../../04-Risk-Management/041-cloud_risk.md), [102-disaster_recovery_plan](../../10-Business-Continuity/102-disaster_recovery_plan.md) |
| [002-azure_management_group_hierarchy](002-azure_management_group_hierarchy.md) | Current flat Azure subscription vs. target management group structure | [121-azure_governance_assessment](../../12-Azure-Governance/121-azure_governance_assessment.md) AZG-REC-001 |
| [003-governance_reporting_structure](003-governance_reporting_structure.md) | CSGG membership and reporting lines from Board to operational asset owners | [052-roles_and_responsibilities](../../05-Governance/052-roles_and_responsibilities.md), [111-internal_audit_report](../../11-Audit/111-internal_audit_report.md) AUD-006 |

Existing data flow and trust boundary diagrams for the Patient Portal and core clinical systems already live in [06-Information-Governance/Data_Flow_Diagrams/](../../06-Information-Governance/Data_Flow_Diagrams/) — they are not duplicated here.
