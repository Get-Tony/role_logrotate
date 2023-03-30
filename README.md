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
      vars:
        logrotate_conf_dir: /etc/logrotate.d
        logrotate_scripts:
          - name: nginx
            path: /var/log/nginx/*.log
            options:
              - daily
              - missingok
              - rotate 7
              - compress
              - delaycompress
              - notifempty

License
-------

This project is licensed under the MIT License.

Author Information
------------------

This role was created in 2022 by Anthony Pagan.
