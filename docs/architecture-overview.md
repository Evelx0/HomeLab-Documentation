# Architecture Overview

## Purpose

This home lab is a self-hosted infrastructure environment running on a Raspberry Pi 5 using Debian Linux, Docker and Docker Compose.

The environment provides hands-on experience with Linux administration, containerisation, networking, DNS management, reverse proxies, SSL certificates and security tooling.

## Infrastructure Overview

Raspberry Pi 5 (Debian 12)
│
├── Docker & Docker Compose
├── Nginx Proxy Manager
├── Vaultwarden
├── AdGuard Home
├── WireGuard
├── CrowdSec
├── Cowrie Honeypot
├── Portainer
├── Homepage
├── Dozzle
├── Linkwarden
├── Pingvin Share
└── Additional utility services

## External Access Flow

Only Vaultwarden is intentionally exposed to the internet.

Internet User
↓
deSEC DNS
↓
Public IP Address
↓
Home Router Port Forward
↓
Nginx Proxy Manager
↓
Vaultwarden Container

Nginx Proxy Manager handles SSL certificate management and forwards traffic to the appropriate backend service.

## Internal Service Access

Most services are only accessible from the local network or through WireGuard VPN access.

Examples include:

* Portainer
* Homepage
* AdGuard Home
* CrowdSec
* FileBrowser
* Linkwarden
* Pingvin Share

This approach reduces attack surface by limiting unnecessary public exposure.
