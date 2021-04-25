# Overview
This role will define ansible custom facts on the target system based on host variables.

The facts can then be used in other roles or plays.

# Ansible host-info fact file format

    [general]
    infrastructure=onpremise
    hostgroup=linux
    subgroup=redhat-idm
    role=master
    environment=testing
    instance=1

# Variables

| Name  | Type | Required | Default Value | Description |
| ----- | ---- | -------- | ------------- | ----------- |
| host_info_infrastructure | string | no | 'none' | The infrastructure this host is deployed on |
| host_info_environment | string | yes | 'none' | Can be development,testing,staging,production |
| host_info_hostgroup | string | yes | 'none' | Group the hosts belong too |
| host_info_subgroup | string | no | 'none' | More specific group thee host belongs to |
| host_info_role | string | no | 'none' | The role of this host |
| host_info_instance | string | no | 'none' | The instance of this host, can be an index |

# Automatique Testing

This role is tested using Molecule against:
- Python 3.7 and 3.8
- CentOS 7/8
- Debian 9/10

# Facts
> Minimal facts are used in this role. This allows to get the Red Hat release number.