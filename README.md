# Home Assistant Configuration

![Project Maintenance][maintenance-shield]
[![License][license-shield]](LICENSE.md)

[![GitHub Activity][commits-shield]][commits]
[![GitHub Last Commit][last-commit-shield]][commits]

![GitHub Stars][stars-shield]
![GitHub Watchers][watchers-shield]
![GitHub Forks][forks-shield]

## About

This is my personal Home Assistant configuration, running my home automations.

## Server

Home assistant and various other services are mainly run in separate docker containers. Docker (compose) is installed on a Debian 10 Buster VM running on Proxmox-VE. Besides the Debian VM, the server runs an OPNSense Firewall/router vm.

### System

```bash
Proxmox VE
├── OPNSense Firewall
    └── Telegraf
└── Debian 10 Buster
    └── Docker
        ├── DNS: Adguard Home
        ├── Home Asistant: Home Asistant + Postgres Database + ESPHome
        ├── Git: Gitea + Postgres Database
        ├── DSRM: DSMR Reader + Postgres Database
        ├── InfluxDB: Telegraf + InfluxDB + Chronograf + Kapacitor (TICK stack) + Grafana
        ├── Media: Transmission + Radarr + Sonarr + Plex
        ├── VPN: OpenVPN (UDP + TCP)
        ├── Unify: Unify Controller + MongoDB
        ├── MQTT: HiveMQ
        ├── Traefik
        └── Cloud: NextCloud + Mariadb + Redis
```

### Server Specifications

| Part              | Product                                                                                                               | Note          |
|-------------------|:----------------------------------------------------------------------------------------------------------------------|:--------------|
| Processor         | [Intel Core i3-9100](https://tweakers.net/pricewatch/1402228/intel-core-i3-9100-boxed/specificaties/)                 |               |
| Motherboard       | [ASRock H370M-ITX/ac](https://tweakers.net/pricewatch/1162377/asrock-h370m-itx-ac/specificaties/)                     |               |
| CPU cooler        | [Noctua NH-U12S](https://tweakers.net/pricewatch/331490/noctua-nh-u12s-bruin/specificaties/)                          |               |
| Enclosure         | [Fractal Design Node 304 Black](https://tweakers.net/pricewatch/313258/fractal-design-node-304-zwart/specificaties/)  |               |
| Power Supply      | [Corsair CX550M](https://tweakers.net/pricewatch/486673/corsair-cx550m/specificaties/)                                |               |
| RAM               | [Adata XPG Z1 AX4U2400W4G16-QRZ](https://tweakers.net/pricewatch/410906/adata-xpg-z1-ax4u2400w4g16-qrz.html)          | 4x 4GB DDR4   |
| OS SSD            | 256 GB OEM                                                                                                            |               |
| Data HDDs (3x)    | [WD Red (64MB cache), 3TB](https://tweakers.net/pricewatch/315368/wd-red-64mb-cache-3tb/specificaties/)               | RAID 5        |

### Other Network parts

* Synology DS214Play (2x 3TB WD RED)
* UniFi Switch 16 PoE
* UniFi nanoHD Access Point
* APC UPS 950VA BX950U-GR

## Other Noteworthy Configurations

* [frenck](https://github.com/frenck/home-assistant-config)
* [klaasnicolaas](https://github.com/klaasnicolaas/Student-homeassistant-config)
* [Sholofly](https://github.com/Sholofly/home-assistant-config)
* [niro1987](https://github.com/niro1987/homeassistant-config)
* [basnijholt](https://github.com/basnijholt/home-assistant-config)
* [hmmbob](https://github.com/hmmbob/HomeAssistantConfig)

<!-- Links -->
[commits-shield]: https://img.shields.io/github/commit-activity/y/Sanderhuisman/home-assistant-config.svg
[commits]: https://github.com/Sanderhuisman/home-assistant-config/commits/master
[contributors]: https://github.com/Sanderhuisman/home-assistant-config/graphs/contributors
[home-assistant]: https://home-assistant.io
[issue]: https://github.com/Sanderhuisman/home-assistant-config/issues
[license-shield]: https://img.shields.io/github/license/Sanderhuisman/home-assistant-config.svg
[maintenance-shield]: https://img.shields.io/maintenance/yes/2020.svg
[last-commit-shield]: https://img.shields.io/github/last-commit/Sanderhuisman/home-assistant-config.svg
[stars-shield]: https://img.shields.io/github/stars/Sanderhuisman/home-assistant-config.svg?style=social&label=Stars
[forks-shield]: https://img.shields.io/github/forks/Sanderhuisman/home-assistant-config.svg?style=social&label=Forks
[watchers-shield]: https://img.shields.io/github/watchers/Sanderhuisman/home-assistant-config.svg?style=social&label=Watchers
