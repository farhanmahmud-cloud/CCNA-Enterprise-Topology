# Cisco Troubleshooting Lab

## Objective
Diagnose and resolve a multi-fault network failure preventing hostnames from resolving across the topology. The lab required isolating issues across Layer 1/2, Layer 3, and Layer 7 to restore full connectivity between routers and a centralized DNS server.

## Topology & Fault Isolation
*   **Layer 1/2 (Physical/Data Link):** Traceroute revealed packet drops at R2. Verified interface status and found `FastEthernet0/0` administratively down. Restored the physical link.
*   **Layer 3 (Network):** Pings to the DNS server succeeded, but hostname resolution failed. Identified that R3 was querying an incorrect DNS IP (`10.10.10.1` instead of `10.10.10.10`). Corrected the local `name-server` configuration on R3.
*   **Layer 7 (Application):** Verified network paths were clear, then isolated the final fault to the host itself. The DNS service application was turned off on the server. Enabled the service to restore functionality.

## Outcome
Full end-to-end hostname resolution restored. R3 successfully resolves and pings R1 by its hostname.
