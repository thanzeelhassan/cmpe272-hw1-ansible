CMPE 272 
HW1 - Ansible

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
