# SOHO Network Architecture (Class C Subnetting)

## Project Overview
A custom-engineered Small Office / Home Office (SOHO) network architecture designed to manage traffic flow across distinct zones of a residential/office estate. The topology integrates a hardwired infrastructure core with an extended wireless edge, utilizing highly efficient Variable Length Subnet Masking (VLSM) to minimize address waste.

## Network Specifications
* **Base Network Block:** `192.168.50.0` (Class C Address Space)
* **Subnet Mask deployed:** `255.255.255.240` (`/28` CIDR notation)
* **Total Host Capacity:** 16 addresses (14 Usable Host IPs)

### IP Assignment Structure

| Host Description | IP Address | Subnet Mask | Default Gateway |
| :--- | :--- | :--- | :--- |
| Core Router Interface (`Gig0/0/0`) | `192.168.50.1` | `255.255.255.240` | N/A |
| Central File-Server | `192.168.50.2` | `255.255.255.240` | `192.168.50.1` |
| Workstation PCs (Wings 1-3) | `192.168.50.3 - .5` | `255.255.255.240` | `192.168.50.1` |
| Network Printer | `192.168.50.6` | `255.255.255.240` | `192.168.50.1` |
| Wireless Laptops | `192.168.50.7 - .8` | `255.255.255.240` | `192.168.50.1` |
| Mobile Smartphones | `192.168.50.9 - .10` | `255.255.255.240` | `192.168.50.1` |

## Core Competencies Demonstrated
1. **VLSM Subnetting Logic:** Successfully partitioned a standard Class C block down to a `/28` slice to fit specific low-host constraints.
2. **Cisco IOS CLI Configuration:** Configured interface states, static IP addresses, and validated line operations using Cisco IOS core verification commands.
3. **Layer-2/Layer-3 Troubleshooting:** Used internal ARP caching and active ping streams to trace connectivity breaks down to physical endpoint configuration levels.
