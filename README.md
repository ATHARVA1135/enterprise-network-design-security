# Enterprise Network Design and Security Implementation

## Project Overview
This project simulates an enterprise network using Cisco Packet Tracer. It demonstrates network segmentation, inter-VLAN routing, DHCP configuration, and access control.

## Objectives
- Divide departments into separate VLANs.
- Configure 802.1Q trunking between the switch and router.
- Enable inter-VLAN communication using router-on-a-stick.
- Configure DHCP pools for four VLANs.
- Restrict traffic from the Sales network to the Servers network using an ACL.
- Verify connectivity and practise network troubleshooting.

## Network Topology
![Enterprise Network Topology](%5BEnterprise%20Network%20Topology%5D.png)

The network contains:
- 1 Cisco 2911 router
- 1 Cisco 2960 switch
- 4 PCs
- 1 server

## VLAN and IP Addressing

| VLAN ID | Department | Network | Default Gateway |
|---|---|---|---|
| 10 | HR | 192.168.10.0/24 | 192.168.10.1 |
| 20 | IT | 192.168.20.0/24 | 192.168.20.1 |
| 30 | Sales | 192.168.30.0/24 | 192.168.30.1 |
| 40 | Servers | 192.168.40.0/24 | 192.168.40.1 |

## Technologies Used
- Cisco Packet Tracer
- VLANs and 802.1Q trunking
- Router-on-a-stick inter-VLAN routing
- IPv4 addressing and subnet masks
- DHCP
- Extended Access Control Lists (ACLs)
- ICMP ping and CLI troubleshooting

## Security Implementation
An extended ACL is applied inbound on the Sales subinterface to deny traffic from `192.168.30.0/24` to `192.168.40.0/24`.

## Verification
- Verified that the router subinterfaces are up/up.
- Verified that the switch trunk carries VLANs 10, 20, 30, and 40.
- Verified that PC1 in the IT VLAN received an IP address automatically through DHCP.
- Verified successful connectivity to the server from the router.
- Tested the Sales-to-Servers ACL.

**Known issue:** Automatic DHCP assignment and gateway connectivity for the Sales PC still require troubleshooting.

## Project File
Open `Enterprise_Network_Design_Security 1.pkt` using Cisco Packet Tracer to inspect the topology and configurations.

## Learning Outcomes
This project provided hands-on practice with VLAN configuration, inter-VLAN routing, DHCP, ACLs, and systematic network troubleshooting.
