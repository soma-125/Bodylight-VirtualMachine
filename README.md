# Virtual machine for Bodylight.js

This is vagrant script to prepare devel VM from scratch

## Requirements

Requirement: 
- HW: 1 CPU, 2 GB RAM, 5-50GB disk space.
- OS: Any OS supported by VirtualBox and Vagrant tool (tested on Windows 7,Windows 10, Ubuntu 16.04)
- SW: Install [VirtualBox](https://www.virtualbox.org/wiki/Downloads) and [Vagrant](https://www.vagrantup.com/downloads.html) tested version 2.1.1. Some OS has their own distribution of vagrant and virtualbox: `yum install vagrant virtualbox` OR `apt install vagrant virtualbox`.

## Local Installation Using Vagrant and Virtualbox

Type in your command line:

```bash
git clone https://github.com/creative-connections/Bodylight-VirtualMachine.git
cd Bodylight-VirtualMachine
vagrant up
```
### After installation
After several minutes the VM is installed and configured. 
Port forwarding is done from guest VM 80 to host 8080 by default, refer Vagrantfile for exact port number. Refer default page at http://localhost:8080
Refer Jupyter notebook at http://localhost:8080/jupyter/