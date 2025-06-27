# What is Ansible?
Ansible is an open-source automation engine that automates software provisioning, configuration management, and application deployment.
It's designed to be simple, agentless, and highly efficient. Unlike many other automation tools, Ansible doesn't require any special agents or software to be installed on the machines it manages (known as "managed nodes"). Instead, it communicates over standard SSH for Linux/Unix machines and WinRM for Windows machines.

Ansible uses a declarative language, meaning you describe the desired state of your systems, and Ansible figures out how to get there. This desired state is defined in human-readable YAML (YAML Ain't Markup Language) files called playbooks. These playbooks are a collection of "plays," and each play defines a set of "tasks" to be executed on specific groups of machines.

## Key components of Ansible include:

Control Node: The machine where Ansible is installed and from where playbooks are executed.

Managed Nodes: The target servers or devices that Ansible automates.

Inventory: A file (usually inventory.ini or hosts) that lists the managed nodes, often organized into groups.

Modules: Small programs that Ansible pushes out to managed nodes to perform specific tasks (e.g., installing packages, managing services, copying files). Ansible has a vast library of modules.

Playbooks: YAML files that contain the step-by-step instructions (tasks) for automation.

Roles: A way to organize playbooks and other Ansible content into reusable, shareable, and well-structured units.

