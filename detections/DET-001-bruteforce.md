# DET-001 – Brute Force Authentication Attempts

## Objective
Detect abnormal volumes of failed authentication attempts that may indicate
brute-force password guessing activity.

## Data Source
- Windows Security Event Logs
- Event ID 4625 (Failed Logon)

## Detection Logic
This detection identifies repeated failed login attempts for the same user
account within a short time window.

High failure counts within a limited timeframe may indicate automated or
persistent credential guessing behavior.

## SOC Relevance
Brute-force authentication attempts are common Tier-1 SOC alerts and are often
an early indicator of credential compromise attempts.

## Escalation Criteria
Escalate this alert when:
- Failed logins exceed baseline thresholds
- Attempts target privileged or service accounts
- Activity occurs outside normal business hours
- A successful login follows repeated failures (see DET-003)

## Initial Response Actions
- Review affected user account and host
- Check for successful logons following failures
- Document findings and continue monitoring
