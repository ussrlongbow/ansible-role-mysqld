Role Name
=========

This role install MySQL role from Ubuntu's repo.
Role uses default config and has nothing to do with its modification.

Requirements
------------

`pip` is required to have `mysqclient` installed to create databases and users

Role Variables
--------------

See [defaults](./defaults/main.yml) for role variables.

Dependencies
------------

`geerlingguy.pip` is used as dependency for `pip` installation

Example Playbook
----------------

```
- hosts:
    - dbserver
  roles:
    - role: ussrlongbow.mysqld
      mysqld_databases:
        - wordpress
      mysqld_users:
        - name: wpuser
          pass: 123qwe
          priv: "wordpress.*:ALL"
```

License
-------

MIT

Author Information
------------------

Valentin Gostev (val аt le dоt lc)
