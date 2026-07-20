# Post-Incident Report (PIR)

**Incident ID:** INC-2026-0408-001

**Date:** 2026-04-08

**Severity:** P2

**Status:** Resolved

---

## Incident Summary

On 8 April 2026 at approximately 09:15 IST, a financial institution reported that 25 users were unable to receive Multi-Factor Authentication (MFA) OTPs. Investigation revealed that the SMS provider, Kaleyra, was rejecting messages because the configured sender ID had been flagged. The issue was escalated to the L2 support team, who activated a backup sender ID. OTP delivery resumed successfully, and the customer confirmed restoration of service at 11:45 IST.

---

## Timeline

| Time (IST) | Event |
|------------|-------|
| 09:15 | Customer reported MFA failure affecting 25 users |
| 09:18 | Ticket #1001 created (P2) |
| 09:20 | Initial customer response sent |
| 09:35 | Kaleyra logs reviewed; REJECTED status confirmed |
| 10:30 | Escalated to L2 support |
| 11:30 | L2 identified sender ID issue |
| 11:40 | Backup sender ID activated |
| 11:45 | Customer confirmed OTP delivery restored |

---

## Root Cause

The primary SMS sender ID registered with Kaleyra was flagged, causing SMS OTP requests to be rejected. As a result, OTP messages were not delivered until a valid backup sender ID was configured.

---

## Impact Assessment

- Users affected: 25
- Duration: Approximately 2 hours 30 minutes
- Business Impact:
  - Users could not complete MFA authentication.
  - Business operations experienced login delays.
  - Increased support workload due to authentication failures.

---

## Resolution Steps

1. Reviewed customer reports and application logs.
2. Verified Kaleyra API response codes.
3. Escalated the incident to L2.
4. Confirmed sender ID rejection.
5. Activated backup sender ID.
6. Validated successful OTP delivery.
7. Confirmed service restoration with the customer.

---

## Prevention Actions

- [ ] Monitor SMS gateway rejection rates — Owner: L2 Support — Due: 2026-04-15
- [ ] Configure automatic failover to backup sender ID — Owner: Platform Team — Due: 2026-04-20

---

## Open Items

- [ ] Publish a knowledge base article documenting this incident — Owner: Support Team — Due: 2026-04-18