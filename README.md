[![CI](https://github.com/ayr-ton/ansible-devstation/actions/workflows/ci.yml/badge.svg)](https://github.com/ayr-ton/ansible-devstation/actions/workflows/ci.yml)
Ansible Devstation Collection
==============================

[Ansible Galaxy Collection: Devstation](https://galaxy.ansible.com/ayr_ton/devstation):

- common: 
- dotfiles: download and link dotfiles from git repo

Tested on:
----------

- Ubuntu 20.04 LTS

Example
-------

### Install the role:

```bash
ansible-galaxy collection install ayr_ton.devstation
```

### playbook.yml example

```yaml
- name: setup a devstation environment
  hosts: all
  connection: local
  become: yes
  gather_facts: yes
  roles:
    - role: ayr_ton.devstation.dotfiles
```

### Running a single role:

```
ansible localhost -m include_role -a 'name=ayr_ton.devstation.dotfiles'
```

# References:

- [Ansible Workstation Collection](https://galaxy.ansible.com/crivetimihai/workstation)
- [Ansible Virtualization Collection](https://galaxy.ansible.com/crivetimihai/virtualization)
