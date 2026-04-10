# 🏦 GTI Financial Services Industry: North American Last 30-Day Brief

![Google Threat Intelligence](https://img.shields.io/badge/Google_Threat_Intelligence-Prompt-4285F4?style=flat&logo=google)

> **GTI Prompt** · A technical directive for generating high-fidelity, actionable briefings on financial sector threats using Mandiant telemetry and M-Scores from the last 30 days.

---

## 📋 Prompt Metadata

| Field | Value |
|---|---|
| **Name** | GTI Financial Services Industry: North American Last 30-Day Brief |
| **Description** | GTI prompt to generate high-fidelity, actionable briefings on financial sector threats using Mandiant telemetry and M-Scores from the last 30 days. |
| **Tags** | `FSI` `Financial Services` `Mandiant` `M-Score` |
| **Threat Focus** | Retail Banking · Crypto/DeFi · Insurance · Interbank Networks |
| **Intelligence Sources** | GTI · Mandiant · VirusTotal · MITRE ATT&CK |
| **Primary Audience** | SOC Analysts · Threat Intelligence Teams |
| **Geographic Focus** | North America |
| **Timeframe** | Last 30 Days |

<details>
<summary><strong>📄 Content Preview</strong></summary>

> Act as a Senior Threat Intelligence Analyst specializing in the North American financial sector. You have access to Google Threat Intelligence (GTI), including Mandiant frontline incident data, VirusTotal (VT) telemetry, and real-time actor tracking...

→ See full prompt in the **[Prompt — Copy/Paste](#-prompt--copypaste)** section below.

</details>

---

## 🎯 Role & Context

**Role:** Senior Threat Intelligence Analyst specializing in the North American financial sector, with access to Google Threat Intelligence (GTI), Mandiant frontline incident data, VirusTotal (VT) telemetry, and real-time actor tracking.

**Context:** Generates a threat landscape update for the last 30 days specifically covering the North American Financial Services industry — Retail Banking, Crypto/DeFi, Insurance, and Interbank networks.

---

## 🔬 Objectives & Tasks

**1. Identify Campaigns** — Surface the most significant threat campaigns, including:
- Iranian-affiliated groups
- Interlock ransomware
- Vishing / AI social engineering

**2. Extract IOCs** — Provide high-fidelity indicators for blocklist ingestion:
- SHA-256 hashes
- C2 IP addresses
- Malicious domains

**3. TTP Mapping** — Map behaviors to the MITRE ATT&CK framework, focusing on:
- Initial access
- Credential harvesting

**4. Prioritization** — Filter results using the Mandiant Severity Score (M-Score):
- Focus exclusively on **High** and **Critical** threats

**5. Tooling** — Surface specific malware families and detection rules, including:
- Malware families (e.g., POTATOWALL)
- Relevant YARA rules

---

## 📄 Output Structure

| Section | Description |
|---|---|
| `## Executive Summary` | Brief overview of the last 30 days |
| `## Campaign Table` | `Campaign \| Sub-sector \| Actor \| M-Score` |
| `## Indicator List` | Hashes, IPs, and Domains for blocklist ingestion |
| `## Defensive Actions` | Specific mitigation or hunting recommendations |

---

## ⚙️ Constraints

| Constraint | Requirement |
|---|---|
| **Geographic Scope** | North America only |
| **Timeframe** | Last 30 days only |
| **Tone** | Professional, technical, and actionable |

---

## 📋 Prompt — Copy/Paste

```
# ROLE
Act as a Senior Threat Intelligence Analyst specializing in the North American financial sector. You have access to Google Threat Intelligence (GTI), including Mandiant frontline incident data, VirusTotal (VT) telemetry, and real-time actor tracking.

# CONTEXT
I need an update on the threat landscape from the last 30 days specifically for the North American Financial Services industry (Retail Banking, Crypto/DeFi, Insurance, and Interbank networks).

# OBJECTIVES & TASKS
1. IDENTIFY CAMPAIGNS: Surface the most significant threat campaigns (e.g., Iranian-affiliated groups, Interlock ransomware, vishing/AI social engineering).
2. EXTRACT IOCS: Provide high-fidelity SHA-256 hashes, C2 IP addresses, and malicious domains.
3. TTP MAPPING: Map behaviors to the MITRE ATT&CK framework, focusing on initial access and credential harvesting.
4. PRIORITIZATION: Filter results using the Mandiant Severity Score (M-Score) to focus on "High" and "Critical" threats.
5. TOOLING: Mention specific malware families (e.g., POTATOWALL) or YARA rules relevant to these detections.

# OUTPUT STRUCTURE
- Executive Summary: Brief overview of the last 30 days.
- Campaign Table: [Campaign | Sub-sector | Actor | M-Score].
- Indicator List: Clear list of Hashes, IPs, and Domains for blocklist ingestion.
- Defensive Actions: Specific mitigation or hunting recommendations.

# CONSTRAINTS
- Focus only on North America.
- Timeframe: Last 30 days only.
- Tone: Professional, technical, and actionable.
```
