# Networking

## DNS Architecture

Devices on the local network use AdGuard Home as their primary DNS server.

**Outbound Traffic**<br>
```
Client Device
↓
AdGuard Home
↓
NextDNS
↓
Internet
```

AdGuard Home provides local DNS filtering, logging and custom DNS rules.

NextDNS acts as the upstream resolver, providing additional filtering and threat protection.

**Inbound Traffic**<br>
```
User
↓
deSEC DNS
↓
Router
↓
Nginx Proxy Manager
↓
Vaultwarden
```

## Public DNS

Public DNS records are managed through deSEC.

Responsibilities include:

* Domain management
* DNS record management
* Public resolution for Vaultwarden

## Reverse Proxy

Nginx Proxy Manager acts as the reverse proxy for externally accessible services.

Responsibilities include:

* SSL certificate management
* HTTPS enforcement
* Request routing
* Backend service protection

## WireGuard VPN

WireGuard provides secure remote access to internal services.

This allows administration of internal applications without exposing management interfaces directly to the internet.

## deSEC DNS

Used to manage public DNS records for externally accessible services.

Responsibilities:

- Public DNS management
- Dynamic DNS updates
- Domain resolution for Vaultwarden

## AdGuard Home

Configured as the primary DNS server for the local network.

Responsibilities:

- Network-wide ad blocking
- DNS query logging
- Custom DNS filtering rules
- Local DNS management

## NextDNS

Configured as the upstream DNS resolver.

Responsibilities:

- Threat intelligence filtering
- Malware domain blocking
- Privacy-focused DNS resolution
- Additional content filtering

## Nginx Proxy Manager

Provides reverse proxy functionality for externally accessible services.

Responsibilities:

- SSL certificate management
- HTTPS enforcement
- Request routing
- Backend service protection

## Docker Networking

Services are deployed using Docker Compose.

Docker networking provides:

* Service isolation
* Internal service communication
* Controlled port exposure
* Simplified application deployment

## Networking Skills Demonstrated

* DNS management
* DNS filtering
* Reverse proxy configuration
* SSL/TLS deployment
* VPN administration
* Docker networking
* Network troubleshooting
