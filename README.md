Ansible Role: Security
=========

[![CI](https://github.com/ricsanfre/ansible-role-security/actions/workflows/ci.yml/badge.svg)](https://github.com/ricsanfre/ansible-role-security/actions/workflows/ci.yml)

Security hardening tasks on Linux.

- SSH access hardening

Requirements
------------

None.


Role Variables
--------------

Available variables are listed below along with default values (see `defaults\main.yaml`)


Security SSH security hardened settings disable the login/password access (only access through SSH keys are allowed), disable root login and others.

security_ssh_password_authentication: "no"
security_ssh_permit_root_login: "no"
security_ssh_usedns: "no"
security_ssh_permit_empty_password: "no"
security_ssh_challenge_response_auth: "no"
security_ssh_gss_api_authentication: "no"
security_ssh_x11_forwarding: "no"


Dependencies
------------

None

Example Playbooks
-----------------

### Apply default rules

Install and configure a firewall on a host with default rules

```yml
- hosts: server
  roles:
    - ricsanfre.security
```