# ha-makerspace

Home Assistant configuration snapshot for the **Makerspace** instance.  
Managed by Home Assistant Version Control — direct edits may be overwritten.

## Instance status

| Item | Value | Status |
|---|---|---|
| Hardware | Beelink EQ14 (Intel N100, 16 GB RAM) | ✅ Running |
| OS | Home Assistant OS (HAOS) | ✅ Running |
| Data disk | NVMe only | ⚠️ Seagate Skyhawk 4TB pending |
| HA URL | http://192.168.1.12:8123 | ✅ (verify at router) |

## Add-ons

| Add-on | Status |
|---|---|
| Frigate (Full Access) 0.17.1 | ✅ Running |
| Mosquitto MQTT broker | ✅ Running |
| HACS | ✅ Running |
| Home Assistant Version Control | ✅ Auto-pushing |

## Custom components

| Component | Purpose |
|---|---|
| frigate | Frigate NVR HA integration |
| bambu_lab | Bambu Lab 3D printer |
| browser_mod | Browser customization |

## Cameras (Frigate)

| Name | Model | IP | Detect resolution | Status |
|---|---|---|---|---|
| doorbell | Reolink D340P | 192.168.1.84 | 480×640 portrait | ✅ Live |
| main_hall | Reolink Duo 2 | 192.168.1.120 | 1280×388 (3.3:1) | ✅ Live |
| robotics | Reolink Duo 2 | 192.168.1.21 | 1280×388 (3.3:1) | ✅ Live |
| craft_room | Reolink Duo 2 | 192.168.1.22 | 1280×388 (3.3:1) | ✅ Live |
| TBD (5th) | TBD | TBD | TBD | ⏳ Not installed |

## Detectors

| Detector | Type | Inference | Status |
|---|---|---|---|
| cpu1 | CPU (4 threads) | ~64 ms | ⚠️ Temporary — awaiting Coral fix |
| coral | Google Coral USB TPU | — | ⚠️ Stuck in bootloader — needs data-disk migration |
| VAAPI | Intel iHD (N100 iGPU) | — | ✅ Active (~6–8% GPU) |

## Dashboards

| Dashboard | Status |
|---|---|
| lovelace (default) | ✅ |
| map | ✅ |

## Pending

- Purchase Seagate Skyhawk 4TB → format ext4 → move data disk → Coral TPU will work
- Add Frigate HA integration
- Build Mushroom dashboard
- Install 5th camera

## Related repositories

- [`ha-fleet-context`](https://github.com/alexcua/ha-fleet-context) — shared docs, setup procedures, workarounds
- `ha-home` — Home instance
- `ha-office` — Office instance
