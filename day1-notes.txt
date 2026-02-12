# Core Linux Basics – Summary

## 📁 Filesystem Understanding
- Linux uses a **tree-like directory structure** starting at `/` (root).
- Everything is treated as a file (files, directories, devices, processes).
- Common filesystems: **ext4, XFS, Btrfs**.
- Key directories:
  - `/home` → user files  
  - `/etc` → configuration files  
  - `/var` → logs and variable data  
  - `/bin` → essential binaries  
  - `/tmp` → temporary files  

---

## 🔐 `chmod` Meaning (Permissions)
`chmod` changes file permissions.

Permissions:
- `r = read (4)`
- `w = write (2)`
- `x = execute (1)`

They apply to:
- **User (owner)**
- **Group**
- **Others**

Example:
`chmod 755 file.txt`

Means:
- Owner: read + write + execute  
- Group: read + execute  
- Others: read + execute  

---

## 👤 User & Group Basics
- Every file has:
  - an **owner**
  - a **group**
- Users can belong to:
  - 1 primary group  
  - multiple secondary groups  
- Access depends on file permissions + user/group membership.

Key commands:

`whoami`
`id`
`groups`

---

## 📊 Monitoring Commands
| Command | Purpose |
|--------|---------|
| `top` | Live process and CPU view |
| `htop` | Improved version of top |
| `ps aux` | Snapshot of processes |
| `free -h` | Memory usage |
| `df -h` | Disk usage |
| `uptime` | System load |
| `dmesg` | Kernel logs |
