mm0.ibm-integration-bus
==

[![Build Status](https://travis-ci.org/mm0/ansible-role-ibm-integration-bus.svg?branch=master)](https://travis-ci.org/mm0/ansible-role-ibm-integration-bus) [![Galaxy](https://img.shields.io/badge/galaxy-mm0.ibm--integration--bus-blue.svg?style=flat)](https://galaxy.ansible.com/mm0/ibm-integration-bus)

An Ansible role that installs IBM Websphere MQ on RHEL/Centos using locally provided installation package and License

Requirements
------------

- Sudo access
- Locally (on target host) install package available and License 

Role Variables
--------------

*General variables*

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `environment_name` | `Dev1` | Self Explanatory |
| `iib.unarchive_dir` | `"/IBM/{{ environment_name }}"` | Destination |
| `iib.install_sub_dir` | `"iib-10.0.0.7"` | Root Dir within archive |
| `iib.archive_dir` | `"/mnt/nfs/ansible/ibm-iib/"` | Directory where Install archive resides |
| `iib_install_archive_path` | `"{{ archive_dir }}/10.0.0.7-IIB-LINUX64-DEVELOPER.tar.gz"` | Directory where Install archive resides |
| `iib.user` | `"iibapp"` | App User |
| `iib.group` | `"iibapp"` | App Group |


Dependencies
------------

None

Example Playbook
----------------


```yaml
- hosts: webservers
  roles:
  - { role: mm0.ibm-integration-bus }
```

License
-------

BSD

Author Information
------------------

[Matt Margolin](mailto:matt.margolin@gmail.com)

[mm0](https://github.com/mm0) on github
