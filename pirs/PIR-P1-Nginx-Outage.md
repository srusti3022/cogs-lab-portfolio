# Post Incident Report (PIR)

## Incident Summary

- Incident: P1 – Nginx Gateway Unreachable
- Date: 21 July 2026
- Severity: P1 (Critical)
- Status: Resolved

## Timeline

| Time | Action |
|------|--------|
| T+0 | Uptime Kuma detected outage |
| T+2 | GitHub issue created |
| T+3 | Customer acknowledgement posted |
| T+5 | Investigated Uptime Kuma logs |
| T+8 | Checked Prometheus metrics |
| T+10 | Investigation findings added |
| T+15 | 15-minute update posted |
| T+20 | Restarted Nginx service |
| T+22 | Verified service recovery |
| T+25 | Resolution notice posted |
| T+30 | Incident closed |

## Root Cause

The Nginx service was stopped, causing the website to become unavailable.

## Resolution

The service was restored using:

```bash
sudo systemctl start nginx
```

Uptime Kuma confirmed that the service returned to a healthy state.

## Customer Impact

Users could not access the web application until the service was restored.

## Lessons Learned

- Monitoring detected the outage quickly.
- Following the P1 response process reduced recovery time.
- Documentation and communication were maintained throughout the incident.

## Preventive Actions

- Enable automatic restart for Nginx.
- Continue monitoring using Uptime Kuma and Prometheus.
