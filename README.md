# ansible_for_windows

## Variables
`password_in_vault` is variable located in `vault.yaml` but you need first put your pass here.
Then run command `ansible-vault encrypt vault.yaml` and type new pass for vault file

## How to use

First of all you need to run this playbook `csr-cert-add.yaml` which create cert and key on localhost and add it to Windows machines in `all` group in your inventory (edit if necessary)  

Second - you can run this playbook `win_nginx.yaml` which use role `win_nginx` which install nginx for Windows and configure firewall for 80 and 443 ports

You can fix some variables if necessary for `win_nginx` role in `default` directory 
