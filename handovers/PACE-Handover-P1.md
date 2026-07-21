# PACE Handover

## Incident

P1 – Nginx Gateway Unreachable

Status: Resolved

---

## Primary

The Nginx service has been restored successfully.

Verify service status:

```bash
sudo systemctl status nginx
```

Check Uptime Kuma to ensure the monitor is green.

---

## Alternate

If the service becomes unavailable again:

```bash
sudo systemctl restart nginx
```

Verify:

```bash
curl http://localhost
```

---

## Contingency

If restarting does not resolve the issue:

- Review Nginx logs.
- Check Prometheus for CPU and memory usage.
- Verify firewall and network connectivity.

---

## Emergency

If the outage continues:

- Escalate to the Infrastructure Team.
- Restore the last known working configuration.
- Continue customer updates every 15 minutes until recovery.
