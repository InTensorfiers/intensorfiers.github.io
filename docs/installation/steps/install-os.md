# 1. Install Operating System

## What is Operating System?

An operating system (OS) is a software system that serves as the core foundation for managing and controlling computer hardware resources and providing a platform for software applications to run. It acts as an intermediary between users, applications, and the computer hardware, enabling efficient and organized interaction between them. The operating system facilitates various essential functions, such as process management, memory management, file system management, and user interface management.
Operating systems come in various types, including Windows, macOS, and Linux, each tailored to specific hardware platforms and user needs.

For our project we are going to focus in Linux OS.

## Linux OS

Linux is an open-source operating system kernel that serves as the foundation for a wide range of different Linux distributions, commonly referred to as "distros." These distributions are built upon the Linux kernel and include various software components to create complete operating systems tailored for different purposes and user preferences. Here are some popular Linux distributions:

- Ubuntu 
- Debian
- Fedora
- Red Hat Enterprise Linux(RHEL)
- CentOS
- etc.

Our primary focus will center on the Debian distribution, given its significance, while we will also give due attention to the Ubuntu distribution within the project's scope. Both Ubuntu and Debian stand out as widely recognized Linux distributions in the Data Science world.

Could be 2 different scenarios, when we can setup a GPU drivers for a machine. 

## a. Virtual Machine Setup

![google image](https://images.unsplash.com/photo-1511296265581-c2450046447d?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=1364&q=80)

For the first scenario, we will conduct our documentation testing on virtual machines. Specifically, we will be utilizing Google Cloud Platform, a powerful cloud-based platform that facilitates the creation of customized instances. This includes tailoring various parameters such as the choice of operating system, regional availability, GPU allocation, and more, based on your precise requirements.

By employing virtual machines, we can emulate diverse computing environments and ensure that our documentation is comprehensive and adaptable to a range of configurations. This allows us to verify the effectiveness of our installation instructions across various settings and configurations.

## b. Phisical Machine 
Constructing a physical machine server designed specifically for hosting machine learning workloads entails establishing the requisite environment to operate Ubuntu or Debian as the operating system on a Linux-based server.

We will provide a high-level description of the installation steps for Ubuntu. You can also refer to the official webpage for guidance on installing your operating system with Ubuntu: [Basic Installation Ubuntu](https://ubuntu.com/server/docs/installation)

![Ubuntu image](https://images.unsplash.com/photo-1629654291663-b91ad427698f?ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D&auto=format&fit=crop&w=3474&q=80)



### 1. Prepare Installation Media
Download the Ubuntu Server ISO file from the official Ubuntu website. You can use this ISO to create a bootable installation media, such as a USB drive or a DVD.
### 2. Boot from Installation Media
Insert the bootable installation media into the server and boot from it. This will initiate the Ubuntu Server installation process.
### 3. Choose Installation Options
Follow the on-screen instructions to select language, time zone, keyboard layout, and other basic settings.
### 4. Configure partitioning and storage options
You might choose to set up separate partitions for the root directory (/), /home, and possibly swap space. The partitioning scheme can vary based on your specific requirements.
### 5. Network Configuration
Configure network settings, including IP address, subnet mask, gateway, and DNS server addresses. This ensures that the server can communicate within the network.
### 6. Software Selection
During the installation process, you'll be prompted to choose software packages. For a machine learning server, you can opt for the "OpenSSH server" package for remote access and administration.
### 7. User Account Setup
Create a user account and set a strong password. This account will have administrative privileges, allowing you to perform system tasks.
### 8. Install Updates
After the installation is complete, update the system's package repository and install any available updates to ensure your server is up to date.

This particular step lies beyond the boundaries of our project's scope; thus, it won't be included in our documentation process. We are operating under the assumption that the machine is already equipped with the necessary operating system, which enables us to proceed. It's important to highlight that even though we're acknowledging these steps, it's pertinent to mention that we intend to test our script within a virtual machine to ensure its validation.
