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

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).
