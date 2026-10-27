# Cybersecurity-Lab-Setup
Step-by-step documentation for setting up an isolated virtual cybersecurity lab using VirtualBox and Kali Linux, featuring a custom 10.0.0.0/24 NAT network configuration.
# <p align="center"> 🛡️ Cybersecurity Lab Environment Setup </p>

<p align="center">
Step-by-step documentation for setting up an isolated virtual cybersecurity lab using VirtualBox and Kali Linux, featuring a custom 10.0.0.0/24 NAT network configuration.
</p>

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
