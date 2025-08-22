# Ansible Keepalived
Script for installing and configuring keepalived in Ansible

## Explain
```yaml
---
- name: Install Keepalived
  hosts: primary_serwer, secondary_serwer 
  become: yes
  vars:
    virtual_ip: "192.168.0.10"
    virtual_router_id: 50
    interface: "<<ETERNET INTERFACE>>"
    master_host: "primary_serwer"

  tasks:
    - name: Run install_keepalived.yml
      include_tasks: ./task/ansible_keepalived/playbook.yml
```