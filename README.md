glauth
=========

**This is a really basic playbook**, as this is my first Ansible role.
Please feel free to submit improvements, particularly on automated molecule
testing!

Installs [glauth], and optionally creates systemd units to run it as a
service. This role does not handle other configuration.

Requirements
------------

* `setcap` binaries, unless the default is changed

Role Variables
--------------

    TODO: for now, see defaults/main.yml

Dependencies
------------

* None

Example Playbook
----------------

    # install binary, no systemd services
    - hosts: ldap_servers
      roles:
        - role: liamdawson.glauth
    
    # install a specific version, and enabled systemd service
    - hosts: auto_ldap_servers
      roles:
        - role: liamdawson.glauth
          glauth_version: v1.1.1
          glauth_service: yes
          glauth_autostart: yes

License
-------

MIT or Apache-2.0, at your choice.

Author Information
------------------

Liam Dawson, ldaws.com

[glauth]: https://github.com/glauth/glauth
