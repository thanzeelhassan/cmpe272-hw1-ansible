CMPE 272 
HW1 - Ansible

To check if the two VMs are pingable, run :

ansible webservers -i inventory.ini -m ping

To run deploy script :

ansible-playbook -i inventory.ini deploy.yml

To run undeploy script :

ansible-playbook -i inventory.ini undeploy.yml

