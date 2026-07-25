# Security Metrics — KPI Definitions

**Organisation:** Westbridge Hospitals Trust (WHT)
**Document Type:** Metrics Reference
**Owner:** CISO (Chief Information Security Officer)
**Version:** 1.0
**Audience:** Trust Board and other non-technical readers

## 1. Purpose

This document explains, in plain English, the small set of numbers ("KPIs" — Key Performance Indicators) the Trust Board uses to track whether cyber security is getting better or worse. Each number is explained in a way that answers one question: *what does this actually tell the Board, and why should they care?* The dashboards described in [132-powerbi_dashboards](132-powerbi_dashboards.md) display these numbers visually; this document is where their meaning is defined so everyone reading a dashboard means the same thing by the same number.

## 2. How to Read This Document

Each KPI below is described the same way:

- **What it measures** — in everyday language, not technical jargon
- **Why it matters** — what it tells the Board about patient safety, regulatory standing, or organisational risk
- **Where the number comes from** — the underlying document it is calculated from, so anyone can check the working
- **What "good" looks like** — a simple target, and what colour (Red/Amber/Green) it shows as on the dashboard

## 3. Key Performance Indicators

### 3.1 Overall Risk Position

**What it measures:** How many of the Trust's top cyber security risks are rated Critical or High, out of the twelve risks the Trust actively tracks.

**Why it matters:** A rising number means more things could seriously harm patients or disrupt services if nothing is done. A falling number means the Trust's improvement work is paying off.

**Where the number comes from:** [../04-Risk-Management/049-risk_register.md](../04-Risk-Management/049-risk_register.md).

**What good looks like:** Green if 2 or fewer risks are Critical/High; Amber if 3–5; Red if more than 5.

### 3.2 Time to Fix Serious Security Weaknesses

**What it measures:** How quickly the Trust fixes the most dangerous technical weaknesses ("vulnerabilities") once they're found — for example, a piece of software with a known flaw a hacker could exploit. The Trust has committed to fixing the most dangerous weaknesses within 14 days, and the next most dangerous within 30 days.

**Why it matters:** The longer a serious weakness stays open, the longer there is a real chance of an attacker using it to get in. This is one of the clearest "are we actually doing the work" numbers the Board has.

**Where the number comes from:** [../09-Security-Operations/091-vulnerability_register.md](../09-Security-Operations/091-vulnerability_register.md) §6 (the Trust's agreed fix-it timescales).

**What good looks like:** Green if all fixes are on time; Amber if a small number are late but being actively worked; Red if any are significantly overdue with no plan.

### 3.3 Staff Who Have Completed Security Training

**What it measures:** The percentage of staff who have completed mandatory cyber security awareness training (recognising phishing emails, protecting passwords, reporting incidents).

**Why it matters:** Most successful cyber attacks start with tricking a person, not breaking technology. Trained staff are the Trust's first line of defence.

**Where the number comes from:** [../04-Risk-Management/046-risk_treatment_plans.md](../04-Risk-Management/046-risk_treatment_plans.md) (tracked against CR-008, the risk of staff being tricked by phishing or social engineering).

**What good looks like:** Green if 95% or more of staff are up to date; Amber if 80–94%; Red if below 80%.

### 3.4 Regulatory Standing (DSPT)

**What it measures:** Whether the Trust would currently pass its annual data security check-up with NHS England, called the Data Security and Protection Toolkit (DSPT). Every NHS organisation has to complete this once a year.

**Why it matters:** Failing this check can restrict the Trust's access to shared national NHS systems (such as the ability to view a patient's shared care record from another hospital), so it is a direct, practical consequence — not just a paperwork exercise.

**Where the number comes from:** [../03-Current-State-Assessment/024-dsp_toolkit_review.md](../03-Current-State-Assessment/024-dsp_toolkit_review.md).

**What good looks like:** Green = "Standards Met"; Amber = "Standards Not Met" but with an agreed improvement plan; Red = "Standards Not Met" with no agreed plan.

### 3.5 Security Incidents

**What it measures:** How many cyber security incidents happened this quarter, split by how serious they were, and how quickly the Trust responded.

**Why it matters:** This tells the Board what is actually happening, not just what could happen. A pattern of incidents in the same area often points to a control that needs fixing.

**Where the number comes from:** [../08-Incident-Management/081-incident_response_plan.md](../08-Incident-Management/081-incident_response_plan.md).

**What good looks like:** There is no fixed "good number" of incidents — the Board instead watches the trend over time and how quickly each one was contained.

### 3.6 Suppliers Without a Completed Security Check

**What it measures:** How many of the Trust's IT and clinical technology suppliers have not yet had their security checked and signed off.

**Why it matters:** A supplier with weak security can be a back door into the Trust's systems, even if the Trust's own defences are strong. This is currently one of the Trust's weakest areas (see [../04-Risk-Management/049-risk_register.md](../04-Risk-Management/049-risk_register.md), CR-006).

**Where the number comes from:** [../02-Asset-Management/025-supplier_register.xlsx](../02-Asset-Management/025-supplier_register.xlsx).

**What good looks like:** Green if fewer than 10% of suppliers are unchecked; Amber if 10–25%; Red if more than 25%.

## 4. Review and Maintenance

These definitions are reviewed every six months by the CISO, or sooner if a KPI's source document materially changes (for example, a new risk methodology or a revised DSPT assertion set). Changes are agreed with the Cyber Security Governance Group (CSGG) before being reflected on the dashboards in [132-powerbi_dashboards](132-powerbi_dashboards.md), so the numbers the Board sees never silently change meaning between reports.
