# Matija Aleksić

**Backend Developer & Linux Systems Technician**

Backend developer and IT technician studying at TVZ. I write applications in strongly-typed languages and maintain a dedicated self-hosted Proxmox infrastructure for deployment, automation, and networking.

---

## Technical Focus

- **Backend Development:** Building application logic in Java (Spring Boot, JavaFX) and C# (.NET Core). Database schema design, querying, and optimization with MySQL.
- **Systems & Virtualization:** Hypervisor-level virtualization (Proxmox VE), unprivileged LXC containerization, ZFS storage, and infrastructure networking.
- **Traffic Routing & Security:** Reverse proxying with Traefik v3, secure edge routing over Cloudflare Tunnels and Tailscale, and local DNS with AdGuard Home and Unbound.

---

## Homelab Architecture

One bare-metal Proxmox host running three unprivileged Debian LXCs. Services run in Docker *inside* the containers rather than in full VMs, to keep virtualization overhead down on modest hardware.

### Hardware & Core Platform

- **Host:** Intel Core i3-6100 (2c/4t) | 16 GB RAM | Proxmox VE
- **Storage:** ZFS pool for application data, 4 TB HDD for media

### Service Layout

| LXC | Role | Key services |
| --- | --- | --- |
| `network` (102) | Edge routing & DNS | Cloudflare Tunnel, Tailscale, AdGuard Home → Unbound, WatchYourLAN |
| `apps` (100) | Application stack | Traefik v3, Immich, Paperless-ngx, Jellyfin/Plex, Servarr suite, SparkyFitness, Uptime Kuma, Portainer |
| `llm` (104) | Local inference | Ollama, SearXNG, ChromaDB, ntfy |

- **No open router ports.** External traffic enters through a Cloudflare Tunnel terminating at Traefik; administrative access is over a Tailscale mesh.
- **DNS** for every container resolves through AdGuard Home, which forwards to a local Unbound recursive resolver rather than an upstream provider.
- **The repo is generated, not written.** A nightly cron job on the Proxmox host pulls live configs out of all three LXCs with `pct pull`, scans them with `gitleaks`, and commits only when something actually changed — so [`my-homelab`](https://github.com/Matija-Aleksic/my-homelab) mirrors the running system instead of drifting from it.

**Current focus:** migrating remaining services onto a unified Traefik network, and building out the local LLM stack.

---

## Tech Stack

- **Languages:** Java, C#, Python, Bash, C
- **Frameworks & Libraries:** Spring Boot, .NET Core, JavaFX
- **Databases:** MySQL, PostgreSQL, H2
- **Tools & Infrastructure:** Docker & Compose, Proxmox VE, LXC, ZFS, Traefik, Cloudflare Tunnel, Tailscale, Unbound, Git, Maven, Samba/NFS
- **Currently learning:** K3s, CI/CD pipelines with GitHub Actions, Prometheus & Grafana

---

## GitHub Stats

[![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=Matija-Aleksic&layout=compact&theme=dracula&hide_border=true)](https://github.com/Matija-Aleksic)

---

## Contact

- **Email:** <matijaaleksic22@gmail.com>
- **LinkedIn:** [linkedin.com/in/matija-aleksic-9bb252265](https://www.linkedin.com/in/matija-aleksic-9bb252265/)
