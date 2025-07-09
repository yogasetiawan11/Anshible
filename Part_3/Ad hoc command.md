In ansible there are 2 ways of providing instruction,
- First way using Playbook (Yaml)
- Second way using Adhoc command

You can simply understand them as running some instruction on AWS 
**When to use Adhoc command**
Using Adhoc command if you have a simple Task such as:
Install ``Apache server``, ``Creating files on the target server``, ``Restarting server``, `` Install nodejs`` Or anything simple task.

**Simple Example** 
```bash
ansible inventory.ini -m shell -a "apt update" all
```

``ansible:`` Runs an ad hoc Ansible command.
``inventory.ini:`` Specifies the inventory file containing the list of target hosts.
``-m "shell":`` Uses the shell module to run shell commands on the target hosts.
``-a "apt update":`` The argument to the module; runs the apt update command (updates package lists on Debian/Ubuntu systems).
``all:`` Runs the command on all hosts listed in the inventory. you can also use one host/group within ``.ini`` file.


- Link to learn more about ad hoc command:
https://docs.ansible.com/ansible/latest/command_guide/intro_adhoc.html
