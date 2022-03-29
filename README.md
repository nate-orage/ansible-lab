# ansible-lab

This repo is an ongoing lab meant to display different automated LAN deployments. The Vagrantfile will prompt Virtualbox to spawn one or many Ubuntu (ub) and Fedora (fed) servers. After the VMs are created, ansible playbooks are used to manage the servers. I have 1 other LAN server and 1 cloud server that I manage as well. I won't include those below. Other configuration files will be added over time.

## Default Provision

- Hosts:
  - ub1: 192.168.1.206
    - Ubuntu 20.04. Provisioned with cockpit server dashboard and fail2ban.
  - fed1: 192.168.1.207
    - Fedora Cloud Edition
- Services
  - Vagrant: VM provisioning 
  - VirtualBox: VM creation
  - Ansible: Automation