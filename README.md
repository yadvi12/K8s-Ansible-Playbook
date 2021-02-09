# Kubernetes Ansible Playbook
Build a Kubernetes cluster using Ansible with kubeadm. The goal is to easily install a Kubernetes cluster on machines running RHEL8 and centos on top of AWS public cloud.

System requirements:

- Deployment environment must have Ansible 2.9.0+
- Master and nodes must have passwordless SSH access

## Usage:

- Install ansible 2.9.0+ in your system.
- Clone this repository in any location you want.
- Create a folder "/etc/ansible" in your system.
- Copy the "ansible.cfg" file in /etc/ansible location.
- Open the ansible.cfg file and change the required parameters.

