# Cisco IOS Command Reference Guide

## 1. System Navigation & Modes
| Command | Mode | Description |
| :--- | :--- | :--- |
| `enable` | User EXEC | Enters Privileged EXEC mode. |
| `configure terminal` | Privileged EXEC | Enters Global Configuration mode. |
| `show running-config` | Privileged EXEC | Displays the current active configuration. |
| `write memory` / `copy run start` | Privileged EXEC | Saves the active config to NVRAM. |

## 2. Interface Provisioning
| Command | Mode | Description |
| :--- | :--- | :--- |
| `interface [id]` | Global Config | Enters interface configuration mode. |
| `ip address [ip] [mask]` | Interface Config | Assigns an IPv4 address to the interface. |
| `no shutdown` | Interface Config | Administratively enables the interface. |
| `description [text]` | Interface Config | Adds a label to the interface for documentation. |

## 3. Operational Verification
| Command | Application |
| :--- | :--- |
| `show ip interface brief` | Quick check of all interface states and IP assignments. |
| `show mac address-table` | Verifies Layer 2 CAM table bindings on a switch. |
| `show ip route` | Displays the active Layer 3 routing table. |
| `show arp` | Checks the local IP-to-MAC resolution cache. |
| `show cdp neighbors` | Verifies directly connected Cisco devices. |
