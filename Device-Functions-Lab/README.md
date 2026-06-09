# Cisco Device Functions: MAC & Routing Tables

## Project Overview
This project explores the operational mechanics of Layer 2 and Layer 3 data forwarding using Cisco IOS. By analyzing the behavior of Catalyst switches and Cisco routers under an active traffic load, this lab demonstrates how network devices build localized forwarding logic dynamically.

## Core Lab Objectives
1. **Layer 2 Verification:** Trace physical hardware MAC addresses across dynamic switch address tables to analyze local frame forwarding logic.
2. **Layer 3 Interface Provisioning:** Configure logical IP subnets and bring secure, administratively closed interfaces online via the Cisco IOS CLI.
3. **Routing Table Analysis:** Examine the populating of directly connected (`C`) and local (`L`) host routes within the routing engine.

## Topology Specifications
* **Core Subnet Space:** `10.10.10.0/24`
* **Provisioned Subnet Space:** `10.10.20.0/24`
* **Devices Deployed:** 4 Routers (R1–R4), 2 Interconnected Switches (SW1–SW2)

## Verified Routing Architecture (R1)
| Route Source | Network/Host Destination | Outbound Interface |
| :--- | :--- | :--- |
| **C** (Connected) | `10.10.10.0/24` | GigabitEthernet0/0 |
| **L** (Local Host) | `10.10.10.1/32` | GigabitEthernet0/0 |
| **C** (Connected) | `10.10.20.0/24` | GigabitEthernet0/1 |
| **L** (Local Host) | `10.10.20.1/32` | GigabitEthernet0/1 |

## Key Command Protocols Utilized
* `show ip interface brief` - Verified interface administrative states and IP assignments.
* `show interface [id]` - Extracted burned-in physical MAC addresses.
* `show mac address-table dynamic` - Observed real-time Layer 2 CAM table state mapping.
* `show ip route` - Analyzed the structural topology of the active routing table.
