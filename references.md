# GT PostgreSQL

Ce document recense les ressources collectées dans le cadre du groupe de travail.

## Configuration

## Extensions

* PostGIS
  * [Liste des fonctions](https://postgis.net/docs/reference.html)
* SFCGAL
* Oracle FDW
* [postgresql_anonymizer](https://labs.dalibo.com/postgresql_anonymizer)


## Outils externes

### Utilisation

* [DBeaver](https://dbeaver.io/)
* [PgAdmin v4](https://www.pgadmin.org/)
* [Navicat](https://www.navicat.com/en/products/navicat-for-postgresql)

### Modélisation

* [pgModeler](https://pgmodeler.io/)

### Analyse

* https://explain.dalibo.com/, outil web pour la visualisation d'un EXPLAIN
* [termBoard](https://labs.dalibo.com/temboard), outil de monitoring
* [pg_activity](https://labs.dalibo.com/pg_activity), outil de monitoring
* [ldap2pg](https://labs.dalibo.com/ldap2pg), outil de synchronisation LDAP
* [pgstats](https://github.com/gleu/pgstats), outil d'accès et d'export de statistiques
* []()
* []()

### Administration

* [EDB Postgres Enterprise Manager](https://www.enterprisedb.com/docs/pem/latest/)

### Sauvegarde

* [Barman](https://pgbarman.org/)
* [emaj](https://github.com/dalibo/emaj), outil de suivi et de rollback
* [BART](https://www.enterprisedb.com/docs/bart/latest/)

## En lien avec oracle

### Articles et documentations

* sur une migration
  * [EDB migration Oracle](https://www.enterprisedb.com/blog/the-complete-oracle-to-postgresql-migration-guide-tutorial-move-convert-database-oracle-alternative)
* sur les différences
  * [null & empty strings](https://www.migops.com/blog/null-and-empty-string-in-oracle-vs-postgresql-vs-sql-server/)
  * [migration des synonymes](https://www.migops.com/blog/migration-of-synonyms-from-oracle-to-postgresql/)
  * [type NUMERIC](https://www.migops.com/blog/handling-trailing-zeros-with-numeric-datatype-in-postgresql/)
  * [index rebuild](https://www.migops.com/blog/online-rebuild-of-indexes-oracle-vs-postgresql/)
  * [SUBSTR](https://databaserookies.wordpress.com/2023/01/09/substr-functionality-differences-between-oracle-and-postgresql-what-you-need-to-know/)
  * [ALIAS](https://databaserookies.wordpress.com/2023/01/06/navigating-aliases-in-oracle-to-postgresql-migrations/)
  * [DATE](https://www.migops.com/blog/oracle-vs-sql-server-vs-postgresql-date-date-type/)
  * [transaction control statements ](https://www.migops.com/blog/oracle-vs-postgresql-transaction-control-statements/)
* trucs et astuces
  * [Crunchydata's tips](https://www.crunchydata.com/postgres-tips)

### Migration

* [orafce](https://github.com/orafce/orafce)
* [ora2pg](https://github.com/darold/ora2pg/releases)
* [CYBERTEC Migrator](https://www.cybertec-postgresql.com/en/oracle-to-postgresql-migration-cost-assessment/)
* [EDB Migration Toolkit](https://www.enterprisedb.com/products/migration-toolkit-move-oracle-postgresql)
