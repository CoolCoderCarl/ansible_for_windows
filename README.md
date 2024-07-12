# ansible_for_windows

## Prerequisites

First of all you need to install collections for windows using Ansible Galaxy as folows:
- `ansible-galaxy collection install chocolatey.chocolatey`
- `ansible-galaxy collection install community.windows`

After this you need to check is there is WinRM turn on on the inventory hosts


## Vault
The `password_in_vault` is variable located in `vault.yaml` but you need first put your pass here  
Then run command `ansible-vault encrypt vault.yaml` and type new pass for vault file

## How to use

Playbook `deploy-nginx-and-certs.yaml` is divided by three big steps
- Create certs
- Deploy certs
- Deploy nginx using role `win_nginx`

To run type `ansible-playbook deploy-nginx-and-certs.yaml` 
