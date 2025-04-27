# Homelab Serverrack Naming Scheme

A standardized and scalable naming convention for the Homelab server rack, including TrueNAS, Portainer servers, and all related services.  

---


- **SITE**: Location or environment (e.g., `HOMELAB`, `RACK01`)
- **ROLE**: Purpose of the device (e.g., `SRV`, `NAS`, `CTR`, `APP`, `DB`)
- **FUNCTION**: What the device or service does (e.g., `WEB`, `STOR`, `MEDIA`, `MONITOR`, `DEV`)
- **SERVICE**: Specific service or app (e.g., `NGINX`, `POSTGRES`, `PLEX`, `K8S`)
- **INSTANCE**: Instance number (e.g., `01`, `02`, `03`)

> **Example:** `HOMELAB-NAS-STOR-01`

---

## 🖥 Server and Service Naming Examples

| Purpose                  | Example Hostname                         | Notes                          |
|---------------------------|------------------------------------------|--------------------------------|
| TrueNAS Storage Server    | `HOMELAB-NAS-STOR-01`     | Main storage unit              |
| Portainer Main Server     | `HOMELAB-CTR-CORE-01`     | Manages containers             |
| Second Portainer Server   | `HOMELAB-CTR-CORE-02`     | Secondary/backup Portainer     |
| NGINX Reverse Proxy       | `srv-web-nginx-01`        | Web reverse proxy container    |
| Postgres Database         | `srv-db-postgres-01`      | Database container             |
| Plex Media Server         | `srv-media-plex-01`       | Media server container         |
| Home Assistant            | `srv-app-homeassistant-01`| Smart home container           |

---

## 📂 Storage Naming

For TrueNAS (or similar storage systems):

- **Pools**:
  - `pool-media`
  - `pool-backups`
  - `pool-vm`
  - `pool-archive`

- **Datasets**:
  - `dataset-media-movies`
  - `dataset-backups-pc`
  - `dataset-vm-images`
  - `dataset-documents`

- **Snapshots**:
  - `snap-[datasetname]-daily-YYYYMMDD`
  - `snap-[datasetname]-weekly-YYYYMMDD`

---

## 🐳 Containers and Stacks

- **Container Naming**:
  - Follow: `srv-[function]-[service]-[instance]`
  - Example: `srv-web-nginx-01`

- **Stack Naming (Portainer / Docker Compose)**:
  - `stack-[function]`
  - Examples:
    - `stack-monitoring`
    - `stack-homeautomation`
    - `stack-webapps`
    - `stack-databases`

---

# 🔧 Example Full Setup Overview

| Layer            | Name Example                            | Purpose                      |
|------------------|-----------------------------------------|-------------------------------|
| Storage Server   | `HOMELAB-NAS-STOR-01`    | Main TrueNAS server           |
| Container Server | `HOMELAB-CTR-CORE-01`    | Portainer container host      |
| Media Service    | `srv-media-plex-01`      | Plex container                |
| Web Service      | `srv-web-nginx-01`       | Reverse Proxy                 |
| Database Service | `srv-db-postgres-01`     | PostgreSQL database container |
| Automation Stack | `stack-homeautomation`                  | Home Assistant + Node-RED     |

---



# File-Naming-Conventions

File naming conventions for my Personal Homelab because I couldn't find good existing documentation for this sort of application. 
This makes it easier to sort and find Files. You can copy mine or adjust them how you like.

# General Naming Convention

YYYY-MM-DD_TITLE

# Videoproject Folder Structure

- YYYY-MM_TITLE
  - 01_Footage
  - 02_SFX
  - 03_Music
  - 04_Assets
  - 05_Exports

## Video File Naming Convention

PROJECT_SHOOT_###

# Lightroom Structure

- YYYY
	- YYYY-MM_TITLE
		- 01_RAW
		- 02_EXPORT
