# Windows Server 2022 Home Lab – VMware Workstation Setup

This repository documents my personal lab project where I installed and configured a 64-bit Windows Server 2022 environment using VMware Workstation. This lab covers server configuration, network setup, Active Directory, DNS, DHCP, and system administration tools.

### 1. Install VMware Workstation and Windows Server 2022 ISO
> 💡 **NOTE**: Make sure your computer meets the recommended hardware requirements before setting up a VMware home lab.
- Download VMware Workstation Player: https://www.vmware.com/
- Download Windows Server 2022 ISO (Evaluation): https://info.microsoft.com/ww-landing-windows-server-2022.html

### 2. Create and Install the Windows Server VM

- Open VMware Workstation and create a new VM
- Select “Installer disc image file (ISO)” and choose your ISO
- Guest OS Type: Microsoft Windows > Windows Server 2022
- Set 2 processors and 4096–8192 MB RAM (based on host system)
- Allocate at least 60 GB of disk space
- Power on and install Windows Server 2022 (Datacenter Desktop Experience)

### 3. Configure Network and Access Settings

- Set a static IP address via:
  - Open Control Panel > Network and Sharing Center > Change adapter settings
  - Right-click adapter > Properties > IPv4 > Use the following IP:
    - IP: `192.168.1.10`
    - Subnet: `255.255.255.0`
    - Gateway: Leave blank for isolated lab with Domain Controller as gateway
    - DNS: `127.0.0.1`
      
- Enable Remote Desktop via `sconfig`:
  - Option 7 → then Option 3 (Enable with Network Level Authentication)

- Use Server Manager for additional system config
