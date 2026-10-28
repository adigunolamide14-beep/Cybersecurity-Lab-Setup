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
<p align="center">
  <img src="https://img.shields.io/badge/PROJECT-ISOLATED%20CYBERSECURITY%20LAB-green?style=for-the-badge">
  <img src="https://img.shields.io/badge/HYPERVISOR-VIRTUALBOX-blue?style=for-the-badge">
  <img src="https://img.shields.io/badge/OS-KALI%20LINUX-orange?style=for-the-badge">
  <img src="https://img.shields.io/badge/SUBNET-10.0.0.0%2F24-teal?style=for-the-badge">
  <img src="https://img.shields.io/badge/SKILL-PENETRATION%20TESTING-red?style=for-the-badge">
</p>

---

## 🚀 Project Overview

This project documents the setup of an isolated virtual cybersecurity laboratory using Oracle VM VirtualBox and Kali Linux. 

The lab provides a controlled environment for practicing cybersecurity concepts, network reconnaissance, vulnerability assessment, and penetration-testing techniques in a safe and authorized environment.

---

## 🎯 Objectives

* Install and configure Oracle VM VirtualBox and Kali Linux.
* Build an isolated virtual cybersecurity laboratory.
* Configure a custom NAT Network for the virtual lab.
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
