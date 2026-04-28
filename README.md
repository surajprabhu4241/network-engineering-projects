# Project 04: Static Routing Between Two Networks

## Objective
Configure static routing between two separate networks using two routers and verify end-to-end connectivity.

---

## Topology
(Insert topology screenshot here)

---

## IP Addressing Table

| Device | Interface | IP Address       | Subnet Mask       |
|--------|----------|------------------|-------------------|
| R1     | Fa0/0    | 192.168.1.1      | 255.255.255.0     |
| R1     | Fa0/1    | 10.0.0.1         | 255.255.255.252   |
| R2     | Fa0/0    | 192.168.2.1      | 255.255.255.0     |
| R2     | Fa0/1    | 10.0.0.2         | 255.255.255.252   |
| PC1    | -        | 192.168.1.11     | 255.255.255.0     |
| PC2    | -        | 192.168.2.10     | 255.255.255.0     |

---

## Configuration

### Router 1 (R1)
