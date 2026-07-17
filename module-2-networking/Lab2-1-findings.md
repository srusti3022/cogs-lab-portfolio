# Lab 2.1 – OpenLDAP Fundamentals

## Objective
Install OpenLDAP, create users, and test LDAP authentication.

## Environment
- OS: Ubuntu 22.04
- LDAP Domain: `lab.instasafe.local`

## LDAP Concepts and InstaSafe AD Sync

| LDAP Concept | Lab Example | InstaSafe Equivalent |
|--------------|-------------|----------------------|
| Base DN | `dc=lab,dc=instasafe,dc=local` | Directory search location |
| Bind DN | `cn=admin,dc=lab,dc=instasafe,dc=local` | Service account used to connect to LDAP/AD |
| User DN | `uid=alice,ou=People,...` | User authenticated during login |
| Attributes | `cn`, `uid`, `mail` | User details synced into InstaSafe |

## Validation
- `ldapsearch` successfully returned both users (Alice and Bob).
- `ldapwhoami` authenticated Alice successfully.
- Invalid password returned **Error 49 (Invalid credentials)**.

## Conclusion
This lab demonstrated how LDAP authentication works. Similar to InstaSafe AD Sync, applications use a Bind DN to connect, search users under the Base DN, retrieve user attributes, and authenticate users using LDAP bind.
