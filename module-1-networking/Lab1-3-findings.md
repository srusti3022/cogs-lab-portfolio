# Lab 1.3 Findings – WireGuard → ZTNA Component Mapping

## WireGuard Components

| WireGuard | ZTNA Equivalent |
|-----------|-----------------|
| VM2 (Client) | ZTNA Agent |
| VM1 (Server) | ZTNA Gateway |
| Public/Private Keys | Device Identity |
| WireGuard Tunnel | Encrypted Secure Tunnel |
| Handshake | Authentication |
| AllowedIPs | Access Policy |
| Encrypted UDP (51820) | Secure Communication |

## Verification

- WireGuard tunnel established successfully.
- `wg show` displayed an active handshake.
- `ping 10.0.0.1` from the client succeeded through the VPN tunnel.
- `tcpdump` captured only encrypted UDP packets on port 51820, confirming that application traffic was encrypted.

## Conclusion

WireGuard demonstrates the core idea behind ZTNA. The client (agent) authenticates with the gateway using cryptographic keys, creates an encrypted tunnel, and securely exchanges traffic. Similar to a ZTNA solution, communication is authenticated, encrypted, and restricted to authorized endpoints.
