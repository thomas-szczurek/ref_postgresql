# GT PostgreSQL

Ce document recense les ressources collectées dans le cadre du groupe de travail.

## Conseils de configuration

* [work_mem](https://thebuild.com/blog/2023/03/13/everything-you-know-about-setting-work_mem-is-wrong/), formule de calcul du paramètre work_mem
* [memory-management](https://stormatics.tech/blogs/postgresql-memory-management), présentation des différents paramètres mémoires
* [paramètres parallel](https://stormatics.tech/blogs/understanding-postgresql-parallel-query), présentation de quelques paramètres pour la parallélisation
* [CIS Benchmark](https://www.cisecurity.org/benchmark/postgresql), guide de bonnes pratiques pour une configuration sécurisée

## Extensions

Ces projets étendent les possibilités utilisables dans l'environnement de PostgreSQL.
 
### Analyses

* [Libpostal](https://github.com/pramsey/pgsql-postal), Normalisateur d'adresses basé sur OSM
* [MobilityDB](https://mobilitydb.com/) et son [extension QGIS](https://github.com/MobilityDB/MobilityDB-QGIS), extension pour le traitement de données temporelles (trajectoires de véhicules, etc.)
* [Apache AGE](https://age.apache.org/), apporte des fonctions de traitements et d'analyse de graphe
* [pg_duckdb](https://github.com/duckdb/pg_duckdb), déporte à DuckDB l'exécution de requêtes OLAP, permet de lire et d'écrire sur du stockage objet (S3, GCS, R2) du parquet, lit Iceberg/Delta

### Accès et diffusion

* [Foreign Data Wrappers](https://wiki.postgresql.org/wiki/Foreign_data_wrappers)
* [Oracle FDW](https://github.com/laurenz/oracle_fdw), permet de connecter une base pgSQL à oracle
* [OGR FDW](https://github.com/pramsey/pgsql-ogr-fdw), idem mais pour toutes les sources gérées par GDAL-OGR
* [pgsql-http](https://github.com/pramsey/pgsql-http), idem mais pour tous les services http
* [Postgres Message Queue](https://github.com/tembo-io/pgmq), gestionnaire de queues (~kafka/redis)
* [pg_featureserv](https://github.com/CrunchyData/pg_featureserv), service REST OGC API Features
* [pg_graphql](https://github.com/supabase/pg_graphql), support des appels GraphQL (utilisé par Supabase)

### Outils

* [pg_timetable](https://github.com/cybertec-postgresql/pg_timetable), création de jobs ou de chaînes de jobs
* [postgresql_anonymizer](https://labs.dalibo.com/postgresql_anonymizer), gestion de l'anonymisation
* [pg_partman](https://github.com/pgpartman/pg_partman), facilite la gestion du partionnement (temps ou numérique)
* [pg_incremental](https://github.com/CrunchyData/pg_incremental), outil de traitement par lot incrémental

### Types et Indexation

* [postgis_sfcgal](https://oslandia.gitlab.io/SFCGAL/index.html), support de fonctions 3D
* [HyperLogLog](https://github.com/citusdata/postgresql-hll), indexer une fois pour faire de multiples aggrégations à différents niveaux  [exemple](https://www.crunchydata.com/blog/high-compression-metrics-stograge-with-postgres-hyperloglog)
* [HypoPG](https://github.com/HypoPG/hypopg), support d'indexs fictifs pour étudier les usages
* [pg_idkit](https://github.com/VADOSWARE/pg_idkit), générateur d'id (uuid v6 et v7, nanoid, etc.)
* [snowflake-sequences](https://github.com/pgEdge/snowflake?tab=readme-ov-file#snowflake-sequences-for-postgresql), ajout d'un type de séquence Snowflake
* [ZomboDB](https://github.com/zombodb/zombodb), ajoute le support d'ElasticSearch comme type d'index
* [pg_search](https://github.com/paradedb/paradedb/tree/dev/pg_search), recherche textuelle BM25 (~ Lucene) et vectoriel (pg_vector)

### Stockage

* [pg_tde](https://github.com/Percona-Lab/pg_tde), support "transparent" du chiffrement des tables, TOAST et WAL
* [PostGIS](https://postgis.net/), extension spatiale ([Liste des fonctions](https://postgis.net/docs/reference.html))
* [TimescaleDB](https://github.com/timescale/timescaledb), stockage row/column et fonctions spécifiques aux séries temporelles
* [FerretDB](https://www.ferretdb.io/), support des fonctions MongoDB sans MongoDB
* [Citus](https://github.com/citusdata/citus), stockage en colonne et tables distribuées
* [pg_mooncake](https://github.com/Mooncake-Labs/pg_mooncake), permet d'écrire et de lire des données colonnes stockées en Iceberg/Delta
* [pgstream](https://github.com/xataio/pgstream), outil de capture de changements (CDC) qui permet de répliquer les données et changements DDL

## Outils complémentaires externes

### Analyse du serveur

* https://explain.dalibo.com/, outil web pour la visualisation d'un EXPLAIN
* [termBoard](https://labs.dalibo.com/temboard), outil de monitoring
* [pg_activity](https://labs.dalibo.com/pg_activity), outil de monitoring
* [pgstats](https://github.com/gleu/pgstats), outil d'accès et d'export de statistiques
* [pgAudit](https://access.crunchydata.com/documentation/pgaudit/1.5.0/) permet de produire des journeaux d'audit
* [pgBadger](https://pgbadger.darold.net/), outil d'analyse de logs
* [pgBench](https://www.postgresql.org/docs/current/pgbench.html), execution de benchmark
* [pgmonitor](https://github.com/CrunchyData/pgmonitor), statistiques d'usage de la base
* [postgres-checkup](https://gitlab.com/postgres-ai/postgres-checkup), analyse et diagnostics par IA
* [PoWA](https://powa.readthedocs.io/) outil d'analyse des performances
* [pgsql-tweaks](https://gitlab.com/sjstoelting/pgsql-tweaks), ensemble de fonctions PL/PgSQL (vérification de types, vues systèmes, etc.)

### Administration

* [EDB Postgres Enterprise Manager](https://www.enterprisedb.com/docs/pem/latest/)
* [pg_index_watch](https://github.com/dataegret/pg_index_watch), reconstrution automatisé des index
* [pg_auto_reindexer](https://github.com/vitabaks/pg_auto_reindexer?tab=readme-ov-file) Alternative à pg_index_watch pour le réindexage automatisé
* [ldap2pg](https://labs.dalibo.com/ldap2pg), outil de synchronisation LDAP

### Bac à sable

* [postgres-wasm](https://github.com/snaplet/postgres-wasm), permet de faire tourner PgSQL dans votre navigateur

### Déploiement

* [PgLift](https://gitlab.com/dalibo/pglift), outil de mise en production d'instances avec services annexes (sauvegarde, disponibilité et supervision)

### Migration

* [orafce](https://github.com/orafce/orafce)
* [ora2pg](https://github.com/darold/ora2pg/releases)
* [CYBERTEC Migrator](https://www.cybertec-postgresql.com/en/oracle-to-postgresql-migration-cost-assessment/)
* [EDB Migration Toolkit](https://www.enterprisedb.com/products/migration-toolkit-move-oracle-postgresql)
* [transqlate](https://gitlab.com/dalibo/transqlate), conversion de requêtes SQL sauce Oracle vers PostgreSQL
* [db_migrator](https://github.com/cybertec-postgresql/db_migrator), outil de migration de base MS SQL, Oracle et MySQL/MariaDB
* [Pgcompare](https://github.com/CrunchyData/pgCompare), valide la migration de données entre bases
* [pgroll](https://github.com/xataio/pgroll), outil de migration de schéma

### Modélisation

* [pgModeler](https://pgmodeler.io/)

### Pool de connexions

* [PG-Pool-II](https://pgpool.net/mediawiki/index.php/Main_Page)
* [PgBouncer](https://www.pgbouncer.org/)
* [pgagroal](https://agroal.github.io/pgagroal/)
* [PgCat](https://github.com/postgresml/pgcat)
* [Supavisor](https://github.com/supabase/supavisor)

### Réplication

* [Patroni](https://github.com/zalando/patroni)

### Sauvegarde

* [Barman](https://pgbarman.org/)
* [emaj](https://github.com/dalibo/emaj), outil de suivi et de rollback
* [BART](https://www.enterprisedb.com/docs/bart/latest/)

### Utilisation UI

* [DBeaver](https://dbeaver.io/)
* [PgAdmin v4](https://www.pgadmin.org/)
* [Navicat](https://www.navicat.com/en/products/navicat-for-postgresql)

### Usages et API externes

#### API

* [Supabase](https://supabase.com/database), permet de créer des APIs REST, GraphQL depuis PostgreSQL
* [Hasura](https://hasura.io/), , permet de créer des APIs REST, GraphQL depuis PostgreSQL
* [postgREST](https://postgrest.org/en/stable/), serveur http pour gérer des appels REST
* [pg_tileserv](https://github.com/CrunchyData/pg_tileserv), service de tuiles vectorielles
* [Appsmith](https://www.appsmith.com/), application low/nocode (cf. apex)

#### Applications utilisateurs

* [Budibase](https://budibase.com/), création d'applications low/nocode
* [NocoDB](https://nocodb.com/), création de formulaires, équivalent AirTable
* [ReDash](https://github.com/getredash/redash), requêteur SQL et création de datavisualisation
* [Superset](https://github.com/apache/superset),  création de datavisualisation

#### Manipulation des données

* [dbt](https://github.com/dbt-labs/dbt-core), un ELT SQL graphique
* [Singer](https://www.singer.io/), un ETL Python
* [Airbyte](https://github.com/airbytehq/airbyte), ETL/ELT qui permet d'utiliser SQL pour les transformations
* [AirFlow](https://airflow.apache.org/), un orchestrateur de tâches
* [Domino](https://github.com/Tauffer-Consulting/domino), créateur graphique de workflow
* [Viewflow](https://github.com/datacamp/viewflow), création de vues matérialisées en SQL, R, Python
* [Meltano](https://github.com/meltano/meltano), moteur d'intégration (surcouche singer, dbt, airflow)

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
* sur les index
  * H3, index hexagonal, big up pour les analyses avec agrégation : [site](https://h3geo.org/) [installation et utilisation](https://blog.rustprooflabs.com/2023/05/postgis-h3-v4-refresh), [exemples](https://carto.com/blog/h3-spatial-indexes-10-use-cases?hss_channel=tw-241079136)
* trucs et astuces
  * [Crunchydata's tips](https://www.crunchydata.com/postgres-tips)
  * [préocédures stockées](https://www.cybertec-postgresql.com/en/stored-procedures-getting-started/)
  * [Triggers](https://mydbanotebook.org/post/triggers2/), quelques articles sur les triggers dans PgSQL
  * [generate_series](https://database.guide/how-generate_series-works-in-postgresql/), générer des données artificielles pour tester avec des gros volumes
  * [Réparer l'encodage de caractères](https://www.cybertec-postgresql.com/en/fix-bad-encoding-postgresql/)
  * [PostgreSQL Global Temporary Tables](https://github.com/darold/pgtt)
