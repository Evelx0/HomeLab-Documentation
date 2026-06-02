## Vaultwarden

**Purpose:**<br>
Self-hosted password manager, mainly to make use of the Nginx Proxy Manager & to stop paying for 1Password. 

**Why Implemented:**<br>
Secure credential management, self hosted.

**Dependencies:**<br>

- Docker
- Nginx Proxy Manager
- SSL
- deSEC DNS

**Key concepts learned:**<br>

- Reverse proxying
- HTTPS
- Container deployment
- Authentication systems

**Troubleshooting:**<br>

- SSL validation
- DNS issues
- Container connectivity

**Network Flow**<br>
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
