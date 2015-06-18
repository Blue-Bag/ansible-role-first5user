BB First 5 User setup
=====================

Ansible role to create basic initial user and env setup
Part of the Blue-Bag First 5 set of roles.

Role Variables
--------------
* *first5user_ansible_username:* The user to manage the server
* *first5user_default_shell* Default shell used for new accounts
* *first5user_root_password* A new password for the root
* *first5user_ansible_password* Password for the first5user_ansible_username
* *first5user_public_ssh_keys* Public keys for connecting to the server

* *first5deploy_user_keys* A private and public key for the deploy user (typically the ansible user)

* *first5user_admin_group* Default group for user (should be overridden)

* *first5user_ansible_groups*  A list of groups to create or remove

* *first5user_ansible_add_groups* An additional set of groups (optional)

* *first5user_ansible_user_groups* Groups for the ansible user to belong to

first5
Usage
-----

```
  - hosts: servers
  gather_facts: true
  sudo: true

  roles:
    - { role: ansible-role-first5user, tags: ["provision", "user"], sudo: true}
```


License
-------

BSD

Author Information
------------------
George Boobyer (Blue-Bag Ltd)