# 🐧 Phase 0 — Linux Basics Review (Ubuntu 22.04)

This document summarizes the essential Linux administration tasks required to manage Kubernetes nodes and troubleshoot cluster issues confidently.

---

## 🧭 System Information
| Command | Description 
|----------|--------------
| `lsb_release -a` | Displays Ubuntu version info 
| `uname -r` | Shows kernel version 
| `df -h` | Checks disk usage 
| `free -h` | Shows memory usage 

---

## 🌐 Networking
| Command | Description 
|----------|--------------|----------------|
| `ip a` | Lists network interfaces 
| `ip route` | Shows routing table 
| `ping -c3 8.8.8.8` | Tests connectivity 
| `curl -I https://kubernetes.io` | Checks HTTP connectivity 

---

## 👥 Users & Permissions

sudo adduser devops
sudo usermod -aG sudo devops
sudo su - devops
id devops


⚙️ Package & Service Management
sudo apt update && sudo apt upgrade -y
sudo systemctl status kubelet
sudo systemctl status containerd
sudo systemctl restart containerd

🧾 Logs & Monitoring
sudo journalctl -u kubelet -f
sudo dmesg | tail
sudo journalctl -n 50 --no-pager
top

✅ Summary

This Linux review validates readiness to manage Kubernetes environments.
All commands tested successfully in KodeKloud Pro Ubuntu 22.04 controlplane node.
