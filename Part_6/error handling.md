## What is Error handling
In Ansible, error handling refers to the mechanisms that control how a playbook reacts when a task fails. By default, Ansible follows a "fail-fast" approach: if a task fails on a host, the execution of the playbook is halted for that specific host, and Ansible moves on to the next host in the inventory. 

### Why use Error handling?
As a DevOps you may given a task configuration management activity on all manage nodes that are associated with control node. Let's say the task is install docker but the first step they want to:
1. make sure the open ssh and open ssl exist with the latest version for security purpose
2. verify the docker has installed
3. Install docker if second task is doesn't exist

imagine out of these VM (manage nodes) doesn't have task number 1 open ssh and ssl on any manage node. all of the script will fail this become problem

`with error handling` if this packages doesn't exist on vm you can skip to another task.