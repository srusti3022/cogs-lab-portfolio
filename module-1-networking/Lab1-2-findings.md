# Lab 1.2 Findings 

## Objective
Configured HTTPS on an Nginx web server using a self-signed TLS certificate and verified secure communication.

## Steps Performed
- Installed and configured Nginx.
- Created a custom web page.
- Allowed ports **22**, **80**, and **443** using UFW.
- Generated a self-signed TLS certificate with OpenSSL.
- Configured Nginx for HTTPS (TLS 1.2 and TLS 1.3).
- Verified HTTPS using `curl` and `openssl`.

## Certificate Analysis
- **Type:** Self-Signed X.509
- **Subject/CN:** 16.112.158.215
- **Issuer:** Self-Signed (InstaSafe Lab)
- **Validity:** 17 Jul 2026 – 17 Jul 2027
- **Public Key:** RSA 2048-bit
- **Signature Algorithm:** SHA256 with RSA

## Observations
- HTTP and HTTPS were working successfully.
- HTTPS used a self-signed certificate.
- `curl` without `-k` showed a certificate warning because the certificate was not issued by a trusted CA.
- TLS 1.1 was disabled (`no protocols available`), while TLS 1.2 and TLS 1.3 were enabled.

## Conclusion
Successfully configured HTTPS on Nginx using a self-signed TLS certificate and verified secure communication using `curl` and `openssl`.
