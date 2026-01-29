# Incident Report – Suspected Brute Force Activity

## Incident ID
INC-001

## Summary
Multiple failed authentication attempts were detected for a single user account
within a short time window.

## Investigation Steps
- Reviewed Windows Event ID 4625 logs in Splunk
- Analyzed timestamps and failure volume
- Checked for successful logins following failures

## Findings
The activity pattern was consistent with brute-force password guessing.
No successful authentication was observed following the failed attempts.

## Risk Assessment
Potential credential attack targeting user authentication.

## Severity
Medium

## Recommended Actions
- Continue monitoring the affected account
- Enforce account lockout and password policies
- Escalate if successful authentication occurs
