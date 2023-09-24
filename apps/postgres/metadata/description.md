# PostgreSQL

The World's Most Advanced Open Source Relational Database

## Description

PostgreSQL is a powerful, open source object-relational database system with over 35 years of active development that
has earned it a strong reputation for reliability, feature robustness, and performance.
There is a wealth of information to be found describing how to install and use PostgreSQL through the official documentation.
The open source community provides many helpful places to become familiar with PostgreSQL, discover how it works, and find
career opportunities. Learn more on how to engage with the community.

[Learn More](https://www.postgresql.org/about/)
[Docker Hub](https://hub.docker.com/_/postgres)
[Container env](https://github.com/docker-library/docs/blob/master/postgres/README.md)

## Changes since `alpine:3.18`

* Uses `alpine` image instead of `ubuntu`.
* Uses `envsubst` for templating instead of `j2cli`.
* All output goes to `stdout` and `stderr` including `maillog`.
* Included `superviserd` event watcher which will exit the `supervisord` process if one of the monitored processes dies unexpectedly.
* Doesn't use TLS on `smtpd` side.
* And other changes to make the image as **KISS** as possible

## Changed in version `1.3.0`

* Remove `rsyslog` dependancy
* Remove `supervisor`
* Even more **KISS**, just single script used to configure and run `postfix`

## Environment variables

| ENV. Variable            | Description                                                                                                                        |
| ------------------------ | -----------------------------------------------------------------------------------------------------------------------------------|
| `ACCEPTED_NETWORKS`      | Space delimited list of networks to accept mail from. Default: `192.168.0.0/16 172.16.0.0/12 10.0.0.0/8`                     |
| `RECIPIENT_RESTRICTIONS` | Space delimited list of allowed `RCPT TO` addresses. Default: **unrestricted**                                               |
| `SMTP_HOST`              | External relay DNS name. Default: `email-smtp.us-east-1.amazonaws.com`                                                       |
| `SMTP_LOGIN`             | Login to connect to the external relay. **Required**                                                                         |
| `SMTP_PASSWORD`          | Password to connect to the external relay. **Required**                                                                      |
| `SMTP_PORT`              | External relay TCP port. Default: `25`                                                                                       |
| `TLS_VERIFY`             | Trust level for checking remote side cert. Default: `may` (<http://www.postfix.org/postconf.5.html#smtp_tls_security_level>) |
| `USE_TLS`                | Remote require tls. Must be `yes` or `no`. Default: `no`                                                                     |