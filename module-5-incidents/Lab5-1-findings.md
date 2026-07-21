# Lab 5.1 – Findings

## Objective

Simulate a P1 incident, restore the affected service, and complete the incident response process.

## Summary

The Nginx service was stopped, causing Uptime Kuma to detect a service outage. A P1 GitHub issue was created, investigation was performed using Uptime Kuma and Prometheus, and the service was restored by restarting Nginx.

## Resolution

```bash
sudo systemctl start nginx
```

Uptime Kuma confirmed the service was healthy after recovery, and the incident was closed.

## Key Learnings

- Monitoring enables quick outage detection.
- GitHub Issues help track incidents and communication.
- Following a structured response process improves recovery.
- PIR and PACE documentation support future incident handling.
