Vault role
=========

Requirements
------------

No requirements needed to install vault 

Role Variables
--------------

```yaml
vault_version: 0.2.0
vault_dir: /opt/vault
vault_user: vault
vault_user_password: $6$J9/cJI/s$a0bvktGj1hO1WMG.LDgLlfOFM3.dBSHBJA9d7euRiOvw4TUGWF7Y2SgjqcET4OCjeOupVR9XFM9EqWYIPdFDG.
```

Dependencies
------------

No external dependencies

Example Playbook
----------------

Install vault at a specific version

    - hosts: servers
      roles:
         - { role: migibert.vault, vault_version: "0.2.0" }

License
-------

MIT

Author Information
------------------

Mikaël Gibert, Developer / Devops
