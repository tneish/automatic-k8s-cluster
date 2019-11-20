# automatic-k8s-cluster
Provision a K8s cluster automatically using Vagrant and Ansible. 
Based on https://kubernetes.io/blog/2019/03/15/kubernetes-setup-using-ansible-and-vagrant/ by Naresh L J (Infosys).

Vagrant provisions each VM using a pre-built image for the VirtualBox hypervisor; starts the VM; then calls Ansible to run a playbook inside each VM to install required software (Docker, K8s, Calico) and initialize the K8s cluster (kubeadm).

The Ansible playbooks are not idempotent.

Successful with:
(Host) Ubuntu 16.04
Vagrant 2.2.6
VirtualBox 6.0.14r133895
Ansible 2.7.12.
Vagrant box "bento/ubuntu-16.04 (virtualbox, 201910.20.0)"
