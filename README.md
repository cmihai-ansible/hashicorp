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

```yaml
hashicorp_base_url: "https://releases.hashicorp.com"
hashicorp_dir: "/usr/local/bin"
hashicorp_tools:
  - name: terraform
    version: "0.12.18"
    platform: linux_amd64
  - name: vault
    version: "1.3.0"
    platform: linux_amd64
  - name: consul
    version: "1.6.2"
    platform: linux_amd64
  - name: nomad
    version: "0.10.2"
    platform: linux_amd64
  - name: vagrant
    version: "2.2.6"
    platform: linux_amd64
  - name: packer
    version: "1.5.1"
    platform: linux_amd64
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
        hashicorp_base_url: "https://releases.hashicorp.com"
        hashicorp_dir: "/usr/local/bin"
        hashicorp_tools:
          - name: terraform
            version: "0.12.18"
            platform: linux_amd64
          - name: vault
            version: "1.3.0"
            platform: linux_amd64
          - name: consul
            version: "1.6.2"
            platform: linux_amd64
          - name: nomad
            version: "0.10.2"
            platform: linux_amd64
          - name: vagrant
            version: "2.2.6"
            platform: linux_amd64
          - name: packer
            version: "1.5.1"
            platform: linux_amd64
      tags: hashicorp
```

License
-------

MIT

Author Information
------------------

- [Mihai Criveti](https://www.linkedin.com/in/crivetimihai/)
