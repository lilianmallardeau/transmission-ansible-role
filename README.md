Transmission Ansible Role
=========================

An Ansible role to install and configure transmission-daemon. Works on Debian-based distributions.

Requirements
------------

None

Role Variables
--------------

Any variable in the transmission-daemon config file (`/etc/transmission-daemon/settings.json`) can be used, prefixed with `transmission_` and with dashes (`-`) converted to underscores (`_`). For example, the `rpc-enabled` parameter in `settings.json` becomes `transmission_rpc_enabled`.

The default values are the ones found by default in `settings.json`.

See https://help.ubuntu.com/community/TransmissionHowTo for more details about some of the available configuration variables.

Dependencies
------------

None

Example Playbook
----------------

```yaml
- hosts: all
  roles:
    - role: transmission
      vars:
        transmission_rpc_enabled: yes
        transmission_rpc_username: "username"
        transmission_rpc_password: "password"
        transmission_download_dir: "/data/transmission/downloads"
```

License
-------

MIT
