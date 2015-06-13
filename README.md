ansible-role-cron
=========

Install and configure cron scripts

Requirements
------------

This role has only been tested on EL 6 systems using Ansible 1.9.

Role Variables
--------------

__role\_cron\_crontab\_lines__: Custom lines to be added to /etc/crontab

__role\_cron\_user\_whitelist__: An array of usernames to be added to cron.allow

__role\_cron\_user\_blacklist__: An array of usernames to be added to cron.deny

__role\_cron\_hourly\_scripts__: An array of scripts to be copied from files/etc/cron.hourly/ to /etc/cron.hourly/

__role\_cron\_daily\_scripts__: An array of scripts to be copied from files/etc/cron.daily/ to /etc/cron.daily/

__role\_cron\_weekly\_scripts__: An array of scripts to be copied from files/etc/cron.weekly/ to /etc/cron.weekly/

__role\_cron\_monthly\_scripts__: An array of scripts to be copied from files/etc/cron.monthly/ to /etc/cron.monthly/

__role\_cron\_user\_scripts__: An array of scripts to be copied from files/var/spool/cron/ to /var/spool/cron/

Example Playbook
----------------

Override the above variables by modifying your project's group_vars or host_vars.

```
- hosts: servers
  roles:
    - { role: bitmotive.ansible-role-cron, tags: "cron,common" }
```

License
-------

MIT
