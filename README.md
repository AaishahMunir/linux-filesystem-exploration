README.txt
==========

Title: Linux File System Basics – Exploration & Notes

Author: [Aaishah Munir]
Date: [03-08-2025]

Overview:
---------
This repository contains my notes and practical lab work while learning the structure of the Linux file system and understanding the Filesystem Hierarchy Standard (FHS). It also includes command-line operations I performed to explore and analyze directories, system configuration files, logs, and more.

Topics Covered:
---------------

1. File System Basics:
   - The Linux file system starts from the root directory `/`.
   - Everything in Linux is treated as a file, including physical devices.

2. Key Linux Directories Explored:
   --------------------------------
   - `/`       : Root directory
   - `/home`   : Contains personal user directories (e.g., /home/cybrary)
   - `/etc`    : Stores critical system configuration files
   - `/var/log`: Contains system log files
   - `/usr`    : Contains executables, libraries, documentation
   - `/usr/bin`: Contains user-level executable files
   - `/usr/sbin`: Contains administrative tools (requires sudo)
   - `/dev`    : Contains device files (e.g., hard drives, null, urandom)
   - `/mnt`    : Temporary mount point for devices like USBs or CDs
   - `/proc`   : Virtual directory showing real-time running processes
   - `/boot`   : Contains bootloader and kernel files

3. Commands Used:
   ---------------
   - `cd /` → Move to root directory
   - `ls -l` → List files in long format with permissions and ownership
   - `tree / -L 1` → Visualize directory structure up to 1 level
   - `sudo tree /home` → Show user home directories
   - `ls /etc` → View system configuration files
   - `ls /var/log` → See system log files
   - `sudo last` → View last login records from `/var/log/lastlog`
   - `sudo who` → View current users from `/var/log/wtmp`
   - `sudo tail -f /var/log/syslog` → Monitor live system logs
   - `ls /usr`, `ls /opt`, `ls /dev`, `ls /mnt` → View specific system areas
   - `sudo fdisk -l | grep dev | grep -v loop` → List physical storage devices
   - `sudo df -h` → Show mounted file systems with human-readable size
   - `lsblk` → List block storage devices
   - `ps -e` → Show all running processes

4. Permissions:
   -------------
   - Each file/directory has three permission groups: owner, group, others.
   - Permissions are shown as `rwx` (read, write, execute).
   - Example: `drwxr-xr-x` shows full access for owner, read+execute for others.

5. Special Topics:
   ----------------
   - Symbolic links (shown as `l` in `ls -l`) act like Windows shortcuts.
   - Device files in `/dev` are not human-readable but allow software to communicate with hardware.
   - `flag` files (if present) in `/dev` or `/usr/sbin` can be explored using `sudo cat flag`.

How to Use:
-----------
This repo is for learning and reference purposes. You can use the listed commands in your terminal to explore a Linux system and understand how data, configuration, logs, and devices are organized.

Note:
-----
- Always be cautious when using `sudo`.
- Do not delete or modify files in `/etc`, `/boot`, `/dev`, or `/usr` unless you're fully aware of the consequences.
- The logs and device files explored are part of standard Linux practice and are safe to observe, but not to tamper with.

License:
--------
This is a personal educational project. You’re welcome to fork, learn, and contribute your own Linux exploration notes.

