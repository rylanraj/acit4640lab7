# acit4640lab7
## Creating SSH Keys

If you do not already have an SSH key pair, you can create one using the following command:

```bash
ssh-keygen -t ed25519 -b 4096 -f "keyname" -C "comments"
```

**Explanation:**
- `-t rsa`: Specifies the type of key to create
- `-b 4096`: Sets the key length to 4096 bits.
- `-f "keyname"`: Name of file or path of the key
- `-C "rylan.raj@gmail.com"`: Adds a comment to the key for identification.
  
Set a passphrase if desired when prompted



## Running the Playbook

Once your SSH keys are set up and the managed nodes are accessible, run the playbook using the following command:

```bash
ansible-playbook -i inventory/hosts.yml --private-key=~/.ssh/aws playbook.yml
```

**Explanation:**
- `ansible-playbook`: The command to run Ansible playbooks.
- `-i inventory/hosts.yml`: Specifies the inventory file that contains your managed nodes.
- `playbook.yml`: The playbook file that contains the tasks for configuring your web servers.

## Additional Notes

- Ensure that the files referenced in the playbook, such as `files/nginx.conf` and `templates/index.html.j2`, exist in the appropriate directories relative to your playbook.
![image](https://github.com/user-attachments/assets/2d6c4f32-4e05-48c6-a1be-4977c52048cd)




