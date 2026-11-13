
   <div align="center">
  <h1>🔐 Cybersecurity Lab Environment Setup</h1>
  <p><strong>Building an isolated virtual lab for penetration testing and ethical hacking practice</strong></p>
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
  <img src="https://img.shields.io/badge/%20Brian%20BSC-C00000?style=flat-square" />
</p>

---

## 📋 Project Overview

This project focuses on setting up a **virtual cybersecurity and penetration-testing laboratory** using VirtualBox and Kali Linux.

The purpose of the lab is to create a controlled environment where cybersecurity tools, network scanning, reconnaissance, vulnerability assessment, and other security-testing activities can be performed safely and repeatedly.

The lab is configured on a private virtual network so that additional machines can be added later and used as targets for authorized security testing.

---
The main objectives of this project are to: 

✅ Install and configure 7-Zip. 

✅ Install and configure Oracle VirtualBox. 

✅ Install or import Kali Linux as a virtual machine. 

✅ Create a dedicated NAT Network for the cybersecurity laboratory. 

✅ Configure network connectivity for Kali Linux. 

✅ Assign a consistent IP address to the Kali Linux virtual machine. 

✅ Verify network connectivity and test DNS resolution. 

✅ Verify the availability of essential cybersecurity tools. 

✅ Create a clean virtual machine snapshot for recovery. 

✅ Document the complete setup process. 

✅ Prepare the environment for future cybersecurity projects.

---

🛡️ Purpose of the Lab

The laboratory provides a controlled environment for cybersecurity learning and authorised security testing.

It will support practical exercises involving:

🔍 Network reconnaissance

📡 Port scanning

🛠️ Vulnerability assessment

📊 Packet analysis

🌐 Web application security testing

🔐 Penetration-testing tools

🔧 Network troubleshooting

🧪 Security-tool experimentation

## 🏗️ Lab Architecture

![](1-screenshot-title-image.png)

Additional target machines can be added to the same virtual network in future projects.
---

## ⚙️ Lab Configuration

| 🧩 Component       | ⚙️ Configuration   |
| ------------------ | ------------------  |
| 🖥️ Host OS         | Windows 11         |
| 🧠 Host RAM        | 16 GB              |
| ⚡ Processor       | Intel Core i7      |
| 🧰 Hypervisor      | VirtualBox 7.2     |
| 🐉 Security OS     | Kali Linux 2026.3  |
| 🧠 Kali RAM        | 5.8Gi GB (            |
| 🌐 Virtual Network | NAT Network        |
| 📡 Network Address | 10.0.0.0/24        |
| 🐧 Kali IP Address | 10.0.0.3/24        |
| 🚪 Default Gateway | 10.0.0.1           |
| 🌍 DNS Server      | 8.8.8.8            |
| 🔮 Future VM Range | 10.0.0.3–10.0.0.99 |

---

🪜 Lab Setup Procedure

📦 Step 1. Install 7-Zip

7-Zip was installed to extract the Kali Linux virtual-machine package.

Kali Linux virtual-machine downloads may be distributed as compressed archives. The extraction utility is therefore required before importing the virtual machine into VirtualBox.

Tool: 7-Zip

Purpose:

📦 7-Zip Installation and Kali Linux File Preparation

☑️ Extract compressed Kali Linux files.

☑️ Access the virtual-machine installation package.

☑️ Prepare the extracted files for VirtualBox import.

NB: 7-Zip was installed to extract the Kali Linux virtual-machine package, which may be distributed as a `.7z` archive.
**Tool:** 7-Zip

---

## 💻 Step 2. Install VirtualBox

VirtualBox was installed as the hypervisor.

Purpose:

VitualBox was installed as the hypervisor for creating and managing the cybersecurity laboratory.

Purpose:

☑️ Create and manage virtual machines.

🔧 Configure virtual network adapters.

🖥️ Allocate hardware resources.

♻️ Create and restore virtual-machine snapshots.

🔐 Establish a controlled virtual testing environment.

---

## 🌐 Step 3. Create the NAT Network

A dedicated NAT Network was created in VirtualBox to provide connectivity between laboratory virtual machines.

NAT Network Configuration

Configuration:
Network Name: NatNetwork
IPv4 Prefix:  10.0.0.0/24
DHCP:         Enabled
IPv6:         Disabled

<img width="3830" height="2007" alt="NatNetwork settings" src="https://github.com/user-attachments/assets/cd745d5f-12c4-4fbb-abb8-28db9cd78f97" />

**Why NAT Network Was Selected**

A NAT Network allows multiple virtual machines connected to the same virtual network to communicate with one another while providing outbound internet connectivity.

This makes it suitable for a multi-machine cybersecurity laboratory.

It allows:

🖥️ Kali Linux to communicate with target virtual machines.

🌐 Multiple laboratory machines to share the same virtual network.

📡 Outbound internet access for software updates and downloads.

🔗 Communication between virtual machines connected to the same NAT Network.

Unlike standard NAT, NAT Network supports communication between virtual machines connected to the same NAT Network.
This will allow future attacker and target virtual machines to communicate within the laboratory.

---

## 🐉 Step 4. Import Kali Linux

Kali Linux was downloaded from the official Kali Linux website and imported into Oracle VirtualBox.

Kali Linux is a Debian-based operating system designed for penetration testing, digital forensics and information security assessments.

The VM network adapter was configured as follows:

```text

Adapter 1

Enable Network Adapter: Enabled
Attached to:            NAT Network
Network:                NatNetwork
Adapter Type:           Intel PRO/1000 MT Desktop
Promiscuous Mode:       Deny
Cable Connected:        Enabled
```
<img width="3827" height="2042" alt="NatNetwork Adapter type" src="https://github.com/user-attachments/assets/6b79f7d5-e3fd-410f-8f0f-06e61069b4a5" />

💾 Virtual Machine Resource Allocation

The Kali virtual machine was allocated the following resources:

```text
RAM: 6144 MB (6 GB)
<img width="2225" height="1552" alt="RAM Allocation" src="https://github.com/user-attachments/assets/3f02aec6-34bd-4b6b-b477-29bab0ec4e5d" />

```
![](3-screenshot-kali-linux.png)
🗂️ Shared Folder Configuration

A shared folder was also configured to facilitate file transfers between the Windows host operating system and the Kali virtual machine.

This provides a convenient way to exchange laboratory files, scripts and documentation.
<img width="3810" height="1990" alt="Shared folder on Desk Top" src="https://github.com/user-attachments/assets/27701b42-5da9-4406-8d82-d0becbccce08" />

---

📡 Step 5. Configure the Kali Linux Network

The Kali Linux network configuration was checked and configured with a consistent IPv4 address.

A static IPv4 configuration was used to make the Kali machine easier to identify and reference during future laboratory exercises.

IPv4 Configuration

```text
IIP Address:   10.0.0.3
Subnet Mask:  255.255.255.0
Gateway:      10.0.0.1
DNS Server:   8.8.8.8
```

A consistent IP address makes it easier to document the lab and reference the Kali machine in future exercises.

<img width="3182" height="2000" alt="Configure the Kali Linux Network" src="https://github.com/user-attachments/assets/48090d47-da08-4c87-b1ec-986460d050e9" />


## 📸 Step 6. Create a Clean VM Snapshot

After completing the initial Kali Linux installation and network configuration, a VirtualBox snapshot was created.

Snapshot Configuration

Snapshot name:

```text
Clean Kali - Network Setup
```
<img width="1270" height="1030" alt="Clean kali Set Up" src="https://github.com/user-attachments/assets/91bd3e47-ec3e-4732-b629-f33b781f53c2" />

The snapshot represents the clean baseline of the laboratory.

If a future exercise changes or damages the VM configuration, the machine can be restored to this baseline.

---

# 🔎 Lab Verification
After completing the initial configuration, several tests were identified to verify network connectivity and the availability of essential tools.

🧪 Network and System Verification Commands

| ✅ Test                        | 🧾 Command                      | 🎯 Expected Result            |
| ----------------------------- |  ------------------------------ | ------------------------------- |
| 🌐 Check IP address           | `ip a`                          | Correct Kali IP displayed       |
| 📡 Test gateway               | `ping 10.0.0.1`                 | Successful replies              |
| 🌍 Test Internet connectivity | `ping 8.8.8.8`                  | Successful replies              |
| 🔎 Test DNS resolution        | `nslookup networkwalks.com`     | Domain resolves                 |
| 🔎  Check DNS utility         | `nslookup cisco.com`            | Domain resolves                 |
| 🧰 Verify Nmap                | `nmap --version`                | Nmap version displayed          |
| 🔄 Verify snapshot            | Restore snapshot and run `ip a` | Baseline configuration restored |

An additional DNS test can be performed using Cisco:
```text
nslookup cisco.com

### 📊 Example Results

```text
IP Address:
10.0.0.2/24

Gateway:
10.0.0.1

DNS:
8.8.8.8
```

---

🐞 Problems Encountered & Solutions

During the laboratory setup, I encountered network configuration and shared-folder issues. The following documents the problems and how they were resolved.

📡 Problem 1. Network Connectivity After Static IP Configuration

After manually configuring the IPv4 settings in Kali Linux, I experienced network connectivity issues.

Resolution

I used Linux networking commands to inspect the IP address, default gateway and DNS configuration. I also tested connectivity to the gateway and an external IP address, followed by DNS resolution.

Commands used included:

ip addr
ip route
cat /etc/resolv.conf
ping -c 4 10.0.0.1
ping -c 4 8.8.8.8
nslookup networkwalks.com

I also inspected the active network connection using NetworkManager to check the configuration.

Outcome: I was able to verify the network settings and establish connectivity.

📂 Problem 2. VirtualBox Shared Folder Not Appearing on the Kali Linux Desktop

After configuring a shared folder in VirtualBox, it was mounted in Kali Linux but did not initially appear on the desktop.

Resolution

I first checked the mounted directories using:

ls /media/

The command confirmed that the shared folder was mounted and available.

Since the folder was mounted but not visible on the desktop, I created a symbolic link to make it accessible directly from the desktop:

ln -s /media/<shared-folder-name> ~/Desktop/Shared

This created a desktop shortcut named Shared pointing to the mounted VirtualBox shared folder.

Outcome: The shared folder became accessible directly from the Kali Linux desktop, making it easier to exchange files between the Windows host and the virtual machine.

💡 What I Learned

Through this project, I gained practical experience in virtualisation, network configuration and setting up a cybersecurity laboratory.

The key lessons included:

🔀 1. NAT vs NAT Network

I learned that standard NAT provides internet access to an individual virtual machine, while NAT Network also allows multiple virtual machines on the same network to communicate with one another.

🖧 2. Virtual Machine Networking

I learned how to configure VirtualBox network adapters and connect Kali Linux to a dedicated NAT Network.

📍 3. Static IP Configuration

I gained practical experience configuring IP addresses, subnet masks, default gateways and DNS servers. I also learned the importance of ensuring that static IP addresses match the network configuration and do not conflict with other devices.

🔧 4. Network Troubleshooting

I learned how to use Linux networking commands to inspect network settings, test connectivity and identify DNS resolution issues.

📂 5. Shared Folder Configuration

I learned how to configure VirtualBox shared folders, check whether they were mounted in Kali Linux and create desktop shortcuts using symbolic links to make them easily accessible.

♻️ 6. Virtual Machine Snapshots

I learned how snapshots provide recovery points, making it easier to restore a virtual machine to a known working state before further testing or configuration changes.

📝 7. Technical Documentation

I learned the importance of recording configurations, commands, problems, solutions and verification results to make technical work easier to reproduce and maintain.

# 🔐 Security & Ethical Use

This laboratory is intended strictly for education purposes only.

---

# 🔗 Tools & Resources

- **7-Zip:** [https://7-zip.org/download.html](https://7-zip.org/download.html)
- **VirtualBox:** [https://virtualbox.org/wiki/Downloads](https://virtualbox.org/wiki/Downloads)
- **Kali Linux:** [https://kali.org/get-kali](https://kali.org/get-kali)

---

# 👤 Author

**Brian Simpande**\


LinkedIn: https://www.linkedin.com/in/brian-simpande/

---

## 📌 Project Information

**Program Name:** Cybersecurity at Networkwalks | **Week:** 01 | **Project:** Cybersecurity & Pentesting Lab Setup | **Repository:** GitHub
