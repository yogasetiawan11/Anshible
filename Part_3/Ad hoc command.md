In ansible there are 2 ways of providing instruction,
- First way using Playbook (Yaml)
- Second way using Adhoc command

You can simply understand them as running some instruction on AWS 
**When to use Adhoc command**
Using Adhoc command if you have a simple Task such as:
Install ``Apache server``, ``Creating files on the target server``, ``Restarting server``, `` Install nodejs`` Or anything simple task.

**Simple Example** 
```bash
ansible -i name_your_inventory all -m "shell" -a "touch yoga setiawan"
```

- ``ansible:`` Runs an ad hoc Ansible command.
- ``-i name_inventory:`` Specifies the inventory file containing the list of target hosts or IP addresses.
- ``-m "shell":`` module Uses the shell module to run shell commands on the target hosts.
- ``-a "touch":`` The argument to the module; runs the touch command (make a new file).
- ``all:`` Runs the command on all hosts listed in the inventory. you can also use one host/group within ``.ini`` if you have 1 host only you can change with the name IP address but if have 100 IP you can make a group inside the ``.ini`` file.


#### Example In Aws #### 
``` ansible -i Devops all -m "amazon.aws.s3_bucket_info" -a "region=us-east-1" ```
- Use the S3 bucket info module (-m "amazon.aws.s3_bucket_info")
- Query the us-east-1 region (-a "region=us-east-1")



- Link to learn more about ad hoc command:
https://docs.ansible.com/ansible/latest/command_guide/intro_adhoc.html
