# CHANGE-001 – TLS Upgrade

**Change ID:** CHANGE-001

**Type:** Normal Change

**Description:** Update Nginx TLS configuration to prefer TLS 1.3.

**Justification:** TLS 1.3 provides improved security and performance over TLS 1.2.

## Execution Steps

1. Backup the current Nginx configuration.
2. Update the `ssl_protocols` directive.
3. Test the configuration using `nginx -t`.
4. Reload the Nginx service.
5. Verify TLS 1.3 is working.

## Rollback Trigger

If TLS verification fails or the website becomes unreachable.

## Rollback Steps

1. Restore the backup configuration.
2. Test the configuration.
3. Reload Nginx.

```bash
sudo cp /etc/nginx/nginx.conf.backup /etc/nginx/nginx.conf
sudo nginx -t
sudo systemctl reload nginx
```

**Rollback Time:** 2 minutes

**Maintenance Window:** Immediate (Lab Environment)
