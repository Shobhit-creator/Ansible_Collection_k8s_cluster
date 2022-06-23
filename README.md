# Ansible_Collection_k8s_cluster

## Description
Ansible Collection for configuring Kubernetes cluster on aws on t2.micro 

## Roles
### ec2
* This Role launch ec2 instances on aws with 1 master and 3 slave by using instance type t2.micro
* you need to run this role using hosts: localhost

### k8s_master
* This Role configure the master node of k8s
* For running this Role make sure your dynamic inventory configured

### k8s_slave 
* This Role configure slave node for k8s on aws, by default its three but can change using vars.
* For running this Role make sure your dynamic inventory configured

## Use This Role
* Download this `ansible-galaxy collection install collection_name
* Playbook Example for running this Role
		
		- hosts: Hosts
		  collections:
		    - namespace.collection_name
		  roles:
		    - role: role_name


## Tested OS
* Amazon AMI 2
* RHEL8
