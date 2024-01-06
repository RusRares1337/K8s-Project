# Create infrastructure with Terraform for K8s self-managed cluster (1 Master, 2 Nodes)

1. Move pem file to ~/.ssh, give permissions 400 and connect. (or from IaC select to use the public key from your localhost like in this terraform main.tf)
```shell
mv ~/Downloads/key.pem ~/.ssh
chmod 400 ~/.ssh/key.pem
ssh -i ~/.ssh/key.pem user@ip 
```
## Configure Ansible on Master and Worker Nodes
1. Configure hosts inventory file

2. On localhost where Ansible runs:
From our localhost connect to target server, add target infos in known_hosts in our server with:
```shell
ssh-keyscan -H <ip> >> ~/.ssh/known_hosts
```
To allow target server to communicate with host server, target server has to have in ~/.ssh/authorized_keys the localhosts public ssh (~/.ssh/id_rsa.pub)
```shell
ssh-copy-id root@<ip> 
```
3.