## Introduction

This project provides a streamlined approach to setting up and managing AWS infrastructure using Ansible. By leveraging these roles, you can quickly create and manage Virtual Private Clouds (VPCs), subnets, security groups, and Ubuntu VMs with additional storage.

## Note

* Before starting the project, ensure you add your SSH public key path (ssh_pub_key_path) in the Ansible configuration variable file called all.yml


## * Creating VPC, Linux ubuntu vm with a secondary data disk and configuring it run :

```
ansible-playbook -i demo.aws_ec2.yml --private-key lu3  gate.yml -e "@all.yml" 

```
## * Stopping the Linux ubuntu vm 

```
ansible-playbook -i demo.aws_ec2.yml --private-key lu3  stop-linux-vm-aws.yml -e "@all.yml"

```

## * Starting the Linux ubuntu vm 

```
ansible-playbook -i demo.aws_ec2.yml --private-key lu3  start-linux-vm-aws.yml -e "@all.yml"

```


## * Re-starting the Linux ubuntu vm 

```
ansible-playbook -i demo.aws_ec2.yml --private-key lu3  re-start-linux-vm-aws.yml -e "@all.yml"

```

## * Delete the Linux ubuntu vm  with the secondary data disk

```
ansible-playbook -i demo.aws_ec2.yml  delete-linux-vm-aws.yml -e "@all.yml"

```


