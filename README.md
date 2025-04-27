# HomeLab Naming Standard

## General Rules
- **Lowercase only** (`truenas`, `pve1`, `vm-db01`)
- **Use hyphens (-)** to separate words (`app-data`, `docker-vol`)
- **Keep names short but descriptive**
- **No special characters** other than hyphens
- **Environment codes** when necessary (e.g., `prod`, `dev`, `test`)

---

## TrueNAS Naming

| Type            | Naming Pattern               | Example         |
|-----------------|-------------------------------|-----------------|
| Server Hostname | `truenas-xx`                  | `truenas-main`  |
| Pool            | `pool-xx`                     | `pool-fast`     |
| Dataset         | `ds-xx`                       | `ds-backups`    |
| Zvol            | `zvol-xx`                     | `zvol-vmstorage`|

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

## Proxmox Naming

| Type            | Naming Pattern               | Example         |
|-----------------|-------------------------------|-----------------|
| Node Name       | `pve-xx`                      | `pve01`          |
| VM/CT Name      | `vm-xx` / `ct-xx`              | `vm-db01`, `ct-nginx01` |
| VM/CT Storage   | `store-xx`                    | `store-fast`    |
| Volume Name     | `vol-xx`                      | `vol-db01-root` |

> **Notes:**  
> - `vm` = virtual machine  
> - `ct` = container (LXC)  
> - `store` = pool or storage backend (local-lvm, ZFS, NFS, etc.)

---

## UniFi Naming (Future)

| Type             | Naming Pattern               | Example          |
|------------------|-------------------------------|------------------|
| Controller       | `unifi-ctrl`                  | `unifi-ctrl`     |
| Switch           | `switch-xx`                   | `switch-core01`  |
| AP (Access Point)| `ap-xx`                       | `ap-lr01`        |
| Gateway          | `gw-xx`                       | `gw-main`        |

> **Notes:**  
> - Switches/APs based on location (`core01`, `lab01`, `office01`)  
> - APs can indicate model if needed (`lr`, `nano`, etc.)

---

## Examples

- `truenas-main` hosts `pool-fast`, which has `ds-media`, `ds-backups`, and `zvol-vmstorage`
- `docker-main` runs `svc-pihole` using volume `vol-pihole-data`
- `pve01` runs `vm-db01` with storage `store-fast` and disk `vol-db01-root`
- `unifi-ctrl` manages `switch-core01`, `ap-office01`, and `gw-main`

---

## Future-proofing Tips
- Reserve numbers for clusters (`pve01`, `pve02`, etc.)
- Keep pool and volume names generic enough for expansion
- Use descriptive but short service names for docker containers
- Name devices based on function and location


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
