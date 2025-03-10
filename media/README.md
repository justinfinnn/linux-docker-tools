# Media Management with Docker Compose

This repository provides a **Docker Compose** configuration to deploy a suite of **Arr Apps** for managing movies, TV shows, music, audiobooks, and ebooks. These services automate searching, downloading, and organizing media files.

## Services

### 📽 Radarr

[Radarr](https://radarr.video/) is a movie collection manager for Usenet and BitTorrent users. It automatically monitors, downloads, and manages movie files.

- **Web UI:** `http://localhost:7878`
- **Config & Data Location:** `./radarr:/config` and `/[YourPathHere]:/data`

### 📺 Sonarr

[Sonarr](https://sonarr.tv/) is a PVR (Personal Video Recorder) for TV shows, allowing automated downloading, renaming, and organization.

- **Web UI:** `http://localhost:8989`
- **Config & Data Location:** `./sonarr:/config` and `/[YourPathHere]:/data`

### 📚 Readarr

[Readarr](https://readarr.com/) manages ebooks and audiobooks, automating downloads and organizing them.

- **Web UI:** `http://localhost:8787`
- **Config & Data Location:** `./readarr:/config` and `/[YourPathHere]:/data`

### 🔎 Prowlarr

[Prowlarr](https://github.com/Prowlarr/Prowlarr) acts as an indexer manager, integrating with Radarr, Sonarr, Readarr, and Lidarr to handle search queries and track available media.

- **Web UI:** `http://localhost:9696`
- **Config Location:** `./prowlarr:/config`

### 🎵 Lidarr

[Lidarr](https://lidarr.audio/) is a music collection manager that automates the downloading and organizing of music files.

- **Web UI:** `http://localhost:8686`
- **Config & Data Location:** `./lidarr:/config` and `/[YourPathHere]:/data`

## Getting Started

1. **Install Docker & Docker Compose** if not already installed. ([Guide](https://docs.docker.com/get-docker/))
2. **Clone this repository**:
   ```sh
   git clone https://github.com/justinfinnn/arr-apps.git
   cd arr-apps
   ```
