

# 🐉 My Kali Linux Setup Journey: Overcoming the 32-Bit Wall

This repository documents my experience setting up a professional penetration testing environment on Windows 11 and how I bypassed common virtualization conflicts.

---

### 📝 The Problem
While attempting to install Kali Linux on **VirtualBox**, I encountered several critical blockers:
* 🛑 **32-Bit Only:** VirtualBox restricted all OS options to 32-bit versions.
* 🛑 **Hyper-V Conflict:** Attempting to disable Hyper-V via PowerShell failed with the error: `Feature name Windows-Hypervisor-Platform is unknown`.
* 🛑 **Performance Issues:** The environment was sluggish and system features remained locked.

---

### 🛠 The Solution: The "VMware Switch"
Instead of struggling with Windows 11’s deep-rooted Hyper-V/Core Isolation settings, I pivoted to **VMware Workstation Pro**, which handles modern Windows virtualization much more effectively.

#### ➤ Step-by-Step Fix:
1. **Official Download:** Acquired VMware Workstation Pro from the Broadcom Support Portal (now free for personal use!).
2. **Kali Image:** Downloaded the **Pre-built VMware image** (`.7z`/`.zip`) from [Kali.org](https://www.kali.org/get-kali/#kali-virtual-machines).
3. **Extraction:** Unzipped the package to locate the `.vmx` configuration file.
4. **The "Copy" Rule:** When importing, I selected **"I Copied It"** to ensure all hardware settings were localized to my machine.

#### ➤ Post-Install Setup (Terminal Operations):
Once logged in, I ran these essential commands to modernize the system:

```bash
# Update the package list
sudo apt update

# Upgrade all tools and the kernel
sudo apt full-upgrade -y

# Clean up unnecessary files
sudo apt autoremove -y
```
---
## 🛠 Skills & Tools
I am currently building my expertise in the following areas:

### 🛡️ Cybersecurity & OS
![Kali Linux](https://img.shields.io/badge/Kali%20Linux-557C94?style=for-the-badge&logo=kali-linux&logoColor=white)
![Linux](https://img.shields.io/badge/Linux-FCC624?style=for-the-badge&logo=linux&logoColor=black)
![VMware](https://img.shields.io/badge/VMware-607078?style=for-the-badge&logo=vmware&logoColor=white)

### 💻 Networking & Scripting
![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Bash](https://img.shields.io/badge/Bash-4EAA25?style=for-the-badge&logo=gnu-bash&logoColor=white)
![Networking](https://img.shields.io/badge/Networking-005963?style=for-the-badge&logo=cisco&logoColor=white)

### 🎯 Current Focus
* 🕵️‍♂️ Network Penetration Testing
* 🛡️ Hardening Virtual Environments
* 🐚 Advanced Bash Scripting
