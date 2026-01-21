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


## 🔍 OSPF Verification

After configuring OSPF on all routers, we check the neighbor adjacencies to ensure proper OSPF operation.

### R1(CSR) OSPF Neighbors
<img width="708" height="82" alt="neighbors r1" src="https://github.com/user-attachments/assets/88f033fd-565f-40fb-b1b8-d253267b0e9b" />

### R1(CSR) OSPF IP routes
<img width="713" height="288" alt="show ip route ospf on R1" src="https://github.com/user-attachments/assets/23121a9e-e9cc-440e-84f7-756549378a97" />

--------------------

### R2(CSR2) OSPF Neighbors
<img width="694" height="96" alt="Neighbors R2" src="https://github.com/user-attachments/assets/28982c27-a7a7-4ec7-92e1-67d22b14ecdb" />

### R2(CSR2) OSPF IP routes
<img width="705" height="256" alt="show ip route ospf on R2" src="https://github.com/user-attachments/assets/b54b6150-2e90-4d66-bff3-acbbad35fbae" />

--------------------

### R3(CSR3) OSPF Neighbors
<img width="750" height="232" alt="Neighbors R3" src="https://github.com/user-attachments/assets/03b86f96-0fae-48eb-8f37-da5fbbb6ae5c" />
### R3(CSR3) OSPF IP routes
<img width="712" height="286" alt="show ip route ospf on R3" src="https://github.com/user-attachments/assets/53ad3394-89f5-4ee0-abac-83de50946ab6" />

--------------------

### TEST Connectivity From VPC on Area1 to VPCs on Area2 and Area3
<img width="641" height="353" alt="ping from area1 to area 2 et area3" src="https://github.com/user-attachments/assets/275b9937-6ac7-4ea2-88db-136b4b073138" />

After OSPF was configured, all VPCs and routers can ping each other successfully, confirming full network connectivity.

### Configuration
Find configs for all 3 routers (R1, R2, R3) are in the `configs/` folder.
