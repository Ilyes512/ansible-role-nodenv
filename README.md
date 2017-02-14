Nodenv (Ansidev)
=========
[![Build Status](https://travis-ci.org/Ilyes512/ansible-role-nodenv.svg)](https://travis-ci.org/Ilyes512/ansible-role-nodenv)

This role installs and configures node through Nodenv for Ubuntu Trusty (14.04) and Xenial (16.04).

Requirements
------------

Any pre-requisites that may not be covered by Ansible itself or the role should be mentioned here. For instance, if the role uses the EC2 module, it may be a good idea to mention in this section that the boto package is required.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.

```
ansidev_package_state: present

nodenv_package_state: "{{ ansidev_package_state }}"
nodenv_user: vagrant
```

Dependencies
------------

No dependencies.

Example Playbook
----------------

```
- hosts: servers
  roles:
     - { role: ilyes512.nodenv, tag: ansidev.nodenv }
```

Todo's
------

[ ] Add node-build.
[ ] Optionally install global node version (and npm)
[ ] Optionally install yarn
[ ] Optionally compile dynamic bash extension to speed up nodenv `$ cd ~/.nodenv && src/configure && make -C
src`

License
-------

MIT

Author Information
------------------

Ilyes Ahidar [@Ilyes512](https://twitter.com/ilyes512)
