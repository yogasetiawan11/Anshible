## What is passwordless & ssh authentication
Passwordless authentication is a method of logging in to a system without asking for a password. In the context of SSH (Secure Shell), this usually means using SSH key-based authentication.

## How to set up Passwordless Authentication

### Using Public key with EC2

Enter the command on Control node
```bash
ssh-copy-id -f "-o IdentityFile <PATH TO PEM FILE>" ubuntu@<INSTANCE-PUBLIC-IP>
```

``ssh-copy-id:`` A tool to install your public key on a remote server for SSH key-based (passwordless) authentication.
``-f:`` Forces the copying of the key, even if it already exists on the remote server.
``-o IdentityFile <PATH TO PEM FILE>:`` Tells SSH to use the private key file at <PATH TO PEM FILE> (commonly a .pem file from AWS EC2) for authentication.
``ubuntu@<INSTANCE-PUBLIC-IP>:`` Connects as the ubuntu user to the server at <INSTANCE-PUBLIC-IP>.

### Using password
- Go to the file ``vim /etc/ssh/sshd_config.d/60-cloudimg-settings.conf``  
this folder is a configuration file for the SSH server (sshd) on Linux systems, especially cloud images (like Ubuntu on AWS, Azure, or GCP).

- then change ``PasswordAuthentication yes``

- afterwards restart SSH using ``sudo systemctl restart ssh``