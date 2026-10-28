<div align="center">

# 🔐 Cybersecurity Lab Environment Setup

**Building an isolated virtual lab for penetration testing and ethical hacking practice**
</div>

<p align="center">
  <img src="https://img.shields.io/badge/Skill-Cybersecurity-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ver-Virtualbox%20v7.2-0070C0?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Kali%20Linux-v2026.2-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Linux-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Network-10.0.0.0%2F24-238F89?style=flat-square&labelColor=000000" />
  <img src="https://img.shields.io/badge/Penetration%20Testing-C00000?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Skill-Virtualization-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/GitHub-404040?style=flat-square&labelColor=0070C0&logo=github&logoColor=white" />
  <img src="https://img.shields.io/badge/Kali%20Linux-404040?style=flat-square&labelColor=C00000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/NetworkWalks-404040?style=flat-square&labelColor=C00000" />
  <img src="https://img.shields.io/badge/Ethical%20Hacking-E87500?style=flat-square&labelColor=000000&logo=kalilinux&logoColor=white" />
  <img src="https://img.shields.io/badge/Waqas%20Karim%20CCIE-C00000?style=flat-square" />
</p>

---

## 🛡️ Purpose of the Lab
The lab provides an isolated and controlled environment for cybersecurity learning and authorized security testing. It supports activities such as:
* Network reconnaissance & port scanning
* Vulnerability assessment & packet analysis
* Web security testing & exploitation practice
* Security-tool experimentation

> ⚠️ **Disclaimer:** This laboratory environment is intended strictly for educational purposes, self-hosted training, and authorized systems where explicit permission has been granted.

---

## 🏗️ Architecture & Network Topology

```text
+-------------------------------------------------------------+
|                     Host Machine (OS)                       |
|                                                             |
|   +-----------------------------------------------------+   |
|   |                  Oracle VirtualBox                  |   |
|   |                                                     |   |
|   |   +-------------------+       +-----------------+   |   |
|   |   |  Kali Linux (VM)  | <---> | Target VM (Opt) |   |   |
|   |   |  IP: 10.0.0.2     |       | IP: 10.0.0.x    |   |   |
|   |   +-------------------+       +-----------------+   |   |
|   |             ^                                       |   |
|   +-------------|---------------------------------------+   |
|                 v                                           |
|       [ Virtual NAT Network: 10.0.0.0/24 ]                  |
+-------------------------------------------------------------+
🪜 Lab Setup Procedure
Step 1: Install Required Tools & Hypervisor
VirtualBox: Installed as the core hypervisor to manage virtual machines.

Archiving Utilities: Installed 7-Zip or native extraction utilities to extract compressed Kali Linux virtual machine packages (.7z or .ova).

Step 2: Create the NAT Network
To allow internal routing between lab machines while safely segregating traffic from the physical host network:

Open Oracle VirtualBox Manager.

Go to File → Preferences → Network.

Create a new NAT Network with the following configuration:

Network Name: NatNetwork (or Lab-Network)

IPv4 Prefix: 10.0.0.0/24

DHCP: Enabled

IPv6: Disabled

Step 3: Import and Configure Kali Linux
Download the official virtual machine image from the Kali Linux Downloads page and import it into VirtualBox.

Configure VM settings:

RAM / Base Memory: 2048 MB (or higher based on host capacity)

Processor Cores: 2+ Cores allocated

Configure the virtual network adapter:

Adapter 1: Checked / Enabled

Attached to: NAT Network

Name: NatNetwork

Adapter Type: Intel PRO/1000 MT Desktop

Step 4: Configure Static IP & Network Settings
To ensure reproducible referencing and documentation across future lab exercises, configure a consistent static IPv4 address inside the Kali guest:

IP Address: 10.0.0.2

Subnet Mask: 255.255.255.0

Gateway: 10.0.0.1

DNS Nameserver: 8.8.8.8 (or gateway IP 10.0.0.1)

Step 5: Create a Clean Baseline Snapshot
Power off the Kali VM cleanly.

Open Snapshots in VirtualBox Manager.

Click Take, name the snapshot Clean Kali - Network Setup, and document its baseline configuration. This ensures instant rollback capability if package management or configurations break during subsequent modules.

💡 Key Learnings & Takeaways
NAT vs. NAT Network: Standard NAT allows isolated outbound internet access for a single VM, whereas a VirtualBox NAT Network allows multiple VMs on the same subnet to talk directly to one another—essential for building multi-node lab topologies.

Static IP Addressing: Setting static addressing simplifies mapping targets, writing automation scripts, and executing repeatable network scans.

Disaster Recovery via Snapshots: Creating verified baseline checkpoints before running experimental tools protects system integrity and cuts down troubleshooting time.

📌 Project Metadata
Program / Course: Cybersecurity Laboratory Series

Environment: Oracle VirtualBox & Kali Linux

License: MIT License — see the LICENSE file for details.


<ElicitationsGroup message="To extend or automate this lab setup further:">
  <Elicitation label="Add instructions for integrating Metasploitable as a lab target" query="How do I add Metasploitable 2 or 3 as a target machine inside this VirtualBox NAT network?"/>
  <Elicitation label="Include automation scripts (Vagrant & Bash) for rapid lab deployment" query="Provide automated provisioning scripts and a Vagrantfile to deploy this Kali Linux VirtualBox lab environment automatically."/>
</ElicitationsGroup>ab.
* Configure appropriate IP addressing, gateway, and DNS settings.

---

## 💻 Lab Environment

| Component | Configuration |
| :--- | :--- |
| **Host Operating System** | Windows 11 |
| **Virtualization Platform** | Oracle VM VirtualBox |
| **Security Operating System** | Kali Linux |
| **Network Mode** | NAT Network |
| **Kali Linux IP** | `10.0.0.2/24` |
| **Default Gateway** | `10.0.0.1` |

---

## 📐 Lab Architecture

![Lab Architecture Diagram](lab-architecture.png)

---

## 🛠️ Installation & Setup

### 1. Install VirtualBox
Oracle VM VirtualBox was installed on the host to provide the virtualization environment.

### 2. Configure the NAT Network
A dedicated NAT Network was created in VirtualBox with the following configuration:

| Network Component | Configuration |
| :--- | :--- |
| **Name** | `NatNetwork` |
| **IPv4** | `10.0.0.0/24` |
| **DHCP** | Enabled |
