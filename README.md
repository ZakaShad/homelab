# My Homelab
## Getting Started
### Requirements
- Docker 
- Tailscale 

### Installation
- Install Tailscale (see [Tailscale Docs](https://tailscale.com/docs/install))
- Point Tailscale's DNS to the server's tailscale IP and restrict to domain `homelab.internal`
  - Currently, that would be network > DNS > add nameserver > custom > server ip > restrict to domain > `homelab.internal`
- `docker compose up -d`

## Current Services
- `Anchor`: For note-taking
- `Immich`: For image management
- `Homepage`: Services dashboard
- `Vaultwarden`: Password management 
    - Assumes Tailscale is running; currently relies on `tailscale serve` for SSL certs
- `Pi-Hole`: DNS Sinkhole for network-wide ad-blocking  
    - This assumes Tailscale is running 
- `Vikunja`: Task management
- `Syncthing`: File syncing
- `Zotero-webdav`: Zotero file sync

## Adding a Service 
- Update `compose.yaml` 
- Update `homepage/config/services.yaml`
- Update `README/Current Services`

### Future Services
- [x] pihole 
- [ ] personal banking services
- [ ] reverse proxy (e.g., Caddy)
- [ ] cloud drive service
