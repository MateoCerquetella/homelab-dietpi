# Docker Services Configuration

Centralized Docker services setup with unified secrets management for DietPi on Raspberry Pi.

<img src="./dashboard.png" alt="Dashboard"/>


## 📁 Service Structure

```
homelab-dietpi/
├── .env
├── .env.example
├── .gitignore
├── README.md
├── filebrowser/
│   └── docker-compose.yml
├── glance/
│   └── docker-compose.yml
├── monitoring/
│   ├── compose.yaml
│   ├── grafana/
│   ├── influxdb2/
│   ├── prometheus/
│   └── telegraf/
├── nginx-proxy-manager/
│   └── docker-compose.yml
├── pihole/
│   └── docker-compose.yml
├── portainer/
│   └── docker-compose.yml
├── speedtest/
│   └── docker-compose.yml
└── stirling-pdf/
    └── docker-compose.yml
```

## 📋 Services Overview

### Pi-hole (DNS & Ad Blocking)

-   **Ports:** 53 (DNS), 8053 (Web UI)
-   **URL:** http://192.168.88.250:8053
-   **Credentials:** See `PIHOLE_PASSWORD` in `.env`
-   **Network:** raspberry-net

### Nginx Proxy Manager

-   **Ports:** 80, 443, 81 (Admin)
-   **Admin URL:** http://192.168.88.250:81
-   **Default credentials:** admin@example.com / changeme
-   **Network:** raspberry-net

### Speedtest Tracker

-   **Port:** 8094
-   **URL:** http://192.168.88.250:8094
-   **API Key:** Set in `.env` after first setup
-   **Network:** raspberry-net

### Monitoring Stack

-   **Grafana:** http://192.168.88.250:3000
-   **Prometheus:** http://192.168.88.250:9090
-   **InfluxDB:** http://192.168.88.250:8086
-   **Network:** raspberry-net

### Stirling PDF

-   **Port:** 8082
-   **URL:** http://192.168.88.250:8082
-   **Network:** raspberry-net

### FileBrowser

-   **Port:** 8083
-   **URL:** http://192.168.88.250:8083
-   **Network:** raspberry-net

### Glance Dashboard

-   **Port:** 8081
-   **URL:** http://192.168.88.250:8081
-   **Network:** raspberry-net

## 🚀 Coming Soon

-   **NAS (Network Attached Storage)** - File storage and sharing solution (Immich)
-   **Servarr Stack** - Media automation suite (Sonarr, Radarr, Prowlarr, etc.)
-   And more...
