letsencrypt
===========

[![Build Status](https://travis-ci.org/andrelohmann/ansible-role-letsencrypt.svg?branch=master)](https://travis-ci.org/andrelohmann/ansible-role-letsencrypt)

This role installs letsencrypt

Role Variables
--------------

    letsencrypt_authenticator: standalone/webroot
    letsencrypt_webroot_path: /var/www/letsencrypt # optional, only set, if authenticator webroot is chosen
    letsencrypt_prehook: "service nginx stop"
    letsencrypt_posthook: "service nginx start"
    letsencrypt_inis:
    - name: example.com
      email: info@example.com
      domains:
      - example.com
      - test.example.com
      - demo.example.com

Requirements
------------

This role requires ubuntu.

Example Playbook
----------------

    - hosts: all
      roles:
         - { role: andrelohmann.letsencrypt }

License
-------

MIT

Author Information
------------------

https://github.com/andrelohmann
