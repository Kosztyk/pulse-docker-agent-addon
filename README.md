<svg width="256" height="256" viewBox="0 0 256 256" xmlns="http://www.w3.org/2000/svg">
  <title>Pulse Logo</title>
  <style>
    .pulse-bg { fill: #2563eb; }
    .pulse-ring { fill: none; stroke: #ffffff; stroke-width: 14; opacity: 0.92; }
    .pulse-center { fill: #ffffff; }
    @media (prefers-color-scheme: dark) {
      .pulse-bg { fill: #3b82f6; }
      .pulse-ring { stroke: #dbeafe; }
      .pulse-center { fill: #dbeafe; }
    }
  </style>
  <circle class="pulse-bg" cx="128" cy="128" r="122"/>
  <circle class="pulse-ring" cx="128" cy="128" r="84"/>
  <circle class="pulse-center" cx="128" cy="128" r="26"/>
</svg>
**This is the pulse-docker-agent-addon for Homeassistant**

To read more about Pulse Real-time monitoring for Proxmox VE, Proxmox Mail Gateway, PBS, and Docker infrastructure visit the official repository **https://github.com/rcourtman/Pulse**

---
![pulse-logo](https://github.com/user-attachments/assets/9a08a186-0b61-4a29-9d61-7718216ecaee)

## 🚀 Overview

Pulse is a modern, unified dashboard for your **Proxmox** and **Docker** estate. It consolidates metrics, logs, and alerts from Proxmox VE, Proxmox Backup Server, Proxmox Mail Gateway, and standalone Docker hosts into a single, beautiful interface.

Designed for homelabs, sysadmins, and MSPs who need a "single pane of glass" without the complexity of enterprise monitoring stacks.

![Pulse Dashboard](docs/images/01-dashboard.png)

## ✨ Features

- **Unified Monitoring**: View health and metrics for PVE, PBS, PMG, and Docker containers in one place.
- **Smart Alerts**: Get notified via Discord, Slack, Telegram, Email, and more when things go wrong (e.g., "VM down", "Storage full").
- **Auto-Discovery**: Automatically finds Proxmox nodes on your network.
- **Secure by Design**: Credentials encrypted at rest, no external dependencies, and strict API scoping.
- **Backup Explorer**: Visualize backup jobs and storage usage across your entire infrastructure.
- **Privacy Focused**: No telemetry, no phone-home, all data stays on your server.
- **Lightweight**: Built with Go and React, running as a single binary or container.

## ⚡ Quick Start

### Option 1: Proxmox LXC (Recommended)
Run this one-liner on your Proxmox host to create a lightweight LXC container:

```bash
curl -fsSL https://github.com/rcourtman/Pulse/releases/latest/download/install.sh | bash
```

### Option 2: Docker
```bash
docker run -d \
  --name pulse \
  -p 7655:7655 \
  -v pulse_data:/data \
  --restart unless-stopped \
  rcourtman/pulse:latest
```

Access the dashboard at `http://<your-ip>:7655`.

## 📚 Documentation

- **[Installation Guide](docs/INSTALL.md)**: Detailed instructions for Docker, Kubernetes, and bare metal.
- **[Configuration](docs/CONFIGURATION.md)**: Setup authentication, notifications, and advanced settings.
- **[Security](SECURITY.md)**: Learn about Pulse's security model and best practices.
- **[API Reference](docs/API.md)**: Integrate Pulse with your own tools.
- **[Architecture](ARCHITECTURE.md)**: High-level system design and data flow.
- **[Troubleshooting](docs/TROUBLESHOOTING.md)**: Solutions to common issues.

## ❤️ Support Pulse Development

Pulse is maintained by one person. Sponsorships help cover the costs of the demo server, development tools, and domains. If Pulse saves you time, please consider supporting the project!

[![GitHub Sponsors](https://img.shields.io/github/sponsors/rcourtman?label=Sponsor)](https://github.com/sponsors/rcourtman)
