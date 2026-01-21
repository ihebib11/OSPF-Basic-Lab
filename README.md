# OSPF-Basic-Lab
OSPF (Open Shortest Path First) is a fast, scalable routing protocol used to efficiently exchange routes within and between areas in a network. This lab demonstrates multi-area OSPF configuration and basic best practices.
## Topology
<img width="1150" height="645" alt="Topologie" src="https://github.com/user-attachments/assets/87525b9b-7024-487c-a997-92a914b2e262" />

## Lab Environment
The network emulator used is EVE-NG.
- 3 × Cisco CSR1000v (IOS XE 16.x)
- 3 × Cisco vIOS Switch
- 6 × VPCs
* OSPF Areas:
  - Area 0 (Backbone)
  - Area 1 (LAN1)
  - Area 2 (LAN2)
  - Area 3 (LAN3)

## Lab Steps
1. Configure IP addresses (without OSPF)
2. Enable OSPF on backbone (Area 0)
3. Advertise LAN networks into the correct areas
4. Configure passive interfaces on LANs to stop unnecessary OSPF hello messages.

Configs for all 3 routers (R1, R2, R3) are in the `configs/` folder.
