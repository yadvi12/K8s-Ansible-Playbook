K8s-Worker Role
=========

A Kubernetes cluster consists of a set of worker machines, called nodes, that run containerized applications. Every cluster has at least one worker node.
This role is created to configure Kubernetes Worker on top of AWS RHEL8 Instance.

Requirements
------------
- Deployment environment must have Ansible 2.9.0+
- Master and nodes must have passwordless SSH access
- Boto3 

About Worker Node
------------
- The worker node(s) host the Pods that are the components of the application workload. 
- The control plane manages the worker nodes and the Pods in the cluster.
- The node components run on every cluster node. These include:
container runtime: such as Docker, to execute containers on the node.
kubelet: executes containers (pods) on the node as dictated by the control plane’s scheduling, and ensures the
health of those pods (for example, by restarting failed pods).
kube-proxy: a network proxy/loadbalancer that implements the Service abstraction. It programs the iptables rules on
the node to redirect service IP requests to one of its registered backend pods.

Example Playbook
----------------

To use this role in your own playbook, refer the following example:

    - hosts: tag_Name_K8s_Worker
      roles: 
     - role: "K8s-worker"

License
-------

The Project is released under the terms of the MIT License.


Author Information
------------------

If you have any queries regarding the project, you can join and ask queries in our [discord server]().
