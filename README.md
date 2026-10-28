# Cybersecurity Lab Setup & Configuration

This repository documents the step-by-step engineering, deployment, and configuration of my isolated virtual cybersecurity laboratory environment used for penetration testing, vulnerability assessment, and malware analysis simulations.

## Network Architecture & Design
* **Hypervisor:** Oracle VM VirtualBox (v7.2+)
* **Network Topology:** Isolated NAT Network
* **Subnet Address Range:** 10.0.0.0/24
* **Gateway IP:** 10.0.0.1
* **Primary Attacking Platform:** Kali Linux 2026.3 (Configured at Static IP: 10.0.0.2)

## Phase 1: Attacker Machine Deployment
1. **Network Provisioning:** Built a custom virtual adapter utilizing a private local pool matching structural compliance blueprints.
2. **OS Extraction & Virtual Disk Mapping:** Utilized multi-threaded compression architectures (`7-Zip`) to preserve raw pre-configured system layouts.
3. **Network Configuration & Bug Fixing:** 
   In newer rolling releases (Kali Linux 2026.x), a network timeout bug drops connection on static configurations. I resolved this system constraint programmatically using the NetworkManager CLI:
   ```bash
   sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0
   sudo nmcli connection down "Wired connection 1"
   sudo nmcli connection up "Wired connection 1"
   ```
4. **State Persistence:** Captured a full environment snapshot titled `Fresh Lab Setup` to maintain a gold-image state.
Endpoint for mobile application security assessments.
