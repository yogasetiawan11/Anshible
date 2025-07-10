## What is Ansible Galaxy
basically Ansible is like a market place for Ansible roles In Ansible Galaxy there are many ,Module, Task, Role that are written by different Devops engineer that you can use instead of write from scratch. 
Example if you have a task to install docker in your *Control Node* and you maybe have different os Instead of writting Playbook or Role one by one You can simply go to Ansible Galaxy and search for the code that suits with your need.

**Example command galaxy to install Docker**
```bash
anshible-galaxy role intall bsmeding.docker
```
then we can look the file inside ``ls ~/.ansible/roles`` this directory is hidden file ``.ansible`` inside this folder there's roles that we've already downloaded

To execute the docker file follow all these steps:
create directory ``Playbook.Yaml`` which contain yaml 
```bash
---
host: All
become: true 
roles:
  - bsmeding.docker     
  # Name docker file that we downloaded
```

save then run the command
``ansible-playbook -i inventory.ini Playbook.Yaml``
-Playbook.Yaml is a Directory which contain Yml above
-Inventory.ini contain all manage nodes