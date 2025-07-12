## What is Ansible vault
Ansible vault is used to secure any sensitive information whithin your Ansible playbooks or roles. it can be the password, API token, or some file that you whan encrypted

## Why you need to secure content in Ansible playbook 
assume you're a DevOps engineer within Playbooks you create EC2 instance or other resources
then within this Playbook you have to provide `aws secret key` or `access key`afterwards you want to share this Playbook with other in organization through git then the sensitive information become public and this is how you need to secure your sensitive information

## How?
to secure sensitive information you don't need to install any tools instead you can simply run command ``ansible-vault`` in control node the you will see positional arguments:
  {create,decrypt,edit,view,encrypt,encrypt_string,rekey}
    create              Create new vault encrypted file
    decrypt             Decrypt vault encrypted file
    edit                Edit vault encrypted file
    view                View vault encrypted file
    encrypt             Encrypt YAML file
    encrypt_string      Encrypt a string
    rekey               Re-key a vault encrypted file
