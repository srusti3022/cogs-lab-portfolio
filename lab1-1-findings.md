# lab1-1-findings.md template
# Lab 1.1 Findings
## My VM Details
- Provider: AWS
- Region: ap-south-2a
- OS: Ubuntu 22.04

## Experiment Results
### Ping to 8.8.8.8
- Average RTT: 13.341/13.348/13.355/0.005ms
- TTL value observed: 117
- What does TTL tell us about the path?

### Traceroute to google.com
- Number of hops: 7
- Any * * * hops? yes
- At which hop number?3 and 4

### DNS Comparison
- **Result from default DNS:**
 - DNS Server: 127.0.0.53 
 - Resolved IPv4 Address: 142.251.223.238
 - Resolved IPv6 Address: 2404:6800:4007:83f::200e
- **Result from 1.1.1.1:**
 - DNS Server: 1.1.1.1
 - Resolved IPv4 Address: 142.251.43.78
 - Resolved IPv6 Address: 2404:6800:4007:800::200e

- Are they different? Why might they differ?
  -Yes. Different DNS servers may return different Google IP addresses due to load balancing, caching, and geographic routing.
### google.com TLS Certificate
- Issuer: Google Trust Services (CN = WE2)
- Expiry date: Sep 21, 2026
- TLS version used: TLS 1.3



