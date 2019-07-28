ansible-role-sshd_config
=========

Primite sshd config role.

Requirements
------------

Tested on ansible 2.8

sshd on remote host.

Role Variables
--------------

```
---
# ansible turns yes to True and no to False
# if not quoted
ssh_port: 22
ssh_login_time: 30
ssh_use_dns: 'no'
# without-password, 'yes', 'no', prohibit-password
ssh_root_login: 'no'
ssh_debian_banner: 'no'
# 'yes' for root password login
ssh_password_auth: 'no'
ssh_x11_forwarding: 'no'
ssh_use_pam: 'yes'
ssh_tcp_keep_alive: 'yes'
ssh_print_lastlog: 'yes'
ssh_printmotd: 'no'
ssh_strict_modes: 'yes'
ssh_use_priv_separation: 'yes'
ssh_auth_key_file_path: '%h/.ssh/authorized_keys'
ssh_pubkey_auth: 'yes'
ssh_subsystem_sftp: sftp
ssh_subsystem_sftp_path: '/usr/lib/openssh/sftp-server'
ssh_allow_agent_forwarding: 'no'
ssh_allow_tcp_forwarding: 'no'
ssh_challenge_response_auth: 'no'
ssh_permit_empty_passwords: 'no'
ssh_permit_user_environment: 'no'
```

Dependencies
------------

None.

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables
passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: sshd_config, x: 42 }

License
-------

GPLv3

Author Information
------------------

Richard Skumat

https://github.com/richardskumat/
