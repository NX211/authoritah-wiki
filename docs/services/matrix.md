# Matrix

## Repository Setup

git clone https://github.com/spantaleev/matrix-docker-ansible-deploy.git

add line host file to inventory > hosts

```bash
[matrix_servers]
authoritah.chat ansible_host=matrix_server_ip_address ansible_ssh_user=root
```

add host variables to inventory > host_vars > authoritah.chat > vars.yaml

run `just roles` to install Ansible Galaxy Roles

run `sudo ansible-playbook -i inventory/hosts setup.yml --private-key ~/.ssh/id_matrix --tags=setup-all` to update Matrix Server
