# MikroTik WiFi Configuration Playbook

Ansible playbook for automated configuration of MikroTik wireless interfaces, including:
- WiFi interface setup
- Security profiles
- DHCP and NAT configuration
- Network infrastructure

## 📌 Features

- **Automatic WiFi interface detection** - Finds and configures primary wireless interface
- **Multi-SSID setup** - Configures master and guest WiFi networks
- **Security** - WPA2-PSK security profile configuration
- **Network services** - DHCP server, IP addressing and NAT setup
- **Idempotent** - Safe for repeated runs

## 🚀 Quick Start
ansible-playbook -i inventory playbook.yml
### Prerequisites
- Ansible 2.9+
- `community.routeros` collection
- MikroTik RouterOS 6.45+ (ROSv7 recommended)
- SSH access to MikroTik device

### Installation
1. Install required Ansible collection:
   ```bash
   ansible-galaxy collection install community.routeros
🔧 Customization
Variables to Modify:
ssid - Your wireless network name

wpa2_psk - WiFi password (minimum 8 characters)

wifi_network - IP subnet for wireless clients

dhcp_range - DHCP address pool range

Advanced Options:
Change country setting in "Configure master wireless settings" task
