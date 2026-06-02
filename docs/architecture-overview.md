# Architecture Overview

The Raspberry Pi acts as the central host for all services.

External traffic enters via:

Internet

↓

Router Port Forward

↓

Nginx Proxy Manager

↓

Backend Services

# Examples:

vault.domain.com

↓

Vaultwarden

files.domain.com

↓

Pingvin Share

links.domain.com

↓

Linkwarden
