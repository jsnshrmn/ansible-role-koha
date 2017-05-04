jsnshrmn.koha
=========

Installs and configures the Koha ILS from source.

Requirements
------------


Role Variables
--------------

```
mariadb_port: 3306
mariadb_host: localhost
mariadb_db: koha
db_user: root
db_pw: root
kohaadmin_user: kohaadmin
kohaadmin_pw: kohaadmin
smtp_host: smtp.example.com
smtp_port: 465
smtp_authuser: user@example.com
smtp_authpassword: mypass
```

See defaults for the rest.

Dependencies
------------

[Centos7](https://github.com/OULibraries/ansible-role-centos7), [Postfix](https://github.com/OULibraries/ansible-role-postfix-mta), [Apache2](https://github.com/OULibraries/ansible-role-apache2), a [MariaDB/MySQL database](https://github.com/OULibraries/ansible-role-mariadb).

Example Playbook
----------------


License
-------

GPLv2

Author Information
------------------

Jason Sherman
