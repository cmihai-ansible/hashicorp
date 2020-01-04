Role Name
=========

hashicorp: installs OS packages (ex: vagrant RPM / deb).

For binary / archive installer - see localbin role.

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
hashicorp_vagrant_version: "2.2.6"
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
        hashicorp_vagrant_version: "2.2.6"
      tags: hashicorp
```

License
-------

MIT

Author Information
------------------

- [Mihai Criveti](https://www.linkedin.com/in/crivetimihai/)
