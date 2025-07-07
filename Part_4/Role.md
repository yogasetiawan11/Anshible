## What is Role in ansible
An Ansible role is a reusable, self-contained unit of automation that is used to organize and manage tasks, variables, files, templates, and handlers in a structured way.

Roles help to modularize the logic and configuration needed to manage a particular system or application component.

This modular approach promotes reusability, maintainability, and consistency across different playbooks and environments.

to make a role you can take individual part in Yaml file and put them each and every folder. Ansible can create that folder structure using command 
```bash
ansible galaxy role init "new_folder"
`` 

## Why use ansible roles
With Ansible roles, we can organize tasks, variables, files, and templates into separate folders instead of putting everything into a single YAML file. If you have hundreds or thousands of tasks in one file, it becomes difficult to manage and understand. By using roles, you make your playbooks easier to read, maintain,

## Advantage Role in ansible
### Modularity
roles allow you to seperate complex playbook into smaller and reusable component.

### Readability
role make your file cleaner and easier to read

### Reusability
Once created, roles can be reused across different playbooks and projects. This saves time and effort in writing redundant code.


### Collaboration
Roles facilitate collaboration among team members by allowing them to work on different parts of the infrastructure independently.

