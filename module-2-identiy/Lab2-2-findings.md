# Lab 2-2 Findings

## Attribute Mapper Explanation

Attribute mappers define which user attributes from Keycloak are included in the SAML assertion sent to the Service Provider after successful authentication.

Configured mappers:

- **email**: Sends the user's email address.
- **groups**: Sends the Keycloak group memberships, which can be used by the Service Provider for authorization decisions.

These attributes allow the Service Provider to identify users and apply access control based on their profile and group membership.

---

## SSO Troubleshooting

During testing, the SAML login reached the Keycloak Identity Provider but returned an "Invalid Request" page.

The sample Flask application generated a placeholder SAML AuthnRequest (`<AuthnRequest/>`) instead of a complete SAML authentication request. A valid AuthnRequest must include required fields such as the Request ID, Issuer, Destination, Assertion Consumer Service URL (ACS), and proper SAML binding encoding. Because these fields were missing, Keycloak rejected the request.

This confirms that Keycloak received the request, but a fully compliant SAML Service Provider is required for a successful SSO flow.
