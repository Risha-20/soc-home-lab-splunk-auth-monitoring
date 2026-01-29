# Baseline Notes – Authentication Failures

## Purpose
Establish baseline behavior to reduce false positives in authentication alerts.

## Observed Baseline
- Typical failed logins per user: 0–2 within 10 minutes
- Occasional user mistyped passwords observed

## Alert Threshold
- Alert triggered when failures >= 8 within 10 minutes

## Tuning Notes
Thresholds should be adjusted based on environment size and user behavior.
