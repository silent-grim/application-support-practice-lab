# Incident Investigation Report — Dashboard Failure

**Module:** 01 — Incident Triage  
**Environment:** Simulated local practice environment  
**Incident Date:** 30 October 2026  
**Status:** Investigation documented — root cause not confirmed

## 1. Incident Summary

A simulated dashboard application experienced a request failure following a database query timeout. The available logs indicate increased response time before the dashboard request failed.

## 2. Reported Symptoms

- Dashboard request failed.
- Database query timeout was recorded.
- Application response time exceeded the expected threshold.

## 3. Log Evidence

| Timestamp | Log entry |
|---|---|
| 09:15:01 | Application started |
| 09:16:10 | Database connection established |
| 09:17:22 | Database query timeout after 30 seconds |
| 09:17:23 | Dashboard request failed |
| 09:18:00 | Response time exceeded threshold |

## 4. Investigation Performed

- Reviewed the simulated application log.
- Used Windows Command Prompt `type` to inspect the log.
- Used `findstr` to filter ERROR and WARN entries.
- Compared timestamps to establish the sequence of recorded events.
- Identified the database query timeout immediately before the dashboard request failure.

## 5. Findings

The available evidence indicates a database query timeout preceding the dashboard failure.

However, the actual root cause remains unconfirmed. The logs do not establish whether the timeout resulted from query performance, database resource constraints, network latency or another dependency.

## 6. Recommended Escalation

Refer the incident to the designated application/database support team.

Recommended investigation:

- Review database query execution and performance.
- Check database resource utilisation.
- Correlate application and database logs.
- Investigate relevant dependencies and network connectivity.
- Identify whether other users or application functions are affected.

## 7. Recovery Verification

After an approved corrective action:

- Retest dashboard access.
- Verify that dashboard data loads correctly.
- Review logs for recurring errors and timeouts.
- Confirm functionality with the affected user.
- Document the resolution before closing the incident.

## 8. Learning Outcomes

- Practised reviewing and filtering application logs.
- Learned to establish an event sequence using timestamps.
- Distinguished observed evidence from an unconfirmed root cause.
- Practised documenting incident impact, investigation findings and escalation recommendations.

---

**Note:** This is a simulated training exercise, not a production incident or professional support engagement.
