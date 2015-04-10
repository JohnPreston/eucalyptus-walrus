eucalyptus-sc
=========

Installs Eucalyptus SC and configures the eucalyptus.conf file

Requirements
------------

CentOS 6/ RHEL 6

Role Variables
--------------

| Parameter | Required | Default | Description
|--- |--- |--- |---
| euca_repo_url | Yes | Latest RPM URL | URL to the wanted eucalyptus rpm
| euca2ools_repo_url | Yes | Latest RPM URL | URL to the wanted euca2ools rpm
| epel_repo_url | Yes | Latest RPM URL | URL to the latest EPEL rpm
| elrepo_repo_url | Yes | Latest RPM URL | URL tp the latest elRepo rpm
| euca_local_repo_url | No | None | URL to a local Eucalyptus Repo
| euca_repo_file | Yes | /etc/yum.repos.d/eucalyptus.repo | Path to the repo file
| euca2ools_local_repo_url | No | None | URL to a local euca2ools repo
| euca2ools_repo_file | Yes | /etc/yum.repos.d/euca2ools.repo | Path to the repo file
| euca_use_local_repo| No | False | Use local repos URL or not
| euca_images | Yes | eucalyptus-service-image | List of the eucalyptus images packages
| euca_conf_file_path | Yes | /etc/eucalyptus/eucalyptus.conf | Path to the root eucalyptus.conf file
| clc_public_key_path | Yes | /var/tmp/clc-pub-key | Path on the Ansible machine where the CLC public key is
| ssh_key_bits | Yes | 4096 | Number of bits for the CLC private Key


Dependencies
------------


Example Playbook
----------------

- hosts: sc
  roles:
  - eucalyptus-sc
  vars:
  java_iface: eth1

License
-------

GPLv3

Author Information
------------------

John Preston [John Mille]
