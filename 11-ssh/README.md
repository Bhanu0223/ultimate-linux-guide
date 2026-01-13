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




