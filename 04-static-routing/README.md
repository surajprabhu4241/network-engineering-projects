# Project 04: Static Routing Between Two Networks

## Objective
The goal of this project is to understand how static routing works by connecting two different networks using two routers. This includes learning how routers communicate and how traffic flows between networks.

---

## Topology
(Insert your topology screenshot here)

---

## Network Design

This lab consists of:
- 2 Routers (R1 and R2)
- 2 Switches
- 2 PCs

### Networks used:
- LAN1: 192.168.1.0/24
- LAN2: 192.168.2.0/24
- Router link: 10.0.0.0/30

---

## IP Addressing

| Device | Interface | IP Address       |
|--------|----------|------------------|
| R1     | Fa0/0    | 192.168.1.1      |
| R1     | Fa0/1    | 10.0.0.1         |
| R2     | Fa0/0    | 192.168.2.1      |
| R2     | Fa0/1    | 10.0.0.2         |
| PC1    | -        | 192.168.1.11     |
| PC2    | -        | 192.168.2.10     |

---

## Configuration

### Router 1 (R1)
- Configured interface Fa0/0 for LAN1
- Configured interface Fa0/1 for router-to-router link
- Added static route to LAN2 network

### Router 2 (R2)
- Configured interface Fa0/0 for LAN2
- Configured interface Fa0/1 for router-to-router link
- Added static route to LAN1 network

---

## Static Routes

- R1 → 192.168.2.0 via 10.0.0.2
- R2 → 192.168.1.0 via 10.0.0.1

This allows both networks to communicate with each other.

---

## Testing

- Ping from PC1 to PC2 initially failed
- After configuring static routes, ping was successful
- Router-to-router connectivity (10.0.0.1 ↔ 10.0.0.2) was verified

---

## Key Concepts Learned

- What a routing table is
- Difference between connected and remote networks
- Static route syntax
- Next-hop concept
- Importance of return path in networking

---

## Troubleshooting

- Faced issue with incorrect interface connections
- Fixed by connecting router-to-router using correct interfaces
- Verified IP addresses and default gateways
- Checked routing tables using `show ip route`

---

## Conclusion

This project helped me understand how routers forward traffic between different networks using static routes and why both forward and return paths are required for successful communication.
