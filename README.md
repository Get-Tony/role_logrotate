logrotate
=========

Deploy logrotate configuration files.

Requirements
------------

None.

Role Variables
--------------

Available variables are listed below, along with default values (see `defaults/main.yml`):

    logrotate_conf_dir
    logrotate_scripts

Dependencies
------------

None.

Example Playbook
----------------

    - name: Deploy logrotate configuration scripts
      hosts: managed
      roles:
         - logrotate

License
-------

All rights reserved.

Author Information
------------------

This role was created in 2022 by Anthony Pagan.
