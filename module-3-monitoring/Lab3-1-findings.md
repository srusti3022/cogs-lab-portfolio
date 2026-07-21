# lab3-1-findings

## Monitor Type Mapping

| Uptime Kuma Monitor | Purpose | InstaSafe / Enterprise Use |
|---------------------|---------|----------------------------|
| HTTP(S) | Checks web server availability | Gateway/Portal health monitoring |
| TCP Port | Checks if a service port is open (SSH) | Service and port availability |
| Ping | Checks host reachability | Network connectivity monitoring |

## Gateway Monitoring Rationale

Monitoring the gateway is important because it is the primary entry point for users. If the gateway or its services become unavailable, users cannot access applications. HTTP, TCP, and Ping monitors help detect outages quickly and enable faster incident response.
