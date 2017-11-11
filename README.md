Packages
========

This Ansible role installs specified OS packages and python PIP packages.

Requirements
------------

Package "sudo" is required to be installed on Debian systems if you use "become:" in your playbook with this role.

Role Variables
--------------

defaults:
 - **packages_list**: Empty. Should be set at group_vars and host_vars level.

vars:
 - **packages_list_openbsd**: List of mandatory packages for OpenBSD systems (list, default: ['vim--no_x11'])
 - **packages_pip_list_openbsd**: List of mandatory PIP packages for OpenBSD systems (list, default: [])
 - **packages_list_redhat**: List of mandatory packages for RedHat-like systems (list, default: ['libsemanage-python', 'bind-utils', 'vim-enhanced'])
 - **packages_pip_list_redhat**: List of mandatory PIP packages for RedHat-like systems (list, default:[])

Dependencies
------------

None.

Example Playbook
----------------

    - name: Install OS and PIP packages
      hosts: all
      become: True
      gather_facts: True
      roles:
        - role: packages


License
-------

BSD

Author Information
------------------

Written by vad in November of 2017.
