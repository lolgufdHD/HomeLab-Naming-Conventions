# Homelab Serverrack Naming Scheme

A standardized and scalable naming convention for the Homelab server rack, including TrueNAS, Portainer servers, and all related services.  
Domain used: **`storagevault.me`** (subject to change if needed).

---

## 📦 Naming Format

[SITE]-[ROLE]-[FUNCTION]-[NUMBER].[DOMAIN]


| Field    | Example                                 | Notes                                                                   |
| -------- | --------------------------------------- | ----------------------------------------------------------------------- |
| Site     | `HOMELAB`, `RACK01`                     | Optional for future multi-location expansion.                           |
| Role     | `SRV`, `NAS`, `CTR`                     | `SRV` = General server, `NAS` = Storage server, `CTR` = Container host. |
| Function | `MEDIA`, `STOR`, `WEB`, `DB`, `CORE`    | Describes what the server or service does.                              |
| Number   | `01`, `02`                              | Increments with multiple instances.                                     |
| Domain   | `storagevault.me` or alternative domain |                                                                         |
## 🖥 TrueNAS Naming

**Main NAS Hostname:**

HOMELAB-NAS-STOR-01.storagevault.me

**Storage Pools:**

- `pool-media`
    
- `pool-backup`
    
- `pool-vm`
    
- `pool-archive`
    

**Datasets/Shares:**

- `dataset-media-movies`
    
- `dataset-media-tv`
    
- `dataset-backups-pc`
    
- `dataset-vm-images`
    

**Snapshots:**

- `snap-datasetname-daily-YYYYMMDD`
    
- `snap-datasetname-weekly-YYYYMMDD`

## 🐳 Portainer Servers Naming

**First Portainer Server:**

HOMELAB-CTR-CORE-01.storagevault.me

Second Portainer Server:

HOMELAB-CTR-CORE-02.storagevault.me

**Docker Containers inside Portainer:**

- `srv-web-nginx-01`
    
- `srv-db-postgres-01`
    
- `srv-app-homeassistant-01`
    
- `srv-app-plex-01`
    

**Stacks:**

- `stack-monitoring`
    
- `stack-homeautomation`
    
- `stack-webapps`

## 🌐 Domain and Subdomain Structure

**Primary Domain:** `storagevault.me`

**Suggested Subdomains:**

- `nas.storagevault.me` - Access to TrueNAS UI
    
- `portainer.storagevault.me` - Access to Portainer management
    
- `cloud.storagevault.me` - Cloud services
    
- `apps.storagevault.me` - Web applications
    

**Alternate Domain Ideas (optional if expanding beyond storage):**

- `vaultlab.me`
    
- `hivevault.net`
    
- `nexuslab.io`
    
- `bytevault.net`
    
- `labvault.io`
    

---

## 📜 Quick Reference Table

|Server/Service|Hostname|Notes|
|---|---|---|
|TrueNAS Main|`HOMELAB-NAS-STOR-01.storagevault.me`|Storage server|
|Portainer #1|`HOMELAB-CTR-CORE-01.storagevault.me`|Main container server|
|Portainer #2|`HOMELAB-CTR-CORE-02.storagevault.me`|Secondary container server|
|NGINX container|`srv-web-nginx-01`|Reverse proxy|
|Postgres DB container|`srv-db-postgres-01`|Database backend|
|Home Assistant Stack|`stack-homeautomation`|Smart home automation|
# ✅ Notes

- Maintain consistent naming across **servers**, **shares**, **containers**, and **stacks**.
    
- Avoid abbreviations that are too obscure for easier maintenance.
    
- Use leading zeros for numbers to ensure sorting consistency (`01`, `02`, `03`...).
    
- Regularly update the README if the structure grows or changes.



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
