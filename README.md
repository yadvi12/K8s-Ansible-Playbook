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
- Cd to the location of cloned repository.
- Export the aws key and value pair using
 
 ```sh
 EXPORT AWS_ACCESS_KEY_ID="7***********9A"
 EXPORT AWS_SECRET_ACCESS_KEY="9***************7S"
 EXPORT AWS_REGION="ap-south-1"
 ```
 
 - Run the playbook using "ansible-playbook setup.yml" command.

## Verification:

The playbook will download /etc/kubernetes/admin.conf file to $HOME/admin.conf.
- Login to the master node.
- Verify cluster is fully running using kubectl:

```sh
kubectl get nodes
kubectl get pods
kubectl get pods -n kube-system"
```
