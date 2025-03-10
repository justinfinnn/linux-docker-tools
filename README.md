# 🐳 Linux Applications with Docker Compose

This repository contains **Docker Compose** configurations for various **self-hosted Linux applications**. It enables quick and straightforward deployment of essential services, including media management tools, network utilities, and AI-powered tools.

## 📌 Included Services

Each service is managed independently via **Docker Compose**, allowing flexible deployment.

### 🎬 **Media Management Suite**

Automate downloading, organizing, and managing media content such as movies, TV shows, music, and ebooks.

| Service      | Description                                                               |
| ------------ | ------------------------------------------------------------------------- |
| **Radarr**   | Movie management for automated downloads and organization.                |
| **Sonarr**   | TV show management with episode tracking and auto-downloading.            |
| **Lidarr**   | Music collection manager for organizing and tracking music files.         |
| **Readarr**  | Ebook and audiobook management system.                                    |
| **Prowlarr** | Indexer manager that integrates with Radarr, Sonarr, Lidarr, and Readarr. |

---

### 🔐 **Network & Security Tools**

Improve security, network management, and privacy with these applications.

| Service       | Description                                               |
| ------------- | --------------------------------------------------------- |
| **Pi-hole**   | Network-wide ad blocker that functions as a DNS sinkhole. |
| **Tailscale** | A secure, simple VPN solution built on WireGuard®.        |

---

### 🤖 **AI & Machine Learning**

Deploy and access AI-powered models effortlessly.

| Service                   | Description                                                  |
| ------------------------- | ------------------------------------------------------------ |
| **OpenWebUI with Ollama** | Web-based UI for AI model interaction with GPU acceleration. |

---

## 🚀 Getting Started

### 1️⃣ **Prerequisites**

Ensure you have **Docker** and **Docker Compose** installed on your system.

- Install **Docker & Docker Compose** → [Guide](https://docs.docker.com/get-docker/)
- If using **GPU-accelerated apps**, install:
  - **NVIDIA drivers**
  - [NVIDIA Container Toolkit](https://docs.nvidia.com/datacenter/cloud-native/container-toolkit/install-guide.html)

---

### 2️⃣ **Clone the Repository**

```sh
git clone https://github.com/justinfinnn/linux-docker-tools.git
```

Navigate into the directory

```sh
cd linux-docker-apps
```

### 3️⃣ **Start a Specific Service**

Navigate into a **specific application's directory** and start it using Docker Compose.

For example, to start **Pi-hole** run:

```
cd pihole
docker-compose up -d
```

## 🔍 Managing Services

- **Check running containers:**

```
docker ps
```

- **Check all containers:**

```
docker ps a
```

**View container logs:**

```
docker logs [container_name]
```

_or_

```
docker logs [container_name] -f
```

The `-f` flag displays a live run of logs

## ⚠️ Important Notes

1.  **Persistent Data & Volumes**

    - Each service maintains its configuration in local **volumes** (e.g., `./data/`, `./config/`).
    - Back up the necessary files before updating containers.

2.  **Port Allocation**

    - Services run on different ports (e.g., Radarr on `7878`, OpenWebUI on `3009`).
    - Adjust ports in `docker-compose.yml` if needed.

3.  **GPU Acceleration (for AI Services)**

    - Ensure NVIDIA drivers and `NVIDIA_VISIBLE_DEVICES=all` are set in **GPU-based containers**.

---

## 🤝 Contributing

- 🛠 Feel free to **submit issues** or **open pull requests** if you encounter problems or improvements.
- 📩 Have a suggestion? Open a discussion!

---

🚀 **Happy Self-Hosting!** 🎉
