ansible_ssh-keygen
=========

Role is intended to create and set up ssh key pair authentication for an existing `remote` user.

Requirements
------------

_Optional:_ Run it with sudo password prompt:
```
ansible-playbook --ask-become-pass main.yml -l remote
BECOME password: 
```

Role Variables
--------------

Existing `remote` user.

Dependencies
------------

If the user does not exist, it may require [`ansible_create_user`](https://github.com/110marc/ansible_create_user) role to be played prior `ansible_ssh-keygen`

Example Playbook
----------------

An example of how to use your role:

    - hosts: servers
      become: yes
      roles:
         - ansible_create_user *optional
         - ansible_ssh-keygen

License
-------

BSD

Author Information
------------------

> https://github.com/110marc
