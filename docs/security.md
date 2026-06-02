# Security

## Security Approach

The environment follows a principle of minimising public exposure wherever possible.

Only Vaultwarden is intentionally accessible from the internet.

All other services remain internal unless accessed through WireGuard VPN.

## SSL/TLS

Nginx Proxy Manager manages SSL certificates for externally accessible services.

HTTPS is enforced to encrypt communications between clients and services.

## CrowdSec

CrowdSec provides security monitoring and threat detection capabilities.

Responsibilities include:

* Log analysis
* Threat detection
* Security monitoring
* Automated response capabilities

## Cowrie Honeypot

Cowrie is deployed as an SSH honeypot for personal development and experience within a blue team environment.

Purpose:

* Observe automated scanning activity
* Monitor attack behaviour
* Gain familiarity with common attack patterns

## Authentication

Vaultwarden provides secure password management.

The platform is protected through:

* HTTPS
* Strong authentication
* Controlled exposure through reverse proxying

## Security Skills Demonstrated

* SSL/TLS management
* Reverse proxy security
* Security monitoring
* Log analysis
* Attack surface reduction
* Secure remote access
* Identity management concepts
