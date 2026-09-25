
<img width="1916" height="907" alt="image" src="https://github.com/user-attachments/assets/cb4cc735-c27c-42f8-8160-6b16cd15afab" />

# IT-Grundschutz-Gap-Analysis-Remediation-Tracker
 Comprehensive BSI IT-Grundschutz Security Control Gap Analysis &amp; Remediation Tracker as an interactive HTML widget. 
 BSI IT-Grundschutz Security Control Gap Analysis & Remediation Tracker
The Problem: NIS2 compliance in Germany is heavily tied to the BSI IT-Grundschutz methodology (Standards 200-1 through 200-4). Organizations must demonstrate "state of the art" measures but often struggle to map their current controls to BSI requirements and track remediation. ​
Project Overview: Create an interactive frontend platform for SOC analysts that:
 
Maps an organization's current security controls against BSI IT-Grundschutz modules (e.g., INF.1 for building protection, APP for applications, NET for networks)
 
Identifies gaps using the BSI's risk analysis methodology (Standard 200-3)
 
Prioritizes remediation based on NIS2 entity classification (KRITIS vs. Essential vs. Important)
 
Tracks audit evidence collection for the 3-year BSI audit cycle
 
Visualizes compliance maturity with heatmaps and trend dashboards
Frontend Features: Interactive BSI control tree browser, gap heatmap by module, remediation ticket board, evidence document repository, and executive summary reports for board-level documentation (addressing §66 BSIG-E fiduciary duty requirements). ​
Why It Matters in Germany: BSI explicitly recommends IT-Grundschutz for NIS2 compliance, and the gap between ISO 27001 and full NIS2 compliance is a known challenge. This project shows deep familiarity with the German regulatory framework rather than generic cybersecurity tooling.

**The tracker includes six interactive views:**
Dashboard — KPI cards, 12-month maturity trend chart, and the BSI Standard 200-3 risk matrix (click any numbered cell for detailed risk analysis)
Control Tree — Expandable BSI module hierarchy (INF, APP, NET, SYS, ORG, IND) with progress bars and gap counts per sub-module
Gap Heatmap — Color-coded compliance grid; click any cell to see control details
Remediation Board — Kanban columns (Open, In Progress, In Review, Done) with priority-coded tickets mapped to BSI controls
Evidence Vault — Document repository with validity status for the 3-year BSI audit cycle
Executive Report — Board-ready summary addressing §66 BSIG-E fiduciary duty with action items, budget estimates, and compliance posture
All modals, filters, and navigation are fully functional. The data is scoped for a KRITIS Energy Sector entity under NIS2, reflecting the specific German regulatory framework.

## Architecture & Production Path

**Current implementation:** Zero-dependency, single-file vanilla JS (HTML/CSS/JS) —
deployable in restricted SOC environments with no build step or external dependencies.

**Production implementation path:** Where multi-user, real-time, or enterprise integration
requirements demand it, the production build is implemented in **React with D3.js/Chart.js**
for componentized state management, API-driven data layers, and role-based access —
migrating the current state-driven rendering pattern into a component architecture.

---
