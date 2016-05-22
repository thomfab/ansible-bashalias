Bash aliases
============

This role creates bash aliases that are available for all users.

Role Variables
--------------


One variable can be set: `bashalias_aliases`

It is a list of aliases to define. Each element is dictionary defining the alias.

Example:

```
bashalias_aliases:
  - { alias: "ll", command: "ls -hl" }
  - { alias: "la", command: "ls -hal" }
```

Example Playbook
----------------

Example:

```
  ---
  - hosts: servers
    roles:
      - role: thomfab.ansible-bashalias
        bashalias_aliases:
          - { alias: "ll", command: "ls -hl" }
          - { alias: "la", command: "ls -hal" }
```

License
-------

BSD
