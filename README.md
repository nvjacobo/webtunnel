Ansible Role: Webtunnel
=========

An Ansible Role that installs and configures Webtunel on GNU/Linux

Supported Operating Systems
------------
- Debian bookworm

Requirements
------------

You need root privileges or sudo user to run this role.

Role Variables
--------------
webtunnel_domain:
webtunnel_mail:
webtunnel_path:
webtunnel_name:

Example Playbook
----------------

        - hosts: servers
          vars:
             webtunnel_domain: example.org
             webtunnel_mail: contact@example.org
             webtunnel_path: --------------------
             webtunnel_name: --------------------
          roles:
             - nvjacobo.webtunnel             
