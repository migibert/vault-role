Vault role
=========
[![Galaxy](http://img.shields.io/badge/ansible--galaxy-vault-blue.svg)](https://galaxy.ansible.com/list#/roles/5261)
[![License](http://img.shields.io/:license-mit-blue.svg)](http://doge.mit-license.org)  
[![Circle CI](https://circleci.com/gh/migibert/vault-role.svg?style=shield)](https://circleci.com/gh/migibert/vault-role)

Requirements
------------

No requirements needed to install this role.

Role Variables
--------------

```
vault_version: 0.5.0
vault_dir: /opt/vault
vault_user: vault
vault_user_password: $6$J9/cJI/s$a0bvktGj1hO1WMG.LDgLlfOFM3.dBSHBJA9d7euRiOvw4TUGWF7Y2SgjqcET4OCjeOupVR9XFM9EqWYIPdFDG.
vault_server: True
vault_server_mode: development (no value means production mode)
vault_server_log_dir: /var/log/vault
vault_server_log_level: info
vault_server_config_path : There is no default value, you MUST provide a server configuration except if you set the variable vault_server_mode with 'development'.
```

Dependencies
------------

No external dependencies

Example Playbook
----------------

Install vault at a specific version

    - hosts: servers
      roles:
         - { role: migibert.vault, vault_version: "0.5.0" }


Install vault server in development mode

    - hosts: servers
      roles:
         - { role: migibert.vault, vault_server_mode: "development" }


Install vault server in production mode

    - hosts: servers
      roles:
         - { role: migibert.vault, vault_server_mode: "production",  vault_server_config_path: "/etc/vault_configuration.hcl"}

Note that the role will not create the server configuration for you, it is your responsibility to provide it because I don't know your requirements =)



License
-------

MIT

Author Information
------------------

Mikael Gibert, Developer / Devops
