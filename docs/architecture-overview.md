# Architecture Overview

The Raspberry Pi acts as the central host for a collection of self-hosted services running within Docker containers.

Most services are accessible only from the local network. Vaultwarden is the only service intentionally exposed to the internet.

## External Access Flow

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

Nginx Proxy Manager handles SSL certificate management, HTTPS enforcement and routing requests to the appropriate backend service.

# Examples:

vault.domain.com

↓

Vaultwarden
