# Data Flow Diagram — Third-Party Data Exchange

**Organisation:** Westbridge Hospitals Trust (WHT)  
**Document Type:** Data Flow Diagram  
**Owner:** Procurement Director / Data Protection Officer (DPO)  
**Version:** 1.0  

## Purpose

This diagram shows data flows between the Trust's core clinical systems and the external vendors that support them, plus the Trust's managed security service provider. It is referenced by [063-data_lineage_assessment](../063-data_lineage_assessment.md) §6, and reflects the vendor dependencies identified in [../../04-Risk-Management/043-third_party_risks](../../04-Risk-Management/043-third_party_risks.md).

## Colour Convention

Trust-owned systems are coloured Restricted (red); external supplier organisations are coloured as external actors (grey), per [061-data_classification](../061-data_classification.md) §4 — the full legend is explained once in [063-data_lineage_assessment](../063-data_lineage_assessment.md) §5.

## Diagram

```mermaid
flowchart LR

    EPR[Electronic Patient Record EPR]:::restricted
    LIS[Laboratory Information System LIS]:::restricted
    RIS[Radiology Information System / PACS]:::restricted
    THEATRE[Theatre Management System]:::restricted
    SOC[Security Operations Centre SOC]:::restricted

    ORACLE[Oracle Health<br/>EPR Vendor]:::external
    INTERSYSTEMS[InterSystems<br/>LIS Vendor]:::external
    SECTRA[Sectra<br/>RIS/PACS Vendor]:::external
    BLUESPIER[Bluespier International<br/>Theatre Management Vendor - SUP-005]:::external
    MSSP[Managed Security Service Provider MSSP]:::external

    ORACLE -->|Vendor Support, Patches, Maintenance Access| EPR
    INTERSYSTEMS -->|Vendor Support, Patches, Maintenance Access| LIS
    SECTRA -->|Vendor Support, Patches, Maintenance Access| RIS
    BLUESPIER -->|Vendor Support, Patches, Maintenance Access| THEATRE

    SOC -->|Security Event Data, Alerts| MSSP
    MSSP -->|Threat Intelligence, Incident Escalation| SOC

    classDef restricted fill:#f8d7da,stroke:#842029,color:#000
    classDef external fill:#e2e3e5,stroke:#41464b,color:#000
```

## Notes

Bluespier International (SUP-005) is flagged "Approaching Renewal" while the Theatre Management System it supports is on legacy vendor-extended support — the compounded position tracked as [043-third_party_risks](../../04-Risk-Management/043-third_party_risks.md) TPR-001 and REC-002. This diagram makes that single-vendor dependency visible: loss of Bluespier support directly affects Theatre Management data exchange with no documented fallback vendor.
