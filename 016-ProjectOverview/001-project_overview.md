# Project SentinelCare — Portfolio Overview, Methodology and Lessons Learned

**Prepared by:** Ben Aduohene
**Document Type:** Portfolio Retrospective
**Version:** 1.0

> **A note on what this document is.** In this repository, "the Trust," "the CISO," "the programme" refer to a fictional NHS organisation, Westbridge Hospitals Trust (WHT). 

## 1. Project Overview

**Project SentinelCare** is a simulated end-to-end Cyber Security Governance, Risk and Compliance (GRC) improvement programme for a fictional NHS acute trust, Westbridge Hospitals Trust. It was built to demonstrate, what a GRC practitioner produces across a full programme lifecycle.

The programme covers:

- **Discovery and context** — executive brief, business context, stakeholders, assumptions and constraints
- **Asset management** — a 35-asset register across eight categories, ownership model, criticality/classification schemes
- **Current-state assessment** — NCSC Cyber Assessment Framework (CAF), ISO/IEC 27001, and NHS DSPT assessments, plus an overall maturity roll-up
- **Risk management** — a central risk register plus domain-specific deep dives (cloud, medical devices, third-party, threat assessment)
- **Governance, information governance, and compliance** — policies, roles and RACI, data classification, DPIAs, UK GDPR assessment
- **Incident management, security operations, and business continuity** — response plans, vulnerability register, patch management, DR/BC plans
- **Independent internal audit** — testing the self-assessed positions in the earlier phases against PSIAS and the Three Lines Model
- **Azure governance, security metrics, and a consolidated roadmap** — cloud-specific governance, KPI/dashboard definitions, and a single sequenced improvement plan that ties every recommendation raised across the whole programme back to one prioritised set of initiatives.
- **Evidence** — supporting diagrams and reusable templates

The whole thing is explicitly framed, at the repository root, as a "simulated cybersecurity consultancy engagement... for a fictional NHS healthcare provider" — every finding, risk score, and recommendation is invented, but the *structure*, cross-referencing discipline, and reasoning are built the way a real engagement's documentation should be.

                                                                                                                            
                                                                                                                            ## 3. Project Steps Taken

The programme was built phase by phase, but not linearly in the way the folder numbers suggest — later phases repeatedly required going back to earlier ones to check a fact rather than re-deriving it. The general pattern per phase was:

1. **Read what already exists** — the current folder's stub files, the README status table, and every document elsewhere in the repository that the new document would need to reference or be consistent with (asset IDs, risk IDs, prior findings).
2. **Clarify scope before writing** — for anything with a real decision in it (file naming, what "simple language" means for a given audience, whether to fabricate evidence artefacts or not), ask rather than assume. See §4.
3. **Write against a checked structure** — assessment documents through the `write-assessment-document` skill and its validator; policies and standards against the metadata-header/numbered-section pattern already established by the earliest phases, so a reader can't tell which phase was authored first from formatting alone.
4. **Cross-link, don't duplicate** — a fact is stated once, in its owning document, and referenced by ID (`CR-004`, `AST-029`, `AUD-001`) everywhere else it's relevant, the same discipline a real risk register and audit trail need to stay trustworthy.
5. **Update the indexes** — every phase README and the top-level `NAVIGATION.md` were kept in lockstep with actual document status, so the navigation table is never aspirational.

The most recent phases — Azure Governance, Security Metrics, the RoadMap, and Evidence — were built in this order specifically because each depended on the one before: the Azure Governance assessment identified the management group/RBAC gap; the Conditional Access and Secure Score documents then had something concrete to close; the RoadMap consolidated *those* recommendations along with everything raised in the previous eleven phases; and the Evidence phase visualised the specific structural findings (the flat Azure subscription, the identity single point of failure, the governance reporting structure) that the RoadMap now tracks.

## 4. Lessons Learned

**A GRC programme's biggest risk is internal contradiction, not missing content.** The most consequential finding of this whole exercise wasn't in any single document — it was noticing, while building the RoadMap, that the same recommendation ID (`REC-001`) had been reused with a completely different meaning in more than fifteen separate documents. That's exactly the kind of thing the internal audit phase (§5 of `111-internal_audit_report.md`) exists to catch in a real programme, and it only became visible by searching across documents rather than reading any one of them carefully. Each tagged back to every source it closes — is now the RoadMap's actual design, not an afterthought.

**Naming conventions matter more than they look like they should.** Every phase in this repository follows a `NN-Phase-Name/NNM-snake_case_document.md` pattern. Several folders in this exercise (Azure Governance, Security Metrics, the RoadMap) started as inconsistent, unnumbered stub files — a small thing, but it's exactly the kind of inconsistency that makes a real document repository hard to navigate at scale, and it was worth pausing to fix before adding content on top of it.

**Clarify scope at decision points, not just at the start.** The most useful moments in this build weren't the big upfront questions — they were the small ones asked mid-task: which naming convention to use, whether to consolidate or preserve duplication, where a new document should physically live. Each of those, answered wrong, would have meant redoing real work later.

## 5. Executive Summary

This repository is a complete, internally consistent 15-phase Cyber Security GRC programme for a fictional NHS trust, built to demonstrate GRC domain knowledge (CAF, ISO 27001, DSPT, risk management, incident response, business continuity, Azure/cloud governance). Eighty-plus Markdown documents and eleven formatted spreadsheets are held to a single validated structure, cross-reference each other by stable ID rather than duplicating facts, and — critically — the programme catches and corrects its own inconsistencies (duplicate recommendation IDs, stale status tables, broken cross-references after a rename) the way a real audit function should. The methodology on display — read before writing, clarify before assuming, validate before claiming done, and draw an explicit line between fiction and fabricated evidence — is the same methodology intended for real engagement work.

## 6. Review and Maintenance

This document reflects the state of the programme as of the most recent session that touched it. It should be updated whenever a new phase or a structural change (renaming, re-scoping, or re-sequencing existing phases) is made, so it remains an accurate account of how the repository was actually built rather than a snapshot that quietly goes stale.
