# Standard Network Troubleshooting Methodology

When approaching a broken lab or failed connectivity test, follow this bottom-up sequence:

1. **Layer 1 (Physical):** Are the interfaces actually `up/up`? (Command: `show ip interface brief`)
2. **Layer 2 (Data Link):** Are the MAC addresses being learned? Is the VLAN correct? (Commands: `show mac address-table`, `show vlan brief`)
3. **Layer 3 (Network):** Is there a valid IP assigned? Is there a route to the destination? (Commands: `show ip route`, `ping`)
4. **Layer 4 (Transport):** Are specific ports being blocked by an ACL?
5. **Layer 7 (Application):** Is DNS resolving the hostname? (Command: `ping [hostname]`)
