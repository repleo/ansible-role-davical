Ansible role - DAViCal CalDAV and CardDAV server installer
=====

[![Build Status](https://travis-ci.org/repleo/ansible-role-davical.svg?branch=master)](https://travis-ci.org/repleo/ansible-role-davical)
[![Ansible Galaxy](http://img.shields.io/badge/galaxy-repleo.davical-660198.svg?style=flat)](https://galaxy.ansible.com/repleo/davical)

This role install and configures DAViCal. DAViCal is a PHP based calendar (CalDAV) and contacts (CardDAV) server. Install DAViCal to host your own calendar services and use it in clients like Apple iCal, Contacts, iPhone IOS, Thunderbird and so on.

Requirements
------------

This role requires Ansible 2.0 or higher and platform requirements are listed in the metadata file.

Role Variables
--------------

```yaml
   # General config.
   davical_hostname: cal.example.com
   davical_admin_email: root@example.com

   # SSL Configuration.
   davical_ssl: yes
   davical_redirect_http_to_https: yes
   davical_ssl_certificate: "/etc/nginx/ssl/davical.crt"
   davical_ssl_certificate_key: "/etc/nginx/ssl/davical.key"

   # Database config.
   davical_db_name: davical
   davical_db_password: davical
   davical_db_host: localhost
```

Dependencies
------------

- repleo.nginx
- repleo.postgresql

Example Playbook
----------------

Install davical
```yaml
- { role: repleo.davical }
```


License
-------

GPL v3 - (c) 2016, Repleo, Amstelveen

Author Information
------------------

Repleo, Amstelveen, Holland -- www.repleo.nl  
Jeroen Arnoldus (jeroen@repleo.nl)


