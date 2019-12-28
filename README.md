Role Name
=========

hashicorp

[![Build Status](https://travis-ci.org/cmihai-ansible/hashicorp.svg?branch=master)](https://travis-ci.org/cmihai-ansible/hashicorp)

Ansible galaxy:
---------------

[https://galaxy.ansible.com/crivetimihai/hashicorp](https://galaxy.ansible.com/crivetimihai/hashicorp)

```bash
ansible-galaxy install crivetimihai.hashicorp
```

Requirements
------------

- For RHEL, a Red Hat subscription or functional local repository.

Role Variables
--------------

```
hashicorp_remove_packages: true
hashicorp_enable_service: true
hashicorp_enable_selinux: true
hashicorp_firewall_configure: true
hashicorp_firewall_rules:
  - service:
```

Dependencies
------------

- For Red Hat, subscription-manager.

Example Playbook
----------------

```yaml
---
- name: Install hashicorp on localhost
  hosts:
    - localhost
  connection: local

  tasks:
    - name: hashicorp is configured
      import_role:
        name: crivetimihai.hashicorp
      vars:
        hashicorp_remove_packages: true
        hashicorp_enable_service: true
        hashicorp_firewall_configure: true
        hashicorp_firewall_rules:
          - service:
      tags: hashicorp
```

License
-------

MIT

Author Information
------------------

- [Mihai Criveti](https://www.linkedin.com/in/crivetimihai/)
