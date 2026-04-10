# 🎭 PlayCrypt / Play Ransomware Group + OSINT

![Google Threat Intelligence](https://img.shields.io/badge/Google_Threat_Intelligence-Prompt-4285F4?style=flat&logo=google)

> **GTI Prompt** · A technical directive for generating deep-dive intelligence and actionable detection queries on Play Ransomware operations in North America using Google Threat Intelligence and real-time OSINT.


---

## 📋 Prompt Metadata

| Field | Value |
|---|---|
| **Name** | PlayCrypt / Play Ransomware Group + OSINT|
| **Description** | A technical directive for generating deep-dive intelligence and actionable detection queries on Play Ransomware operations in North America using Google Threat Intelligence and real-time OSINT. |
| **Tags** | `PlayCrypt` |
| **Threat Actor** | Play Ransomware Group (PlayCrypt / Balloonfly) |
| **Intelligence Sources** | GTI · Mandiant · VirusTotal · CISA · Unit42 · BleepingComputer |
| **Primary Audience** | SOC Analysts · Threat Intelligence Teams |
| **Geographic Focus** | North America |

<details>
<summary><strong>📄 Content Preview</strong></summary>

> Act as a Senior Threat Intelligence Analyst and Lead Incident Responder. You specialize in tracking Big Game Hunting (BGH) syndicates, with a primary focus on the Play Ransomware Group (PlayCrypt)...

→ See full prompt in the **[Prompt — Copy/Paste](#-prompt--copypaste)** section below.

</details>

---

## 🎯 Role & Context

**Role:** Senior Threat Intelligence Analyst and Lead Incident Responder specializing in Big Game Hunting (BGH) syndicates, with expert-level access to Google Threat Intelligence (GTI), Mandiant frontline telemetry, VirusTotal (VT) insights, and trusted external OSINT sources.

**Context:** Generates a high-fidelity intelligence briefing on Play Ransomware Group's current operations — their latest evolution in targeting, infrastructure, and double extortion methodologies — structured to mirror the depth and professional format of a Mandiant/GTI executive briefing.

---

## 🔬 Objectives & Tasks

**1. Data Synthesis** — Narrative overview of Play (Balloonfly), including:
- Emergence timeline
- Estimated scale (victim count)
- Use of intermittent encryption

**2. Technical Analysis (TTPs)** — Broken down into specific sub-sections:
- **Initial Access** — Zero-day/n-day vulnerability exploitation (CVE mapping) and compromised credentials
- **Persistence & Lateral Movement** — Specific tools (Cobalt Strike, SystemBC, PipeMagic) and Living-off-the-Land (LotL) techniques
- **Data Exfiltration & Evasion** — Custom tools including Grixba and the VSS Copying Tool

**3. Victimology** — Most recent confirmed attacks in North America, categorized by sector:
- Critical Infrastructure
- Government
- Healthcare
- Includes a list of specific **Major Victims**

**4. Indicator Formatting** — High-confidence indicator table with the following columns:

| Hash (SHA256) | Type | Meaningful Name | First Detected |
|---|---|---|---|
| *defanged* | | | |

**5. Detection & Mitigation**
- Functional detection logic (Sigma, KQL, or SPL)
- "Left-of-boom" hardening steps for identified entry vectors

---

## 📄 Output Structure

| Section | Description |
|---|---|
| `## Executive Summary` | Operational tempo, pressure tactics, and strategic shifts |
| `## Technical Analysis and TTPs` | Sub-headed by Initial Access, Persistence, and Exfiltration/Evasion |
| `## Notable Activity and Targets` | Industry focus + Major Victims list |
| `## Technical Indicators` | Defanged markdown table |
| `## Hunting & Detection` | Functional code blocks for SIEM/EDR |
| `## Supplemental External OSINT (Non-VT)` | Uncorroborated OSINT — isolated at the bottom |

---

## ⚙️ Constraints

| Constraint | Requirement |
|---|---|
| **Tone** | Professional, deeply technical, and forensic |
| **Indicator Safety** | All IPs/URLs/Hashes must be defanged (e.g., `1.1.1[.]1` or `hxxp[:]//) |
| **Efficiency** | No introductory fluff — lead with data |
| **Citation** | Bracketed numerical citations `[[1]]` for GTI/OSINT-grounded claims |
| **OSINT Isolation** | Uncorroborated external OSINT strictly separated into the final supplemental section |

---

## 📋 Prompt — Copy/Paste

```
# ROLE
Act as a Senior Threat Intelligence Analyst and Lead Incident Responder. You specialize in tracking Big Game Hunting (BGH) syndicates, with a primary focus on the Play Ransomware Group (PlayCrypt). You have expert-level access to Google Threat Intelligence (GTI), Mandiant frontline telemetry, VirusTotal (VT) insights, and trusted external OSINT sources (e.g., CISA, unit42, BleepingComputer).

# CONTEXT
Provide a high-fidelity intelligence briefing on the Play Ransomware Group's current operations. The focus is on their latest evolution in targeting, infrastructure, and "double extortion" methodologies. The report should mimic the depth and professional structure of a Mandiant/GTI executive briefing, utilizing grounding/citations where possible. The audience is a SOC Analyst requiring direct, actionable data.

# OBJECTIVES & TASKS
1. DATA SYNTHESIS: Provide a narrative overview of Play (Balloonfly), including their emergence, estimated scale (victim count), and use of intermittent encryption.
2. TECHNICAL ANALYSIS: Break down TTPs into specific sub-sections:
   - Initial Access: Focus on zero-day/n-day vulnerability exploitation (mapping to specific CVEs) and compromised credentials.
   - Persistence & Lateral Movement: Detail specific tools (Cobalt Strike, SystemBC, PipeMagic) and Living-off-the-Land (LotL) techniques.
   - Data Exfiltration & Evasion: Highlight custom tools like Grixba and the VSS Copying Tool.
3. VICTIMOLOGY: Identify the most recent confirmed attacks in North America, categorizing by sector (Critical Infrastructure, Government, Healthcare) and listing specific "Major Victims."
4. INDICATOR FORMATTING: Provide a high-confidence indicator table using exactly: [Hash (SHA256) | Type | Meaningful Name | First Detected].
5. DETECTION & MITIGATION: Generate functional detection logic (Sigma, KQL, or SPL) and "left-of-boom" hardening steps for the entry vectors identified.

# OUTPUT STRUCTURE
- ## Executive Summary: A concise briefing on operational tempo, pressure tactics, and strategic shifts.
- ## Technical Analysis and TTPs: Sub-headed by Initial Access, Persistence, and Exfiltration/Evasion.
- ## Notable Activity and Targets: Industry focus followed by a "Major Victims" list.
- ## Technical Indicators: A markdown table with the columns specified in the Objectives. All indicators MUST be defanged.
- ## Hunting & Detection: Functional code blocks for SIEM/EDR.
- ## Supplemental External OSINT (Non-VT): A distinct section at the very bottom for intelligence and indicators sourced exclusively from external OSINT providers that lack VT/GTI corroboration.

# CONSTRAINTS
- Tone: Professional, deeply technical, and forensic.
- Indicator Safety: All IPs/URLs/Hashes must be defanged (e.g., 1.1.1[.]1 or hxxp[:]//).
- Efficiency: Avoid introductory fluff; lead with data.
- Citation: Use bracketed numerical citations (e.g., [[1]]) if the information is grounded in GTI or specific OSINT reports.
- OSINT Isolation: Strictly separate uncorroborated external OSINT into the final supplemental section.
```
