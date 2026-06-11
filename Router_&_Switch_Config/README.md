# Cisco Router and Switch Basics: Initial Provisioning & Security

## Project Overview
This project demonstrates the foundational provisioning of Cisco IOS devices. The lab covers the initial configuration of management interfaces, physical port parameter tuning, and the mitigation of Layer 2 reconnaissance by disabling Cisco Discovery Protocol (CDP) on outward-facing interfaces.

## Core Lab Objectives
1. **Device Provisioning:** Configured device hostnames, interface IP addressing, and a management VLAN interface with a configured default gateway for remote switch access.
2. **Link Parameter Hardcoding:** Bypassed auto-negotiation by manually hardcoding port speed (`100 Mbps`) and duplex (`full`) to ensure deterministic link states.
3. **CDP Mitigation:** Disabled Cisco Discovery Protocol on specific interfaces to prevent unauthorized hardware and topology discovery from adjacent devices.

## Topology Specifications
* **Management IP (SW1):** `10.10.10.10/24` (VLAN 1)
* **Switch Default Gateway:** `10.10.10.2` (via R2)
* **Connected Routers:** R1 (`10.10.10.1`), R2 (`10.10.10.2`)

## Key Command Protocols Utilized
* `ip default-gateway` - Configured the gateway of last resort for the Layer 2 switch management interface.
* `speed 100` & `duplex full` - Hardcoded interface link parameters.
* `no cdp enable` - Disabled Layer 2 CDP broadcast frames on an interface-by-interface basis.
* `show cdp neighbors` - Verified that the router could no longer build a topology map of the switch.
