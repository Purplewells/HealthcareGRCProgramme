# Data Flow Diagram — Patient Portal and Healthcare Interoperability Platform

**Organisation:** Westbridge Hospitals Trust (WHT)  
**Document Type:** Data Flow Diagram  
**Owner:** Data Protection Officer (DPO) / Information Governance Team  
**Version:** 1.0  

## Purpose

This diagram shows how patient information moves between external users, digital services, clinical systems, and supporting security controls for the Patient Portal and Healthcare Interoperability Platform. It is referenced by [062-data_protection_impact_assessment](../062-data_protection_impact_assessment.md) §9 and [063-data_lineage_assessment](../063-data_lineage_assessment.md) §5.

## Colour Convention

Nodes are coloured by the classification of the data they process, per [061-data_classification](../061-data_classification.md) §4. The full legend is explained once in [063-data_lineage_assessment](../063-data_lineage_assessment.md) §5:

- 🔴 Restricted — patient/clinical data
- 🔵 Internal — security, monitoring, and audit data
- ⚪ External Actor — outside the Trust's classification scheme

## Diagram

```mermaid
flowchart TD

    A[Patient]:::external -->|Authentication and Access Request| B[Patient Portal]:::restricted

    B -->|Secure HTTPS Connection| C[API Gateway]:::restricted

    C -->|OAuth 2.0 / OpenID Connect Authentication| D[FHIR API Integration Layer]:::restricted

    D -->|Secure API Exchange| E[Electronic Patient Record EPR]:::restricted

    D -->|Clinical Data Exchange| F[Laboratory Information System LIS]:::restricted

    D -->|Diagnostic Data Exchange| G[Radiology Information System RIS]:::restricted

    D -->|Medication Information Exchange| H[Pharmacy Management System]:::restricted

    D -->|Appointment and Messaging Data| I[Patient Communication Services]:::restricted


    E --> J[Clinical Users]:::restricted
    F --> J
    G --> J
    H --> J


    C --> K[API Security Monitoring]:::internal

    D --> K

    K --> L[Security Operations Centre SOC]:::internal

    B --> M[Audit Logging]:::internal

    C --> M

    D --> M

    E --> M
    M --> N[Information Governance Monitoring]:::internal

    classDef external fill:#e2e3e5,stroke:#41464b,color:#000
    classDef restricted fill:#f8d7da,stroke:#842029,color:#000
    classDef internal fill:#cfe2ff,stroke:#084298,color:#000
```

## GRC Relevance

| DPIA Requirement | Mermaid Component |
|---|---|
| Identify data sources | Patient Portal |
| Identify processing systems | FHIR API, EPR, LIS, RIS |
| Identify recipients | Clinical Users |
| Identify security controls | API Gateway, Authentication, Logging |
| Identify monitoring capability | SOC and IG Monitoring |
