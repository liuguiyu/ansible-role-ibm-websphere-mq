IBM Websphere MQ
=====================

Forked from https://github.com/mm0/ansible-role-ibm-websphere-mq

Author Information
[Matt Margolin](mailto:matt.margolin@gmail.com)

Updated for MQ 9 RDQM


An Ansible role that installs IBM Websphere MQ on RHEL/Centos using locally provided installation package and License

Requirements
---------------

- Sudo access
- Locally (on target host) install package available and License 


Role Variables
---------------

*General variables*

| Name              | Default Value       | Description          |
|-------------------|---------------------|----------------------|
| `environment_name` | `Dev1` | Self Explanatory |
| `webspheremq.group` | `"mqm"` | App Group |
| `webspheremq.user ` | `"mqm"` | App User |
| `webspheremq.archive_dir` | `"/mnt/nfs/ansible/websphere-mq/"` | Directory where installer archive lives|
| `webspheremq.unarchive_dir` | `"/opt/temporary/{{ environment_name }}"` | Directory where zip installer lives|
| `webspheremq_internal.install_archive_path` | `"{{ webspheremq.archive_dir }}/MQ_7.5.0.2_TRIAL_LNX_ON_X86_64_ML.tar.gz"` | Full path to archive |


Dependencies
---------------

None 

Example Playbook
---------------
```yaml
- hosts: webservers
  vars:
  - environment_name: Dev1 
  roles:
  - ansible-role-ibm-websphere-mq 
```

License
---------------

BSD-2


