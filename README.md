Role Name
=========

flatpak

[![Build Status](https://travis-ci.org/cmihai-ansible/flatpak.svg?branch=master)](https://travis-ci.org/cmihai-ansible/flatpak)

Ansible galaxy:
---------------

[https://galaxy.ansible.com/crivetimihai/flatpak](https://galaxy.ansible.com/crivetimihai/flatpak)

```bash
ansible-galaxy install crivetimihai.flatpak
```

Requirements
------------

- For RHEL, a Red Hat subscription or functional local repository.

Role Variables
--------------

```yaml
flatpak_remove_packages: true
flatpak_enable_service: true
flatpak_enable_selinux: true
flatpak_firewall_configure: true
flatpak_firewall_rules:
  - service:
```

Dependencies
------------

- For Red Hat, subscription-manager.

Example Playbook
----------------

```yaml
---
- name: Install flatpak on localhost
  hosts:
    - localhost
  connection: local

  tasks:
    - name: flatpak is configured
      import_role:
        name: crivetimihai.flatpak
      vars:
        flatpak_remove_packages: true
        flatpak_enable_service: true
        flatpak_firewall_configure: true
        flatpak_firewall_rules:
          - service:
      tags: flatpak
```

License
-------

MIT

Author Information
------------------

- [Mihai Criveti](https://www.linkedin.com/in/crivetimihai/)
