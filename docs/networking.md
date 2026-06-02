# Networking

## DNS Architecture

Devices on the local network use AdGuard Home as their primary DNS server.

Client Device<br>
↓<br>
AdGuard Home<br>
↓<br>
NextDNS<br>
↓<br>
Internet

AdGuard Home provides local DNS filtering, logging and custom DNS rules.

NextDNS acts as the upstream resolver, providing additional filtering and threat protection.

## Public DNS

Public DNS records are managed through deSEC.

Responsibilities include:

* Domain management
* DNS record management
* Dynamic DNS updates
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
