# Incident Response Plan

**Organisation:** Westbridge Hospitals Trust (WHT)  
**Document Type:** Incident Response Plan  
**Owner:** Chief Information Security Officer (CISO)  
**Version:** 1.0  



# 1. Purpose

This plan sets out how WHT identifies, contains, eradicates, and recovers from cyber security incidents, and how it communicates about them internally and to regulators. It is the document already cited as existing evidence in [../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) §4.4 (CAF D1) and [../03-Current-State-Assessment/024-dsp_toolkit_review](../03-Current-State-Assessment/024-dsp_toolkit_review.md) §4.5 (DSPT Standard 6), and closes the gap previously tracked in `NAVIGATION.md`'s Known Cross-Reference Gap note.



# 2. Scope

This plan applies to all cyber security incidents affecting WHT information, systems, or services — clinical, corporate, and third-party-hosted where the Trust retains security responsibility, per [../01-Discovery/005-project_scope](../01-Discovery/005-project_scope.md). It does not cover general clinical safety incidents unrelated to cyber activity, which follow the Trust's separate clinical governance process, or business continuity invocation itself, which is addressed in [../10-Business-Continuity/](../10-Business-Continuity/).



# 3. Incident Classification

Incidents are classified using the same four-point scale already used for risk rating across the programme ([../04-Risk-Management/047-risk_methodology](../04-Risk-Management/047-risk_methodology.md) §2.2), so that incident severity and risk scoring speak a common language:

| Severity | Description | Example |
|---|---|---|
| Critical | Patient safety or major organisational impact; Critical-rated risk materialising | Ransomware affecting clinical systems (CR-001) |
| High | Significant operational or regulatory impact | Confirmed unauthorised access to Restricted data |
| Medium | Service impact requiring management attention | Isolated malware detection, contained quickly |
| Low | Minimal operational impact | Failed phishing attempt, no compromise |

Critical and High severity incidents trigger the escalation path in §7.



# 4. Roles & Responsibilities

Incident response roles follow the RACI already defined in [../05-Governance/052-roles_and_responsibilities](../05-Governance/052-roles_and_responsibilities.md) §4: the CISO is Responsible for incident response, the SIRO is Accountable, the DPO is Consulted on any incident involving personal data, and the Cyber Security Governance Group (CSGG) is kept Informed and reviews incident response governance as a standing function ([051-security_strategy](../05-Governance/051-security_strategy.md) §6). This plan does not redefine those roles — it operationalises them.

| Role | Incident Response Function |
|---|---|
| CISO | Incident Commander; leads response, coordinates Cyber Security Team, approves containment actions |
| SIRO | Accountable for the incident response decision; approves regulatory notification for High/Critical incidents |
| Cyber Security Team | Executes detection, containment, eradication, and recovery actions |
| DPO | Assesses personal data breach notification obligations; leads ICO liaison |
| CDIO | Coordinates clinical/operational system impact and recovery priorities |
| Clinical Safety Officer | Assesses and manages patient safety implications of any incident affecting clinical systems |
| Cyber Security Governance Group (CSGG) | Informed of all High/Critical incidents; reviews incident response effectiveness as a standing agenda item |



# 5. Detection & Reporting

Detection currently relies on the Security Monitoring Platform (AST-019) and the Managed Security Service Provider relationship (AST-035). Consistent with the current CAF position — C1 Security Monitoring and C2 Proactive Security Event Discovery are both rated **Not Achieved** ([../03-Current-State-Assessment/022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) §3) — this plan does not assume continuous, correlated detection capability. Until that gap closes (CAF REC-005), detection also depends on manual reporting: any member of staff who suspects a security incident must report it immediately to the Cyber Security Team via the Service Desk, per [../05-Governance/053-information_security_policy](../05-Governance/053-information_security_policy.md) §3.

All reported and detected incidents are logged, given a severity classification (§3), and assigned an Incident Commander from the Cyber Security Team.



# 6. Response Phases

This plan follows a standard five-phase incident lifecycle. The diagram below shows the sequence and the one key branch point — high-severity incidents trigger internal escalation (§7) in parallel with containment, not after it:

```mermaid
flowchart TD

    %% ==========================================================
    %% Incident Response Lifecycle - Project SentinelCare
    %% Depicts the 5-phase lifecycle in section 6, the severity
    %% branch point from section 3, the escalation trigger from
    %% section 7, and the feedback loop into 083-lessons_learned_report
    %% and the risk register described at the end of section 6.
    %% ==========================================================

    %% Entry point: an incident is reported by staff (section 5) or
    %% detected via the Security Monitoring Platform / MSSP (AST-019 / AST-035)
    A[Incident Reported or Detected]:::entry

    %% Identify phase: confirm it is a genuine incident and classify
    %% severity using the Low / Medium / High / Critical scale in section 3
    B[Identify:<br/>Confirm incident and classify severity per §3]:::phase

    %% Decision point: severity classification determines whether
    %% the escalation branch below is triggered
    C{Severity Classified<br/>High or Critical?}:::decision

    %% Escalation branch: runs IN PARALLEL with containment, not
    %% sequentially after it - see section 7 Internal Escalation
    D[Escalate to SIRO and CSGG per §7<br/>SIRO Accountable, CISO Responsible]:::escalation

    %% Contain phase: immediate action to limit spread/impact
    E[Contain:<br/>Segment, suspend, or isolate to limit impact]:::phase

    %% Eradicate phase: remove the root cause before recovery
    F[Eradicate:<br/>Remove root cause, confirm environment is clean]:::phase

    %% Recover phase: restore service, prioritising Critical assets
    G[Recover:<br/>Restore service, verify before return to clinical use]:::phase

    %% Post-Incident Review: mandatory for Medium/High/Critical incidents
    H[Post-Incident Review:<br/>Mandatory for Medium, High, or Critical incidents]:::phase

    %% Feedback loop outputs - where findings actually go
    I[083-lessons_learned_report<br/>Findings and action tracker]:::output
    J[049-risk_register<br/>Updated where the incident affects a scored risk]:::output

    A --> B
    B --> C

    %% "Yes" path: escalation runs alongside containment, shown as a
    %% parallel branch rather than a step in the main line below
    C -- Yes --> D
    D -.->|runs in parallel with| E

    %% "No" path: Low/Medium severity incidents proceed straight to containment
    C -- No --> E

    E --> F
    F --> G
    G --> H

    H --> I
    H --> J

    classDef entry fill:#e2e3e5,stroke:#41464b,color:#000
    classDef phase fill:#cfe2ff,stroke:#084298,color:#000
    classDef decision fill:#fff3cd,stroke:#997404,color:#000
    classDef escalation fill:#f8d7da,stroke:#842029,color:#000
    classDef output fill:#d1e7dd,stroke:#0f5132,color:#000
```

## Identify
Confirm whether a reported or detected event is a genuine security incident, classify its severity (§3), and assign an Incident Commander.

## Contain
Take immediate action to limit the spread or impact of the incident — network segmentation, account suspension, system isolation — balancing containment speed against preserving evidence and maintaining critical clinical services.

## Eradicate
Remove the root cause of the incident (malware, unauthorised access, misconfiguration) and confirm the environment is clean before recovery begins.

## Recover
Restore affected systems and services to normal operation, prioritising Critical-rated assets per [../02-Asset-Management/022-master_assets_register.xlsx](../02-Asset-Management/022-master_assets_register.xlsx), with verification before systems are returned to clinical use.

## Post-Incident Review
Every Medium, High, or Critical incident undergoes a post-incident review, feeding findings into [083-lessons_learned_report](083-lessons_learned_report.md) and, where relevant, into the risk register ([../04-Risk-Management/049-risk_register](../04-Risk-Management/049-risk_register.md)).



# 7. Communication & Notification

## Internal Escalation

High and Critical severity incidents are escalated immediately to the SIRO (Accountable) and reported to the CSGG at its next meeting, or convened out-of-cycle for Critical incidents, following the same escalation path CSGG uses for matters outside its mandate ([../05-Governance/052-roles_and_responsibilities](../05-Governance/052-roles_and_responsibilities.md) §3): SIRO → Audit and Risk Committee → Trust Board.

## Regulatory Notification

| Trigger | Notify | Timeframe | Owner |
|---|---|---|---|
| Personal data breach with risk to individuals | Information Commissioner's Office (ICO) | Within 72 hours of becoming aware | DPO |
| Incident affecting NHS systems or shared care records | NHS England / Integrated Care Board (ICB) | As soon as practicable | CISO |
| Significant cyber incident (NIS Regulations scope) | National Cyber Security Centre (NCSC) | As soon as practicable | CISO |
| Incident with clinical safety impact | Care Quality Commission (CQC), via existing clinical governance process | Per clinical governance timelines | Clinical Safety Officer |



# 8. Ransomware-Specific Procedures

Ransomware is the Trust's highest-scored risk (CR-001, Likelihood 5 × Impact 5 = 25, Critical; Risk Owner CDIO, Treatment Owner CISO; treatment status **In Progress** — [../04-Risk-Management/049-risk_register](../04-Risk-Management/049-risk_register.md) §5). In addition to the standard response phases (§6), a suspected or confirmed ransomware incident triggers:

- Immediate network segmentation to prevent lateral spread, ahead of full containment assessment.
- Activation of offline backup validation and restoration procedures, without paying any ransom demand.
- Automatic classification as Critical severity and immediate SIRO/CSGG escalation (§7), regardless of initially observed scope.
- Coordination with [../10-Business-Continuity/](../10-Business-Continuity/) for clinical service continuity if EPR or other Critical-rated systems are affected.

The diagram below shows how this overrides the normal §6 sequence — segmentation and classification happen immediately and automatically rather than in the assessed order §6 otherwise implies:

```mermaid
flowchart LR

    %% ==========================================================
    %% Ransomware Fast-Path Override - Project SentinelCare
    %% Shows how a suspected ransomware incident overrides the
    %% normal section 6 sequence (Identify then Contain). Compare
    %% against the full lifecycle diagram in section 6.
    %% ==========================================================

    subgraph NORMAL["Normal Sequence (§6)"]
        direction LR
        %% Under §6, Identify (assess and classify) completes
        %% before Contain begins
        N1[Identify:<br/>Assess and classify severity]:::phase --> N2[Contain]:::phase
    end

    subgraph FASTPATH["Ransomware Fast-Path (§8)"]
        direction LR
        %% Entry: any suspicion of ransomware, not a confirmed incident,
        %% is enough to trigger this path
        R1[Suspected Ransomware]:::entry

        %% Segmentation starts immediately - it does NOT wait for
        %% Identify to finish classifying severity first
        R2[Immediate Network Segmentation<br/>starts before classification completes]:::escalation

        %% Classification still happens, but the outcome is fixed in
        %% advance: ransomware is always Critical, never assessed as
        %% Medium or Low regardless of initially observed scope
        R3[Classify as Critical<br/>automatic, not assessed]:::phase

        %% These two actions run at the same time, not one after the
        %% other - escalation does not wait for backups to be checked,
        %% and backup validation does not wait for SIRO/CSGG sign-off
        R4[Escalate to SIRO / CSGG §7]:::escalation
        R5[Validate Offline Backups<br/>no ransom payment]:::phase

        R6[Contain]:::phase

        R1 --> R2
        R2 --> R3
        R3 --> R4
        R3 --> R5
        R4 --> R6
        R5 --> R6
    end

    classDef entry fill:#e2e3e5,stroke:#41464b,color:#000
    classDef phase fill:#cfe2ff,stroke:#084298,color:#000
    classDef escalation fill:#f8d7da,stroke:#842029,color:#000
```

Consistent with [../04-Risk-Management/046-risk_treatment_plans](../04-Risk-Management/046-risk_treatment_plans.md) §4.2, this plan does not assume ransomware risk can be fully eliminated: even with these procedures embedded, CR-001's expected residual rating remains **High**, not Low or Medium.



# 9. Testing & Exercise Cadence

This plan is exercised at least annually, closing [022-caf_assessment](../03-Current-State-Assessment/022-caf_assessment.md) REC-006 ("formalise a testing and lessons-learned cadence for the Incident Response and Business Continuity Plans"). The first exercise under this plan is recorded in [082-ransomware_tabletop_exercise](082-ransomware_tabletop_exercise.md); findings and actions are tracked in [083-lessons_learned_report](083-lessons_learned_report.md). Ad hoc exercises are also triggered following any material change to the Trust's threat landscape ([../04-Risk-Management/044-threat_assessment](../04-Risk-Management/044-threat_assessment.md)) or digital estate.



# 10. Review and Maintenance

This plan is reviewed annually by the CISO and ratified by the CSGG, or sooner following a Critical-severity incident, a material change to the Trust's digital estate, or findings from an exercise or real incident that indicate the plan itself needs revision.
