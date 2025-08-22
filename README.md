# Ansible Keepalived

## Explain
```yaml
---
- name: Install Keepalived
  hosts: prymary_serwer, secondary_serwer 
  become: yes
  vars:
    virtual_ip: "192.168.0.10"
    virtual_router_id: 50
    interface: "<<ETERNET INTERFACE>>"
    master_host: "prymary_serwer"

  tasks:
    - name: Run install_keepalived.yml
      include_tasks: ./task/ansible_keepalived/playbook.yml
```