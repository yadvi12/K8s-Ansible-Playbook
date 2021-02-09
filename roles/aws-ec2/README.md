AWS-EC2 ROLE
=========

This role is created to launch the instances in the AWS public cloud and then dynamically retrieving the IPs of the instances and updating the inventory file of the ansible.

Requirements
------------

Boto3 module should be installed in your system. If it's not installed, use `pip3 install boto3` to install it.

Role Variables
--------------
Navigate to vars/main.yml file and provide the value of the variables.

| Variables | Description |
| --- | --- |
| `key` | provide the AWS key in pem format |
| `instanceType` | Provide the instance type |
| `image_id` | ami ID to use for the instance |
| `region_name` | The AWS region to use |
| `security_grp_id` | Security group id (or list of ids) to use with the instance |
| `subnet_id` | The subnet ID in which to launch the instance (VPC) |
| `access_key` | AWS access key |
| `secret_key` | AWS secret key |


Example Playbook
----------------
To use this role in your own playbook, refer the following example:

    - hosts: localhost
      roles: 
     - role: "aws-ec2"
License
-------

The Project is released under the terms of the MIT License.

Author Information
------------------

If you have any queries regarding the project, you can join and ask queries in our [discord server]().
