# CMPE 272 - HW1 - Ansible

## Overview

This project deploys and undeploys NGNIX servers on two Ubuntu virtual machines VM1 and VM2 using Ansible.
There is one script to deploy it and another to undeploy it. Each webserver listens on port 8080 and displays a unique message.

| VM | IP Address | URL | Message |
|-----|---------------|---------------------------|-------------------------|
| VM1 | 192.168.252.4 | http://192.168.252.4:8080 | Hello World from SJSU-1 |
| VM2 | 192.168.252.3 | http://192.168.252.3:8080 | Hello World from SJSU-2 |


## Requirements :
- Ansible
- Two VMs 
- SSH connectivity to both VMs

## How to run :

Start the two VMs. Make sure they are running. 

To check if the two VMs are pingable, run :

```bash
ansible webservers -i inventory.ini -m ping
```

To run deploy script :

```bash
ansible-playbook -i inventory.ini deploy.yml
```

To run undeploy script :

```bash
ansible-playbook -i inventory.ini undeploy.yml
```
