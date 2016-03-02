# Ansible role for zabbix-agent


This role will install zabbix agent 

## Tested On

  * Ubuntu 14.04

## Defaults

The `defaults/main.yml` should be pretty clear on the usage and values. The 
version used by defaults are:

  * `zabbix_version`: 2.2
  * `zabbix_update_cache_valid_time`: 3600
  * `zabbix_conf_server_ip`: 10.10.10.10

## Usage

The tests in the respository should be pretty straight forward, but here are
some examples:

### zabbix-agent

playbook.yml:

```
- name: Install and run zabbix-agent
  hosts: all
  sudo: True

  vars:
    zabbix_conf_server_ip: 10.10.10.10
  
  roles:
    - { role: ansible-zabbix-agent }

```

## TODO

  * Extract supervisor to it's own role
  * Extend to other distros

