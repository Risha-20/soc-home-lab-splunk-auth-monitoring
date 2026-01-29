# SOC Home Lab – Authentication Monitoring & Incident Triage (Splunk + Windows Logs)

## Overview
This project simulates Tier-1 SOC security monitoring by analyzing Windows authentication logs in Splunk SIEM.
The lab focuses on detecting suspicious login activity, performing alert triage, tuning detections, and
documenting SOC-style incident reports aligned with real-world Security Operations workflows.

## Why this project
Authentication-related alerts make up a large portion of Tier-1 SOC investigations.  
This lab was built to practice:
- Log-based detection using Windows Security Event Logs
- Alert validation and triage
- False-positive analysis and tuning
- Clear, escalation-ready incident documentation

## Environment
- Splunk Free
- Windows 10/11 endpoint (VM or host)
- Windows Security Event Logs
- VirtualBox (for lab isolation)

## Log Sources
- Windows Security Event Logs
  - Event ID 4625 – Failed Logon
  - Event ID 4624 – Successful Logon

## Detection Use Cases
- Brute-force login attempts (high-volume failures for a single account)
- Password spray patterns (multiple users targeted from a single source)
- Successful authentication following repeated failures (high-risk scenario)

## SOC Workflow Practiced
1. Ingest Windows logs into Splunk
2. Build SPL searches for authentication abuse
3. Validate alerts and analyze context
4. Tune thresholds to reduce false positives
5. Document incidents with evidence and recommended actions

## MITRE ATT&CK Mapping
- **T1110 – Brute Force**
  - T1110.001 – Password Guessing
  - T1110.003 – Password Spraying

## Repository Structure

## Evidence
Screenshots of Splunk searches, dashboards, and example alerts are stored in the
`screenshots/` directory. Sample SOC-style incident reports are included in
`incident-reports/`.

## Outcome
This lab strengthened hands-on experience with SIEM-based security monitoring,
authentication threat detection, alert triage, and professional incident documentation.
