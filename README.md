# WK1-PM1: Cybersecurity Lab Environment Setup

## Objective
Establish a baseline Kali Linux virtualized testing environment using UTM on macOS, verify network configurations, perform host discovery scanning, and create a baseline snapshot backup.

---

## Environment & Configuration
- **Hypervisor:** UTM on macOS (Apple Silicon / ARM64)
- **Virtual Machine:** Kali Linux ARM64
- **Network Interface:** `eth0`
- **Assigned IP Address:** `192.168.64.4/24`
- **Gateway Address:** `192.168.64.1`

---

## Execution Steps & Results

### 1. Network Interface Verification
Executed `ip a` to confirm local subnet parameters and network interface binding.
- **Result:** Interface `eth0` successfully obtained IP address `192.168.64.4/24`.

### 2. Reconnaissance & Host Discovery Scan
Executed an `nmap` ping sweep across the local `/24` subnet:
```bash
sudo nmap -sn 192.168.64.0/24
