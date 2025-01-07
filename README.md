# Docker Media Server Setup

This repository contains a complete Docker setup for self-hosting a media server using the following services:

- **[Jellyfin](https://jellyfin.org/):** A media streaming server.
- **[Radarr](https://radarr.video/):** A movie collection manager.
- **[Sonarr](https://sonarr.tv/):** A TV series collection manager.
- **[Transmission](https://transmissionbt.com/):** A BitTorrent client.
- **[Jackett](https://github.com/Jackett/Jackett):** A proxy server for torrent trackers.

## Features
- Stream movies and TV shows with Jellyfin.
- Automate downloading and organizing TV shows with Sonarr.
- Automate downloading and organizing movies with Radarr.
- Use Jackett to expand torrent sources.
- Use Transmission for torrent downloads.

---

## Prerequisites

Before you start, ensure you have the following:
- [Docker](https://docs.docker.com/get-docker/) installed.
- [Docker Compose](https://docs.docker.com/compose/install/) installed.

---

## Setup

### Clone the Repository
```bash
git clone https://github.com/yourusername/docker-media-server.git
cd docker-media-server
```

### Configure Environment Variables
1. Create a `.env` file based on the provided template:
   ```
   cp .env.example .env
   ```
2. Update the values in `.env` to match your setup:
   ```env
   PUID=1000
   PGID=1000
   TZ=Etc/UTC
   JELLYFIN_PublishedServerUrl=192.168.1.50
   ```

### Start the Containers
Run the following command to start the services:
```bash
./start.sh
```

### Stop the Containers
To stop the services, use:
```bash
./stop.sh
```

---

## Folder Structure
```
.
├── docker-compose.yaml
├── .env.example
├── jelly/          # Jellyfin config and media folders
├── sonarr/         # Sonarr config and media folders
├── radarr/         # Radarr config and media folders
├── jackett/        # Jackett config
├── transmission/   # Transmission config and downloads
└── scripts/        # Automation scripts
```



