# set up password-less SSH from user
  Generate SSH key:
```bash
ssh-keygen -t rsa -b 2048
```

# This creates: ~/.ssh/id_rsa, ~/.ssh/id_rsa.pub
  Copy the public key to App Servers:
  ```bash
  ssh-copy-id tony@app_server_1
  ```
  Enter tony’s password when prompted.

# above two steps into single command
```bash
ssh-keygen -t rsa -b 2048 -N "" -f ~/.ssh/id_rsa
```
# Check permissions
```bash
chmod 700 ~/.ssh
chmod 600 ~/.ssh/id_rsa
chmod 644 ~/.ssh/id_rsa.pub
```


# Inventory file example with password
```ini
stapp01 ansible_host=172.16.238.10 ansible_ssh_pass=Ir0nM@n
stapp02 ansible_host=172.16.238.11 ansible_ssh_pass=Am3ric@
stapp03 ansible_host=172.16.238.12 ansible_ssh_pass=BigGr33n
```


