Ansible Role: Webtunnel
=========

An Ansible Role that installs and configures Webtunnel on GNU/Linux with Caddy

Background
------------

WebTunnel is a censorship-resistant pluggable transport designed to mimic encrypted web traffic (HTTPS) inspired by HTTPT. It works by wrapping the payload connection into a WebSocket-like HTTPS connection, appearing to network observers as an ordinary HTTPS (WebSocket) connection. So, for an onlooker without the knowledge of the hidden path, it just looks like a regular HTTP connection to a webpage server giving the impression that the user is simply browsing the web. 


Supported Operating Systems
------------
- Debian bookworm

Requirements
------------

You need root privileges or sudo user to run this role.

Collections

You need to install community.general collection

    ansible-galaxy collection install community.general


Role Variables
--------------

Put your domain

    webtunnel_domain:
    
Your email address

    webtunnel_mail:
    
Generate path with the command echo $(cat /dev/urandom | tr -cd "qwertyuiopasdfghjklzxcvbnmMNBVCXZLKJHGFDSAQWERTUIOP0987654321"|head -c 24)

    webtunnel_path:
Nickname Bridge
   
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
