ansible-role-dovecot
=========

Role to setup dovecot for froxlor.

Requirements
------------
This role was created for Debian 10.x (Buster). It is configured to work with [froxlor](https://froxlor.org).The role needs a mysql-database and expects a database-schema as it is used by froxlor.
You might use this role in conjunction with the roles:

* ansible-role-apache
* ansible-role-mysql
* ansible-role-froxlor
* ansible-role-postfix

Role Variables
--------------

The following variables don't have defaults. You need to specify them either in a file in group_vars, host_vars directory or via command-line. 

```yaml
postmaster_address: address to use when sending rejection mails
froxlor_mysql_password: the_froxlor_mysql_password

```

Example Playbook
----------------
This role can be easily used in a playbook like this: 

```yaml
- hosts: froxlor-servers
  roles:
      - ansible-role-dovecot
```

License
-------
GNU GENERAL PUBLIC LICENSE VERSION 3

Author Information
------------------
[blog.retter.jetzt](https://blog.retter.jetzt)
