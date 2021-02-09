K8s-Master Role
=========

A master node is a node which controls and manages a set of worker nodes (workloads runtime) and resembles a cluster in Kubernetes.
This role is created to configure Kubernetes Master on top of AWS RHEL8 Instance.

Requirements
------------
- Deployment environment must have Ansible 2.9.0+
- Master and nodes must have passwordless SSH access
- Boto3 

About Master Node
------------

A master node has the following components to help manage worker nodes:

- Kube-APIServer, which acts as the frontend to the cluster. All external communication to the cluster is via the API-Server.
- Kube-Controller-Manager, which runs a set of controllers for the running cluster. The controller-manager implements governance across the cluster.
Etcd, the cluster state database.
- Kube Scheduler, which schedules activities to the worker nodes based on events occurring on the etcd. It also holds the nodes resources plan to determine the proper action for the triggered event. For example the scheduler would figure out which worker node will host a newly scheduled POD.

Example Playbook
----------------

To use this role in your own playbook, refer the following example:

    - hosts: tag_Name_K8s_Master
      roles: 
     - role: "K8s-master"

License
-------

The Project is released under the terms of the MIT License.


Author Information
------------------

If you have any queries regarding the project, you can join and ask queries in our [discord server]().
