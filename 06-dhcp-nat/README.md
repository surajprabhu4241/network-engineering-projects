# Project 6: DHCP and NAT Lab

## Overview
This project demonstrates DHCP and NAT configuration using Cisco Packet Tracer.

## Topology
PC1 and PC2 connect to a switch. The switch connects to R1. R1 connects to R2, which simulates an outside network.

## IP Plan
| Device | Interface | IP Address |
|---|---|---|
| R1 | Fa0/0 | 192.168.1.1 |
| R1 | Fa0/1 | 10.0.0.1 |
| R2 | Fa0/0 | 10.0.0.2 |
| R2 | Loopback0 | 8.8.8.8 |
| PC1 | DHCP | 192.168.1.x |
| PC2 | DHCP | 192.168.1.x |

## What I Configured
- DHCP on R1
- NAT overload on R1
- Inside and outside NAT interfaces
- Default route from R1 to R2

## Testing
- Verified PC received DHCP address
- Pinged default gateway: 192.168.1.1
- Pinged outside network: 8.8.8.8

## Troubleshooting
The PC first received a 169.254.x.x APIPA address, which meant DHCP failed. I fixed the issue by checking the router interface, correcting the connection, enabling the interface, and refreshing DHCP on the PC.

## Key Learning
DHCP gives IP addresses to clients. NAT translates private IP addresses to outside addresses so internal devices can reach an outside network.
