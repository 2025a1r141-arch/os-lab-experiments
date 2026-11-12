# 🚀 EXPERIMENT 01
# Installation and Configuration of Oracle VirtualBox and Ubuntu Linux

<p align="center">
  <img src="https://img.shields.io/badge/OPERATING%20SYSTEM-LAB-14213D?style=for-the-badge" />
  <img src="https://img.shields.io/badge/EXPERIMENT-01-2563EB?style=for-the-badge" />
  <img src="https://img.shields.io/badge/UBUNTU-LINUX-E95420?style=for-the-badge&logo=ubuntu&logoColor=white" />
  <img src="https://img.shields.io/badge/VIRTUALIZATION-VIRTUALBOX-183A61?style=for-the-badge" />
</p>

---

## 📌 Table of Contents

1. [Project Overview](#-project-overview)
2. [Objective](#-objective)
3. [Introduction](#-introduction)
4. [Technology Stack](#-technology-stack)
5. [System Requirements](#-system-requirements)
6. [VirtualBox Installation](#-step-1--virtualbox-installation)
7. [Ubuntu ISO Download](#-step-2--ubuntu-iso-download)
8. [Virtual Machine Configuration](#-step-3--virtual-machine-configuration)
9. [Ubuntu Installation](#-step-4--ubuntu-installation)
10. [Verification and Linux Commands](#-verification-and-linux-commands)
11. [Screenshots](#-practical-screenshots)
12. [Learning Outcomes](#-learning-outcomes)
13. [Result](#-result)
14. [Conclusion](#-conclusion)
15. [References](#-references)

---

## 🎯 Project Overview

This experiment demonstrates the practical implementation of virtualization technology using **Oracle VirtualBox** and the installation of **Ubuntu Linux** as a guest operating system.

The project focuses on creating a virtual computing environment, allocating system resources, configuring a virtual machine and deploying Ubuntu without replacing the existing host operating system.

**Project Category:** Operating System Laboratory  
**Experiment Number:** 01  
**Platform:** Oracle VirtualBox  
**Guest OS:** Ubuntu Linux

## 🎯 Objective

To install Oracle VirtualBox, create and configure a virtual machine, and deploy the Ubuntu Linux operating system in a virtualized environment.

### Key Objectives

- Understand virtualization and its applications.
- Install and configure Oracle VirtualBox.
- Create and manage a virtual machine.
- Allocate RAM, CPU and virtual storage.
- Install Ubuntu Linux using an ISO image.
- Verify the successful deployment of Ubuntu.

---

## 📖 Introduction

### 1. Virtualization

Virtualization is a technology that allows multiple operating systems to run on a single physical computer through software-based virtual environments.

Each virtual machine operates independently with its own virtual hardware and operating system.

### 2. Oracle VirtualBox

Oracle VirtualBox is a free and open-source virtualization platform that enables users to create, configure and run virtual machines.

**Major Features:**
- Multiple operating system support.
- Virtual CPU and memory allocation.
- Virtual hard disk management.
- Snapshot and cloning support.
- Isolated testing environments.

### 3. Ubuntu Linux

Ubuntu is a free and open-source Linux-based operating system developed by Canonical.

It provides a graphical desktop environment and command-line interface for software development, system administration and educational purposes.

---

## 💻 Technology Stack

| Technology | Description |
|:---|:---|
| Oracle VirtualBox | Virtualization software |
| Ubuntu Linux | Guest operating system |
| Windows | Host operating system |
| ISO Image | OS installation media |
| Linux Terminal | Command-line interface |

---

## ⚙️ System Requirements

### Hardware Requirements

| Component | Recommended Requirement |
|:---|:---|
| Processor | 64-bit compatible CPU |
| RAM | 8 GB recommended |
| Storage | Sufficient free disk space |
| Virtualization | Hardware virtualization support |

### Software Requirements

- Windows host operating system.
- Oracle VirtualBox.
- Ubuntu Desktop ISO image.
- Internet connection for downloads.

*Actual resource allocation depends on the host computer's hardware.*

---

## 🔹 Step 1 – VirtualBox Installation

1. Visit the official Oracle VirtualBox website.
2. Select the appropriate installer for your host operating system.
3. Download the installation package.
4. Run the installer.
5. Follow the installation wizard.
6. Complete the setup and launch VirtualBox.

Official Download: https://www.virtualbox.org/wiki/Downloads

---

## 🔹 Step 2 – Ubuntu ISO Download

1. Open the official Ubuntu website.
2. Navigate to Ubuntu Desktop.
3. Download the available Ubuntu ISO image.
4. Save the ISO file on your computer.
5. Verify that the download is complete.

Official Website: https://ubuntu.com/download/desktop

**What is an ISO file?**

An ISO file is a disk image containing the files required to install an operating system.

---

## 🔹 Step 3 – Virtual Machine Configuration

Open Oracle VirtualBox and follow these steps:

1. Click on the **New** option.
2. Enter the virtual machine name as Ubuntu.
3. Select Linux as the operating system type.
4. Choose the appropriate Ubuntu version.
5. Allocate suitable RAM.
6. Configure the number of virtual processors.
7. Create a virtual hard disk.
8. Attach the downloaded Ubuntu ISO image.

### Virtual Machine Configuration

| Configuration | Description |
|:---|:---|
| VM Name | Ubuntu |
| OS Type | Linux |
| Version | Ubuntu (64-bit) |
| Memory | Based on host resources |
| Processor | Based on host resources |
| Storage | Virtual hard disk |
| ISO Image | Ubuntu Desktop ISO |

---

## 🔹 Step 4 – Ubuntu Installation

1. Select the newly created virtual machine.
2. Click on **Start**.
3. Wait for the Ubuntu installation screen.
4. Select the installation option.
5. Follow the displayed setup instructions.
6. Complete the installation process.
7. Restart the virtual machine when prompted.
8. Log in to the Ubuntu desktop environment.

**Expected Outcome:** Ubuntu Linux should start successfully inside the VirtualBox virtual machine.

---

## 🖥️ Verification and Linux Commands

After installing Ubuntu, open the Terminal and execute the following commands to examine the system.

### 1. Check Linux Kernel Information

```bash
uname -a
```

Displays kernel and system information.

### 2. Check Ubuntu Version

```bash
lsb_release -a
```

Displays the installed Ubuntu distribution information.

### 3. Check Memory Usage

```bash
free -h
```

Displays available and used memory.

### 4. Check Disk Space

```bash
df -h
```

Displays disk space usage.

### 5. Display Current Directory

```bash
pwd
```

Displays the current working directory.

### 6. List Files and Directories

```bash
ls
```

Displays the contents of the current directory.

---

## 📸 Practical Screenshots

The following screenshots can be added to document the actual implementation.

### Screenshot 01 – VirtualBox Installation

*Evidence of Oracle VirtualBox installation.*

### Screenshot 02 – VirtualBox Manager

*Main interface of Oracle VirtualBox.*

### Screenshot 03 – Virtual Machine Configuration

*Configuration of Ubuntu virtual machine.*

### Screenshot 04 – Ubuntu Installation

*Ubuntu operating system installation process.*

### Screenshot 05 – Ubuntu Desktop Environment

*Successfully running Ubuntu Linux inside VirtualBox.*

---

## 📚 Learning Outcomes

By completing this experiment, the following practical skills are developed:

- Understanding virtualization technology.
- Installing and configuring virtualization software.
- Creating and managing virtual machines.
- Allocating virtual hardware resources.
- Installing Ubuntu Linux.
- Executing basic Linux terminal commands.
- Verifying operating system information.

---

## ✅ Result

Oracle VirtualBox was installed and configured, and an Ubuntu Linux virtual machine was created and deployed.

*Mark this experiment as completed after successfully performing and verifying all installation steps.*

## 📝 Conclusion

This experiment provides practical understanding of virtualization technology and the deployment of Ubuntu Linux using Oracle VirtualBox.

It demonstrates how a virtual machine can provide an independent computing environment within an existing physical system. The experiment also introduces basic Linux system verification and terminal commands.

---

## 🔗 References & Documentation

1. [Oracle VirtualBox Official Website](https://www.virtualbox.org/)
2. [VirtualBox User Manual](https://www.virtualbox.org/manual/)
3. [Ubuntu Official Website](https://ubuntu.com/)
4. [Ubuntu Desktop Documentation](https://help.ubuntu.com/)

---

<p align="center">
  <b>OPERATING SYSTEM LAB</b>
  <br/>
  Computer Science & Engineering
  <br/>
  <i>Learn • Configure • Explore • Implement</i>
</p>
