## WireGuard

**Purpose:**<br>
Self-hosted VPN tunnel management.

**Why Implemented:**<br>
Main purpose was to give me a way to access my home network directly from other devices, as way of a secure VPN and also to manage the RaspberryPi remotely if ever required.

**Dependencies:**<br>

- Docker
- RaspberryPi Host (or a linux server if I was going to setup a static vpn)
- UDP Port open in firewall, default is 51820
- Ideally host kernel 5.6+ with WG support, otherwise wireguard-go as fallback.

**Key concepts learned:**<br>

- Reverse proxying
- VPN Tunnels
- Container deployment
- Authentication systems

**Troubleshooting:**<br>

- VPN Tunnel connection issues
- Initial container connectivity
