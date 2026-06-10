# The Life of a Packet: DNS & ARP Resolution

## Project Overview
This project demonstrates the lifecycle of a packet traversing a routed network, focusing specifically on Domain Name System (DNS) resolution and Address Resolution Protocol (ARP) caching within Cisco IOS. The lab verifies how routers utilize external DNS servers for hostname translation and maps the boundaries of Layer 2 broadcast domains.

## Core Lab Objectives
1. **DNS Client Provisioning:** Configured Cisco routers to query a centralized DNS server for hostname-to-IP address resolution without utilizing local host tables.
2. **Name Resolution Verification:** Executed ICMP echo requests using logical hostnames to validate the DNS query-and-response cycle across multiple subnets.
3. **ARP Cache Analysis:** Inspected router ARP tables to verify that Layer 2 MAC address resolution is strictly limited to directly connected local area networks.

## Topology Specifications
* **DNS Server Address:** `10.10.10.10`
* **Network Segments:** `10.10.10.0/24` and `10.10.20.0/24`
* **Devices Deployed:** 3 Cisco Routers (R1, R2, R3), 2 Layer 2 Switches, 1 DNS Server

## Key Architectural Learnings
* **The ARP Broadcast Boundary:** ARP requests utilize broadcast traffic (`FF:FF:FF:FF:FF:FF`), meaning they are inherently blocked by router interfaces. As demonstrated in the lab outputs, a router will never hold an ARP entry for a device on a remote subnet; it relies on the MAC address of its local default gateway (next-hop router) to forward the packet.

## Key Command Protocols Utilized
* `ip domain-lookup` & `ip name-server` - Enabled DNS queries and pointed the router to the centralized server.
* `ping [hostname]` - Triggered the DNS resolution process and verified end-to-end ICMP reachability.
* `show arp` - Extracted the local ARP cache to map active IP-to-MAC hardware bindings.
