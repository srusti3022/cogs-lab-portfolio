# Lab Capstone – Mini ZTNA Architecture

## Objective
Build a mini Zero Trust Network Access (ZTNA) environment using WireGuard, Nginx, Keycloak, and Uptime Kuma.

---

## Architecture Diagram

```text
                Laptop
         (WireGuard Client)
             10.0.0.2
                 │
     WireGuard VPN Tunnel
                 │
                 ▼
          VM2 (10.0.0.1)
    ┌─────────────────────┐
    │ WireGuard Server    │
    │ Nginx Reverse Proxy │
    └─────────┬───────────┘
              │
        HTTP Proxy (/app)
              │
              ▼
       VM1 (Keycloak)
         Port 8080

         Uptime Kuma
(Monitors WireGuard,
 Nginx & Keycloak)
```

---

## Components

- Laptop – WireGuard Client
- VM2 – WireGuard Server & Nginx Reverse Proxy
- VM1 – Keycloak Identity Provider
- Uptime Kuma – Monitoring

---

## Request Flow

```
Laptop
   ↓
WireGuard Tunnel
   ↓
VM2 (Nginx)
   ↓
VM1 (Keycloak)
```

---

## Verification

```bash
sudo wg
sudo nginx -t
curl http://10.0.0.1/app
```

The `curl` request successfully reached the Keycloak application through the WireGuard tunnel and Nginx reverse proxy.

---

## Results

- WireGuard tunnel established successfully.
- Nginx reverse proxy configured.
- Keycloak accessible through `/app`.
- Uptime Kuma monitoring configured.
- End-to-end ZTNA-style communication verified.

---

## Evidence

- Screenshot of WireGuard connection
- Screenshot of `sudo wg`
- Screenshot of `sudo nginx -t`
- Screenshot of `curl http://10.0.0.1/app`
- Screenshot of Uptime Kuma dashboard
- Screenshot of `docker ps` showing Keycloak
