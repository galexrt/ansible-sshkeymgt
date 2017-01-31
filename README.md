ansible-sshkeymgt
=========

[![Build Status](https://travis-ci.org/galexrt/ansible-sshkeymgt.svg?branch=master)](https://travis-ci.org/galexrt/ansible-sshkeymgt)

A role to manage ssh keys for users.

Requirements
------------

No special requirements.

Role Variables
--------------

A description of the settable variables for this role should go here, including any variables that are in defaults/main.yml, vars/main.yml, and any variables that can/should be set via parameters to the role. Any variables that are read from other roles and/or the global scope (ie. hostvars, group vars, etc.) should be mentioned here as well.
```
# the ssh key directory
ssh_key_directory: "/etc/ssh/authorized_keys"

ssh_keys:
  - user: galexrt
    file: "data/test.pub"
  - user: galexrt
    key: "ssh-rsa ..."
[...]
```

Dependencies
------------

No dependencies.

Example Playbook
----------------

An example playbook on how to use this role:

```
- hosts: servers
  roles:
    - { role: galexrt.sshkeymgt, ssh_key_directory: "/etc/ssh/authorized_keys" }
```

License
-------

MIT

Author Information
------------------

If you have problems with the role, feel free to create an issue on Github or contact me by mail.
