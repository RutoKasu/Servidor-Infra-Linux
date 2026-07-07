# 🖥️ Linux Infrastructure Lab (`server-infra-linux`)

This repository contains the practical documentation and logbook for my domestic home lab infrastructure. The main goal is to record the networking, administration, and security configurations performed on an old dedicated physical server using Ubuntu Server (CLI environment).

---

## 🏗️ Hardware and System Architecture
*   **Operating System:** Ubuntu Server (Headless / No graphical interface)
*   **Environment:** Dedicated old machine connected via Wi-Fi (configured entirely via CLI) to the local network.

---

## 🔒 Applied Security (Hardening)

### 1. Cryptographic Keys for SSH
*   **What was done:** Default password-based login was disabled inside the `/etc/ssh/sshd_config` file. Remote access now strictly requires a pair of cryptographic digital keys.

### 2. Active Firewall (UFW)
*   **What was done:** Configured a total block policy by default (`Default Deny`). Only network traffic from the following specific ports has been allowed:
    *   Port `22/tcp` (Secure administrative SSH access)
    *   Port `25565/tcp` (Network traffic testing and gaming services)

---

## 🗺️ Next Steps (Roadmap)
- [x] Switch from passwords to digital cryptographic keys in SSH
- [x] Activate and restrict network ports using the UFW Firewall
- [ ] Install Fail2Ban to automatically block suspicious IP addresses
- [ ] Configure a lightweight local DNS server (Pi-hole)
