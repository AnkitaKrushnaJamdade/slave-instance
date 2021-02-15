slave-instance
=========

This role will launch 2 slave instances and they're tagged as key = Name and value = k8s_slave_an

Requirements
------------

Before running this role you've run master-instance, master_conf roles. You need to install the boto library, ansible version 2.9.15 or 2.9.

Role Variables
--------------

There are aws_access_key and aws_secret_key variables. There value should be IAM User's credentials. IAM User should have the policy to launch the ec2 instances.

Dependencies
------------

The roles required are:
master-instance
master_conf

Example Playbook
----------------

    - hosts: localhost
      roles:
         - slave-instance
