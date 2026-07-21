# Post-Incident Report (PIR)

## Incident Details

- **Ticket:** #1
- **Severity:** P2 – High
- **Product:** MFA
- **Environment:** Production
- **Reported:** 09:15 IST
- **Resolved:** 11:45 IST
- **Status:** Closed

## Summary

A customer reported that 25 Finance department users were not receiving SMS OTPs. Email OTP continued to work, allowing users to authenticate using an alternate method.

## Root Cause

The SMS sender ID was blocked due to a TRAI DND restriction on the messaging route.

## Resolution

- Investigated SMS delivery logs.
- Escalated the issue to L2.
- Switched to a backup sender ID.
- Verified OTP delivery.
- Customer confirmed service was restored.

## Prevention

- Enable sender ID monitoring.
- Maintain a backup sender ID.
- Monitor SMS delivery failures proactively.

## Outcome

All 25 affected users successfully received SMS OTPs, and the incident was closed after customer confirmation.
