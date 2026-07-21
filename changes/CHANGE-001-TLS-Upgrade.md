# Change Plan

**Change ID:** CHANGE-001

**Type:** Normal Change

**Description:** Update Nginx TLS configuration to prefer TLS 1.3.

**Justification:** TLS 1.3 is faster and more secure, aligning with current best practices.

## Execution Steps

1. Backup the current Nginx configuration.
2. Update the `ssl_protocols` setting in the Nginx site configuration.
3. Test the configuration using `nginx -t`.
4. Reload Nginx.
5. Verify that TLS 1.3 is working.

## Rollback Trigger

Rollback if TLS verification fails or the site becomes unreachable.

## Rollback Steps

1. Restore the backup configuration.

```bash
sudo cp /etc/nginx/nginx.conf.backup /etc/nginx/nginx.conf
```

2. Test and reload Nginx.

```bash
sudo nginx -t
sudo systemctl reload nginx
```

## Rollback Time

Approximately 2 minutes.

## Maintenance Window

Immediate (Lab environment – no customer impact).