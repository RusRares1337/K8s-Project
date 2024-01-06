# Create infrastructure with Terraform for K8s cluster and configure Master-Node and Worker-Nodes

1. Move pem file to ~/.ssh, give permissions 400 and connect. (or from IaC select to use the public key from your localhost like in this terraform main.tf)
```shell
mv ~/Downloads/key.pem ~/.ssh
chmod 400 ~/.ssh/key.pem
ssh -i ~/.ssh/key.pem user@ip
```
2. Setup and configure Master Node
```shell

```

3.