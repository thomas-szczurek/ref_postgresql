# GT PostgreSQL

Ce document recense les ressources collectées dans le cadre du groupe de travail.

## Configuration

## Extensions

* PostGIS
  * [Liste des fonctions](https://postgis.net/docs/reference.html)
* [postgis_sfcgal](https://oslandia.gitlab.io/SFCGAL/index.html), support de fonctions 3D
* [Foreign Data Wrappers](https://wiki.postgresql.org/wiki/Foreign_data_wrappers)
  * [Oracle FDW](https://github.com/laurenz/oracle_fdw), permet de connecter une base pgSQL à oracle
  * [OGR FDW](https://github.com/pramsey/pgsql-ogr-fdw), idem mais pour toutes les sources gérées par GDAL-OGR
  * [pgsql-http](https://github.com/pramsey/pgsql-http), idem mais pour tous les services http
* [postgresql_anonymizer](https://labs.dalibo.com/postgresql_anonymizer)
* [FerretDB](https://www.ferretdb.io/), support des fonctions MongoDB sans MongoDB
* [pg_timetable](https://github.com/cybertec-postgresql/pg_timetable), création de jobs ou de chaînes de jobs
* [Citus](https://github.com/citusdata/citus), stockage en colonne et tables distribuées
* [HyperLogLog](https://github.com/citusdata/postgresql-hll), pour faire des count sur des dizaines de milliards d'enregistrements
* [HypoPG](https://github.com/HypoPG/hypopg), support d'indexs fictifs pour étudier les usages
* [https://github.com/CrunchyData/pg_featureserv](https://github.com/CrunchyData/pg_featureserv), service REST OGC API Features


## Outils externes

### Pool de connexions

* [PG-Pool-II](https://pgpool.net/mediawiki/index.php/Main_Page)
* [PgBouncer](https://www.pgbouncer.org/)

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
* [pgAudit](https://access.crunchydata.com/documentation/pgaudit/1.5.0/) permet de produire des journeaux d'audit

### Administration

* [EDB Postgres Enterprise Manager](https://www.enterprisedb.com/docs/pem/latest/)

### Usages et API externes

* [Supabase](https://supabase.com/database), permet de créer des APIs REST, GraphQL sur Postgres

### Sauvegarde

* [Barman](https://pgbarman.org/)
* [emaj](https://github.com/dalibo/emaj), outil de suivi et de rollback
* [BART](https://www.enterprisedb.com/docs/bart/latest/)

### Réplication

* [Patroni](https://github.com/zalando/patroni)

### Migration

* [orafce](https://github.com/orafce/orafce)
* [ora2pg](https://github.com/darold/ora2pg/releases)
* [CYBERTEC Migrator](https://www.cybertec-postgresql.com/en/oracle-to-postgresql-migration-cost-assessment/)
* [EDB Migration Toolkit](https://www.enterprisedb.com/products/migration-toolkit-move-oracle-postgresql)

### Bac à sable

* [postgres-wasm](https://github.com/snaplet/postgres-wasm), permet de faire tourner PgSQL dans votre navigateur

## En lien avec oracle

### Articles et documentations

* sur une migration
  * [EDB migration Oracle](https://www.enterprisedb.com/blog/the-complete-oracle-to-postgresql-migration-guide-tutorial-move-convert-database-oracle-alternative)
  * [Moving from Oracle to PostgreSQL : Lessons learned](https://www.cybertec-postgresql.com/en/building-an-oracle-to-postgresql-migrator-lessons-learned/)
  * [Oracle to PostgreSQL: Basic Architecture](https://www.2ndquadrant.com/en/blog/oracle-to-postgresql-basic-architecture/)
* sur les différences
  * [null & empty strings](https://www.migops.com/blog/null-and-empty-string-in-oracle-vs-postgresql-vs-sql-server/)
  * [migration des synonymes](https://www.migops.com/blog/migration-of-synonyms-from-oracle-to-postgresql/)
  * [type NUMERIC](https://www.migops.com/blog/handling-trailing-zeros-with-numeric-datatype-in-postgresql/)
  * [INTEGER](https://www.crunchydata.com/blog/the-integer-at-the-end-of-the-universe-integer-overflow-in-postgres)
  * [index rebuild](https://www.migops.com/blog/online-rebuild-of-indexes-oracle-vs-postgresql/)
  * [SUBSTR](https://databaserookies.wordpress.com/2023/01/09/substr-functionality-differences-between-oracle-and-postgresql-what-you-need-to-know/)
  * [ALIAS](https://databaserookies.wordpress.com/2023/01/06/navigating-aliases-in-oracle-to-postgresql-migrations/)
  * [DATE](https://www.migops.com/blog/oracle-vs-sql-server-vs-postgresql-date-date-type/)
  * [transaction control statements ](https://www.migops.com/blog/oracle-vs-postgresql-transaction-control-statements/)
* trucs et astuces
  * [Crunchydata's tips](https://www.crunchydata.com/postgres-tips)
  * [préocédures stockées](https://www.cybertec-postgresql.com/en/stored-procedures-getting-started/)
