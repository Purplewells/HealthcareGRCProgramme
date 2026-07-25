# Security Metrics — Dashboards Overview

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Dashboard Reference
**Owner:** CISO (Chief Information Security Officer)
**Version:** 1.0
**Audience:** Trust Board and other non-technical readers

## 1. Purpose

The Trust uses four dashboards, built in Microsoft Power BI (a tool for turning spreadsheet data into charts and visual reports), to show cyber security information to different audiences. This document explains what each dashboard is for, who it's for, and what the numbers on it mean — in plain English. The definition of every number shown is set out in [131-kpi_definitions](131-kpi_definitions.md); this document is about what each dashboard shows and to whom, not how each number is calculated.

## 2. The Four Dashboards

### 2.1 Executive Dashboard

**Who it's for:** The Trust Board and senior leadership.

**What it shows:** A single-page, at-a-glance summary — the handful of numbers described in [131-kpi_definitions](131-kpi_definitions.md) §3, each shown as Red, Amber, or Green so a reader can tell in seconds whether something needs their attention. It answers the question a Board member actually has: *is cyber security getting better, staying the same, or getting worse, and is there anything I need to act on?*

**How often it's updated:** Monthly, ahead of each Cyber Security Governance Group (CSGG) meeting.

### 2.2 Cyber Risk Dashboard

**Who it's for:** The CISO and the Cyber Security Governance Group — the people who own and manage the Trust's risks day to day.

**What it shows:** More detail than the Executive Dashboard — every tracked risk from the [risk register](../04-Risk-Management/049-risk_register.md), how severe each one is, whether it's getting better or worse, and how the work to fix it (the "treatment plan") is progressing. Where the Executive Dashboard tells the Board *something needs attention*, this dashboard tells the CISO *exactly what, and what's being done about it*.

**How often it's updated:** Monthly, alongside the underlying risk register review.

### 2.3 Compliance Dashboard

**Who it's for:** The CISO, Data Protection Officer, and anyone preparing regulatory submissions.

**What it shows:** How the Trust is doing against the external rules it has to follow — the NHS Data Security and Protection Toolkit (DSPT), the NCSC Cyber Assessment Framework (CAF), and ISO/IEC 27001 (an international information security standard). It shows each requirement as met, partly met, or not met, so gaps are visible well before an annual submission deadline rather than being discovered at the last minute.

**How often it's updated:** Quarterly, or immediately before a regulatory submission is due.

### 2.4 Supplier Risk Dashboard

**Who it's for:** Procurement, the CISO, and Information Asset Owners (the people accountable for specific systems or data).

**What it shows:** How well-checked the Trust's suppliers are from a security point of view — which suppliers handle the most sensitive information, which have completed a security check, and which haven't. This exists because a weak supplier can be used as a way into the Trust's own systems, and the Trust currently has more suppliers than it has completed checks for (see [../04-Risk-Management/049-risk_register.md](../04-Risk-Management/049-risk_register.md), CR-006).

**How often it's updated:** Quarterly, alongside the supplier register review.

## 3. How the Dashboards Relate to Each Other

The four dashboards are the same underlying data, shown at different levels of detail for different readers — not four separate data sets. The Executive Dashboard is a summary of the Cyber Risk Dashboard; the Compliance and Supplier Risk dashboards each zoom into one specific area (regulatory standing, and third-party risk) that also feeds into the overall risk picture. If a number on the Executive Dashboard looks wrong, the explanation is always traceable by drilling into the more detailed dashboard underneath it.

## 4. Where the Files Live

The Power BI report files (`.pbix`) referenced by these dashboards are stored alongside this documentation. Each dashboard's underlying data connects directly to the source documents listed in [131-kpi_definitions](131-kpi_definitions.md) §3, so the dashboard numbers and the source registers should always match — if they don't, that is treated as a data-refresh fault to be fixed, not a discrepancy to explain away.

## 5. Review and Maintenance

Dashboard content and layout are reviewed every six months by the CISO alongside the KPI definitions in [131-kpi_definitions](131-kpi_definitions.md), or sooner if the Board asks for a different view of the data. Any change to what a dashboard shows is agreed with the Cyber Security Governance Group first.
