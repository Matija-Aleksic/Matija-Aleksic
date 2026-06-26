# Matija Aleksić
**Backend Developer & Linux Systems Technician**

Backend developer and IT technician studying at TVZ. I write applications in strongly-typed languages and maintain a dedicated self-hosted Proxmox infrastructure for deployment, automation, and networking.

---

## Technical Focus

* **Backend Development:** Building application logic using Java (Spring Boot) and C# (.NET Core). Database schema design, querying, and optimization with MySQL.
* **Systems & Virtualization:** Implementing hypervisor-level virtualization (Proxmox VE), LXC containerization, storage architecture (TrueNAS SCALE, ZFS, NFS), and infrastructure networking.
* **Traffic Routing & Security:** Configuring reverse proxies (Traefik v3, Nginx Proxy Manager), secure edge routing (Cloudflare Tunnels, Tailscale), and local DNS (AdGuard Home, Unbound).

---

## Homelab Architecture

I run a bare-metal home server to test deployments, network topologies, and infrastructure automation.

### Hardware & Core Platform
* **Host:** Intel i3-6100 | 16 GiB RAM | Proxmox VE (ZFS storage host)
* **Storage:** TrueNAS SCALE VM with raw disk passthrough handling NFS shares across the cluster.

### Service Layout
* **LXC `APPS` (Docker Stack):** Runs a containerized microservice environment behind a Traefik v3 reverse proxy. Utilizes `/dev/dri` hardware acceleration passthrough for media transcoding pipelines.
* **Services Deployed:** Jellyfin, Plex, Emby, the Arr suite (Sonarr, Radarr, Prowlarr), Uptime Kuma, Portainer.
* **LXC `NETWORK`:** Isolated container managing edge routing, DNS resolution, and tunneling (`tun` device integration).
* **Current Focus:** Migrating legacy monolithic networking to a unified Traefik proxy network, testing K3s (Kubernetes) clusters in isolated VMs, and experimenting with local LLM integration (Ollama).

---

## Tech Stack

* **Languages:** Java, C#, C++, C, Python, Bash, PHP, JavaScript
* **Frameworks & Libraries:** Spring Boot, .NET Core
* **Tools & Infrastructure:** Docker, Git, Proxmox VE, TrueNAS, Traefik, Nginx, MySQL, Grafana, Prometheus

---

## GitHub Stats

<div align="center">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=Matija-Aleksic&layout=compact&theme=dracula&hide_border=true" height="160" alt="Top Languages"/>
</div>

---

## Contact

* **Email:** matijaaleksic22@gmail.com
* **LinkedIn:** [linkedin.com/in/matija-aleksic-9bb252265](https://www.linkedin.com/in/matija-aleksic-9bb252265/)
