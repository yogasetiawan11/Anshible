## Example of using loops in Ansible playbook
```bash
---
-  name: 'Print list of fruits'
   hosts: localhost
   vars:
     fruits:
       - Apple
       - Banana
       - Grapes
       - Orange
   tasks:
     - command: 'echo "{{ item }}"'
       with_items: '{{ fruits }}'    # here loops are used
```


## Output:
```bash
PLAY [Print list of fruits] ****************************************************

TASK [Gathering Facts] *********************************************************
ok: [localhost]

TASK [command] *****************************************************************
changed: [localhost] => (item=Apple)
changed: [localhost] => (item=Banana)
changed: [localhost] => (item=Grapes)
changed: [localhost] => (item=Orange)
PLAY RECAP ********************************************************************* 
```