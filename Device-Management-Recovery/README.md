# Lab 5: Device Management & Disaster Recovery

## Deployment Overview
This topology serves as a practical execution of Cisco IOS disaster recovery methodologies and administrative device management. 

## Key Operational Tasks Executed:
* **Password Recovery:** Bypassed the startup configuration via the Configuration Register (0x2142) in ROMMON mode to regain administrative access to a locked router.
* **Disaster Recovery (TFTP):** Simulated a catastrophic loss of the operating system by deleting the IOS `.bin` file from flash memory, followed by rescuing and rebuilding the router using `tftpdnld` from the ROMMON prompt.
* **Configuration Management:** Backed up active routing configurations to a remote TFTP server.
* **IOS Upgrades:** Successfully flashed and deployed a newer Cisco IOS image onto a Catalyst 2960 switch.

*Status: Deployment Complete and Verified.*
