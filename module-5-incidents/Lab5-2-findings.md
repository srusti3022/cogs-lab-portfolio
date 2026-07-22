# Lab 5.2 Findings

## Summary
- Simulated a failed TLS configuration by replacing `ssl_protocols` with an invalid directive.
- Confirmed the failure using `sudo nginx -t`.
- Executed the rollback by restoring the backup configuration.
- Verified the restored configuration with `nginx -t`.
- Reloaded Nginx successfully.
- Confirmed the web service was accessible using `curl -k https://localhost`.

## Outcome
- Rollback completed successfully.
- Service was restored with no remaining configuration errors.
- Rollback procedure validated and documented.
