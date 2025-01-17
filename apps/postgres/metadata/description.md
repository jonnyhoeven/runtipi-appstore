## The World's Most Advanced Open Source Relational Database

PostgreSQL is a powerful, open source object-relational database system with over 35 years of active development that
has earned it a strong reputation for reliability, feature robustness, and performance.
There is a wealth of information to be found describing how to install and use PostgreSQL through the official documentation.
The open source community provides many helpful places to become familiar with PostgreSQL, discover how it works, and find
career opportunities. Learn more on how to engage with the community.

[Learn More](https://www.postgresql.org/about/)
[Docker Hub](https://hub.docker.com/_/postgres)
[Container env](https://github.com/docker-library/docs/blob/master/postgres/README.md)

Because RunTipi already includes ```postgres:14``` on port ```5432```
this app will use port ```8003```.

To manage postgres you can use [adminer](/app-store/adminer) or [pgAdmin](/app-store/pgadmin)

## Folder Info
| ROOT FOLDER                      | CONTAINER FOLDER         |
|----------------------------------|--------------------------|
| /runtipi/app-data/postgres/data  | /var/lib/postgresql/data |