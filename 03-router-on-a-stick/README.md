# Project 3 - Inter-VLAN Routing (Router-on-a-Stick)

## Objective
Configure VLANs and allow communication between different VLANs using a Cisco router.

## Topology
- 1 Cisco 2811 Router
- 1 Cisco 2960 Switch
- 4 PCs

## VLANs
- VLAN 10 = Sales
- VLAN 20 = HR

## IP Addressing
### Sales
- PC0: 192.168.10.11
- PC1: 192.168.10.12
- Gateway: 192.168.10.1

### HR
- PC2: 192.168.20.11
- PC3: 192.168.20.12
- Gateway: 192.168.20.1

## Switch Configuration
- Created VLAN 10 and VLAN 20
- Assigned access ports
- Configured trunk port to router

## Router Configuration
- Subinterface Fa0/0.10
- Subinterface Fa0/0.20
- Used encapsulation dot1Q

## Verification
- Same VLAN ping successful
- Inter-VLAN ping successful

## Skills Learned
- VLANs
- Trunking
- Subinterfaces
- Default Gateway
- Inter-VLAN Routing
- Troubleshooting
