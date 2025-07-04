## What is a YAML Playbook?
Ansible Playbook is basically is a Yaml file. to present Ansible Playbook you can present tripple hyphen  ``---``  at the first and inside the Playbook you can have a number of Plays. (a play is a section of a playbook that defines a set of tasks to be executed on a group of hosts.)

### Example
```bash
---                   # 3 hyphen
name: Yoga            # String
age: 22               # Number
working: true         # Boolean
tasks:                # List
  - writing
  - reading
  - learning
activity:             # Dictionary
    swimming:
    exercise:
    eating:

#the only different between List and Dictionary there's in hyphen
```

you can make sure your yaml code is correct in web ``YAML Lint``