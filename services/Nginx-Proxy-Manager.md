## Nginx Proxy Manager

**Purpose:**<br>
User-friendly Nginx reverse proxy.

**Why Implemented:**<br>
Specifically this was installed to route traffic through my DeSEC DNS domain for vaultwarden, however having it setup is useful in general should I wish to add other services and make them publicly accessible.

**Dependencies:**<br>

- Docker
- SSL (specifically for Vaultwarden in my use case)
- deSEC DNS (or any other domain + dns provider)

**Key concepts learned:**<br>

- Reverse proxying
- HTTPS
- Container deployment

**Troubleshooting:**<br>

- SSL validation
- DNS issues
- Container connectivity
