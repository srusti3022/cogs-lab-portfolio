# Lab 2.3 Findings – TOTP

## Root Causes of TOTP Failure

- User device clock is out of sync with the server.
- Incorrect shared secret is configured.
- Expired OTP entered after the 30-second validity period.
- Wrong account or QR code scanned.
- Time zone or automatic time settings are disabled on the device.

## Conclusion

TOTP authentication depends on both the client and server sharing the same secret and having synchronized clocks. Even a small time difference can cause authentication to fail.
