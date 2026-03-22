# HomeLab Naming Standard

## General Rules
- **Lowercase only** (`truenas`, `pve1`, `vm-db01`)
- **Use hyphens (-)** to separate words (`app-data`, `docker-vol`)
- **Keep names short but descriptive**
- **No special characters** other than hyphens
- **Environment codes** when necessary (e.g., `prod`, `dev`, `test`)

---

## TrueNAS Naming

 - Hostname: truenas-main
	 - Pool: pool-bulk-01 (4x HDD 4TB RaidZ1)
		 - Dataset: ds-media
		 - Dataset: ds-plex
	- Pool: pool-bulk-02 (4x HDD 4TB RaidZ1)
		- Dataset: ds-backups
		- Dataset: ds-family
		- Dataset: ds-gamevault
	- Pool: pool-fast (2x SSD 1TB Mirror)
		- Dataset: ds-portainer
		- Dataset: ds-ix-applications
		- Dataset: ds-apps

> **Notes:**  
> - Pools describe performance or use (`fast`, `bulk`, `archive`)  
> - Datasets describe content (`media`, `backups`, `vm-images`)  
> - Zvols for block storage (e.g., iSCSI, VM disks)

---

## Portainer/Docker Naming

| Type             | Naming Pattern               | Example           |
|------------------|-------------------------------|-------------------|
| Server Hostname  | `docker-xx`                   | `docker-main`     |
| Container Name   | `svc-xx`                      | `svc-pihole`      |
| Volume Name      | `vol-xx`                      | `vol-pihole-data` |

> **Notes:**  
> - `svc` = service  
> - `vol` = persistent storage for service data
---
## Examples

- `truenas-main` hosts `pool-fast`, which has `ds-media`, `ds-backups`, and `zvol-vmstorage`
- `docker-main` runs `svc-pihole` using volume `vol-pihole-data`
- `pve01` runs `vm-db01` with storage `store-fast` and disk `vol-db01-root`
- `unifi-ctrl` manages `switch-core01`, `ap-office01`, and `gw-main`

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
