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

Centos7, Apache2, a MariaDB/MySQL database.

Specifically, the stunnel configuration expects access to the OULibraries.apache2 role vars.

Also configures Postfix as a local MTA that uses stunnel for TLS connections.  Koha wants to send mail on port 25 without authenticating instead of just using the system sendmail. My first use case for this had an SMTP server that supported TLS, but not StartTLS. So stunnel handles the TLS connection out to the mail server, and postfix logs into the local port in cleartext.

The mail piece would be much simpler if Koha called on the system-configured sendmail like most web apps, or if postfix still directly supported TLS without StartTLS, or if the Library I wrote this role for had a StartTLS-enabled mailserver.

If you want to use this role, but your SMTP server uses StartTLS, just open an issue and I'll add support for it.

Example Playbook
----------------


License
-------

GPLv2

Author Information
------------------

Jason Sherman
