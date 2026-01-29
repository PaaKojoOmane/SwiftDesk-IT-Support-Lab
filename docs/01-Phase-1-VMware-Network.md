# Phase 1 – Virtualisation & Network Setup

This phase establishes the virtual environment used for the entire lab. A stable and isolated virtual network is critical, as all domain services, clients, and validation depend on reliable connectivity.

The objective of this phase is to prepare VMware Workstation and configure a host-only network that simulates an internal corporate LAN.

---

## Purpose of This Phase

The purpose of this phase is to:

- Install and prepare VMware Workstation for lab use  
- Create an isolated network that does not rely on external connectivity  
- Provide a stable IP addressing foundation for all future phases  

No servers or clients are deployed at this stage. The focus is on **infrastructure readiness**.

---

## Tools and Configuration Used

- **Virtualisation platform:** VMware Workstation  
- **Network type:** Host-Only  
- **Custom network:** VMnet2  
- **IP range:** 10.88.0.0/24  

---

## Network Design Decision

A **Host-Only** network was chosen for this lab instead of NAT or Bridged networking.

This decision was made to:

- Keep the lab isolated from the home or corporate network  
- Avoid DHCP conflicts with external networks  
- Simulate an internal business LAN with no internet dependency  

This mirrors how internal enterprise environments are often segmented from external networks.

---

## Configuration Steps (High Level)

1. VMware Workstation was installed and verified  
2. A custom Host-Only network (VMnet2) was created using the Virtual Network Editor  
3. VMnet2 was configured with the 10.88.0.0/24 address range  
4. DHCP was left enabled for flexibility during early testing  

No virtual machines were created during this phase.

---

## Validation Performed

The following checks confirmed the setup was successful:

- VMnet2 appeared as an available network option in VMware  
- The host machine received an IP address in the 10.88.0.0/24 range  
- VMware networking services were running correctly  

This confirmed the virtual network was ready to support server and client builds.

---

## Screenshots Included

Only key evidence screenshots are included for this phase:

- VMware Workstation installation confirmation  
- Virtual Network Editor showing VMnet2 configuration  
- Host network adapter showing the VMnet2 interface  

(Stored under [assets/screenshots/phase-1](../assets/screenshots/phase-1))

---

## Notes and Lessons

Taking time to configure networking correctly at the beginning prevents cascading issues in later phases, particularly with Active Directory and DNS.

An isolated network also makes troubleshooting simpler, as all traffic remains inside the lab environment.

---

## Next Phase

Proceed to:

- [Phase 2 – Domain Controller Deployment (AD DS + DNS)](02-Phase-2-DC01-AD-DNS.md)
