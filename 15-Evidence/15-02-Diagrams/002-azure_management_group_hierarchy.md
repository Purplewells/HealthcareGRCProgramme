# Azure Management Group Hierarchy Diagram — Current vs Target

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Architecture Diagram
**Owner:** Cloud Service Owner
**Version:** 1.0

## Purpose

This diagram visualises the specific structural gap identified in [../../12-Azure-Governance/121-azure_governance_assessment.md](../../12-Azure-Governance/121-azure_governance_assessment.md) §4.1: a single flat Azure subscription with no management group hierarchy, versus the target state that recommendation AZG-REC-001 would deliver. It is intended to be read alongside that assessment, not as a replacement for its narrative findings.

## Diagram — Current State

```mermaid
flowchart TB
    TENANT[Entra ID Tenant — Westbridge Hospitals Trust]:::internal
    SUB[Single Subscription<br/>All resources, no boundary between<br/>production and non-production]:::risk
    TENANT --> SUB
    SUB --> AST007[Patient Portal<br/>AST-007]:::restricted
    SUB --> AST008[Appointment Booking<br/>AST-008]:::restricted
    SUB --> AST009[Remote Consultation<br/>AST-009]:::restricted
    SUB --> AST010[Patient Messaging<br/>AST-010]:::restricted

    classDef internal fill:#cfe2ff,stroke:#084298,color:#000
    classDef restricted fill:#f8d7da,stroke:#842029,color:#000
    classDef risk fill:#f5c6cb,stroke:#58151c,color:#000,stroke-width:3px
```

No scope exists here at which an Azure Policy or RBAC model could be assigned once and inherited across all four applications — this is the root cause behind observations 4.1–4.3 in the governance assessment.

## Diagram — Target State (AZG-REC-001)

```mermaid
flowchart TB
    TENANT[Entra ID Tenant — Westbridge Hospitals Trust]:::internal
    ROOT[Management Group: WHT Root<br/>Policy: Microsoft Cloud Security Benchmark]:::internal
    PROD[Management Group: Production]:::confidential
    NONPROD[Management Group: Non-Production]:::confidential

    TENANT --> ROOT
    ROOT --> PROD
    ROOT --> NONPROD

    PROD --> SUB1[Subscription: Patient-Facing Services]
    SUB1 --> RG1[Resource Group: Patient Portal<br/>AST-007]:::restricted
    SUB1 --> RG2[Resource Group: Appointment Booking<br/>AST-008]:::restricted
    SUB1 --> RG3[Resource Group: Remote Consultation<br/>AST-009]:::restricted
    SUB1 --> RG4[Resource Group: Patient Messaging<br/>AST-010]:::restricted

    NONPROD --> SUB2[Subscription: Dev/Test]

    classDef internal fill:#cfe2ff,stroke:#084298,color:#000
    classDef confidential fill:#fff3cd,stroke:#997404,color:#000
    classDef restricted fill:#f8d7da,stroke:#842029,color:#000
```

In the target state, RBAC and Azure Policy are assigned once at the Management Group level (closing AZG-REC-002 and AZG-REC-003) and inherited by every resource group beneath it, rather than being configured — or missed — application by application.

## Review and Maintenance

Reviewed alongside [../../12-Azure-Governance/121-azure_governance_assessment.md](../../12-Azure-Governance/121-azure_governance_assessment.md); the "Current State" diagram above should be deleted once AZG-REC-001 is delivered and only the target state remains accurate.
