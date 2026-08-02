# ha-makerspace

Home Assistant configuration snapshot for the **Makerspace** instance.

This repository is managed by the Home Assistant Version Control add-on. Direct edits may be overwritten by a later synchronization from Home Assistant.

## What this repository contains

- YAML configuration files (`configuration.yaml`, automations, scripts, scenes)
- Lovelace dashboard definitions
- Add-on configurations (where included by Version Control)

## What this repository does NOT contain

- `secrets.yaml` or any credentials
- Database files
- Log files
- Backups
- Private keys or certificates

## Instance summary

| Item | Value |
|---|---|
| Hardware | Beelink EQ14 (Intel N100, 16 GB RAM) |
| OS | Home Assistant OS (HAOS) |
| Frigate | 0.17.1 (Full Access add-on) |
| Coral TPU | Google Coral USB — pending drive migration |
| Storage | NVMe only — Seagate Skyhawk 4TB pending |
| HA URL | http://192.168.1.12:8123 (verify at router) |

## Cameras in Frigate

| Name | Model | IP | Notes |
|---|---|---|---|
| doorbell | Reolink D340P | 192.168.1.84 | 480×640 portrait detect |
| main_hall | Reolink Duo 2 | 192.168.1.120 | 1280×388 detect (3.3:1) |
| robotics | Reolink Duo 2 | 192.168.1.21 | 1280×388 detect (3.3:1) |
| craft_room | Reolink Duo 2 | 192.168.1.22 | 1280×388 detect (3.3:1) |

5th camera pending installation.

## Pending

- Seagate Skyhawk 4TB — purchase and install for data disk migration
- Coral TPU will work after data disk migration (same fix as Home instance)
- 5th Reolink camera installation

## Related repositories

- Shared documentation and setup procedures: [`ha-fleet-context`](https://github.com/alexcua/ha-fleet-context)
- Home instance: `ha-home`
- Office instance: `ha-office`

For installation procedures, hardware details, Frigate config patterns, and known workarounds see `ha-fleet-context`.
