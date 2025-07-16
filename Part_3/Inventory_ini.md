## What is Inventory 
typically ``Inventory`` is a file which used By Control Node to understand and manage the manage node in ansible. you can write ``Inventory`` in ``Yaml`` or ``.ini``file

You can put this ``.ini`` anywhere but it's recommended to place in folder ``etc/Ansible/host`` 

It contains a list of IP addresses or hostnames (managed nodes) that you want to control.
You can directly specify the VM or instance name within the inventory file.


## Example inside .ini file
```bash
ubuntu@192.168.1.10
ubuntu@192.168.1.11

```

or you can make a groups based on your server:

```bash
[App servers]
192.168.1.10
192.168.1.11

[DB servers]
192.168.1.20

```
