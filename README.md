# Awesome Apache Iceberg Links

Подборка полезных ресурсов по [Apache Iceberg](https://iceberg.apache.org/): документация, каталоги, движки запросов, облачные сервисы и материалы сообщества. Многие материалы — на русском языке.

Обозначения ссылок: ✅ — доступность проверена автоматически; ⚠️ — автоматическая проверка недоступна (сайт блокирует роботов), но ссылка подтверждается поисковыми индексами.

## Содержание

- [Курсы по Apache Iceberg](#курсы-по-apache-iceberg)
- [Официальная документация и спецификация](#официальная-документация-и-спецификация)
- [Основы и архитектура](#основы-и-архитектура)
- [Каталоги и REST Catalog](#каталоги-и-rest-catalog)
- [Движки запросов и библиотеки](#движки-запросов-и-библиотеки)
- [Где попробовать (песочницы и демо)](#где-попробовать-песочницы-и-демо)
- [Оптимизация и обслуживание таблиц](#оптимизация-и-обслуживание-таблиц)
- [Time Travel, ветвление и версионирование](#time-travel-ветвление-и-версионирование)
- [Сервисы и управляемые платформы](#сервисы-и-управляемые-платформы)
- [CDC и стриминговая запись](#cdc-и-стриминговая-запись)
- [Инструменты и утилиты](#инструменты-и-утилиты)
- [Топовые статьи блогов](#топовые-статьи-блогов)
- [Книги](#книги)
- [Видео и конференции](#видео-и-конференции)
- [Сообщества](#сообщества)

## Курсы по Apache Iceberg

- [Apache Iceberg: практический курс](https://subquery.ru/course/iceberg) — бесплатный русскоязычный курс из 6 глав и 19 уроков: от архитектуры и каталогов до обслуживания таблиц и экосистемы движков.
- [Apache Iceberg and Tableflow (Tim Berglund)](https://www.timberglund.com/videos/apache-iceberg-course) ✅ — видеокурс автора спецификации Iceberg: архитектура формата, транзакции, каталоги и практические примеры.
- [Плейлист курса на YouTube](https://www.youtube.com/playlist?list=PLf38f5LhQthcLN84xP6JgQ-pEbAc8SbSi) ⚠️ — модули курса Берглунда на канале Confluent.

## Официальная документация и спецификация

- [Официальный сайт](https://iceberg.apache.org/) ✅ — обзор проекта, ключевые возможности и ссылки на все разделы.
- [Документация](https://iceberg.apache.org/docs/latest/) ✅ — концепции, конфигурация, интеграции со Spark, Flink и Hive.
- [Спецификация формата](https://iceberg.apache.org/spec/) ✅ — детальное описание v1–v3: типы данных, манифесты, снапшоты, трансформации партиционирования.
- [Релизы](https://iceberg.apache.org/releases/) ✅ — страница загрузки релизов и артефактов.
- [Официальный блог](https://iceberg.apache.org/blog/) ✅ — анонсы новых версий и технические заметки команды проекта.

## Основы и архитектура

- [Вступление](https://subquery.ru/blog/courses/iceberg/introduction) — зачем нужен Iceberg и как устроен табличный формат.
- [Архитектура и концепции](https://subquery.ru/blog/courses/iceberg/architecture-and-concepts) — файлы данных, манифесты, списки манифестов и метаданные.
- [ACID-транзакции](https://subquery.ru/blog/courses/iceberg/acid-transactions) — атомарность, консистентность, изоляция и долговечность на практике.
- [UPDATE и DELETE](https://subquery.ru/blog/courses/iceberg/updates-and-deletes) — copy-on-write, merge-on-read и write amplification.
- [Типы данных и эволюция схемы](https://subquery.ru/blog/courses/iceberg/data-types-and-schema-evolution) — безопасное добавление, переименование и удаление колонок.

## Каталоги и REST Catalog

- [Каталоги](https://subquery.ru/blog/courses/iceberg/catalogs) — как выбрать каталог: Hive Metastore, AWS Glue, REST Catalog.
- [Протокол REST Catalog](https://iceberg.apache.org/docs/latest/rest-protocol/) ✅ — спецификация протокола: эндпоинты, коммит-протокол, выдача учётных данных.
- [Настройка REST-каталога](https://iceberg.apache.org/docs/latest/rest-catalog/) ✅ — подключение Spark и Flink с аутентификацией OAuth2/SigV4/Google.
- [Apache Polaris](https://polaris.apache.org/) ✅ — открытый каталог ASF с поддержкой REST API Iceberg.
- [Репозиторий apache/polaris](https://github.com/apache/polaris) ✅ — исходный код и quickstart-инструкция.
- [Lakekeeper](https://lakekeeper.io/) ✅ — REST-каталог на Rust с централизованным контролем доступа.
- [Репозиторий lakekeeper/lakekeeper](https://github.com/lakekeeper/lakekeeper) ✅ — исходники и готовые примеры docker-compose.
- [Project Nessie](https://projectnessie.org/) ✅ — транзакционный каталог с Git-подобным версионированием.
- [Unity Catalog](https://github.com/unitycatalog/unitycatalog) ✅ — открытый мультимодальный каталог (LF AI & Data), совместимый с Iceberg REST.
- [AWS Glue как каталог](https://iceberg.apache.org/docs/latest/aws/#glue-catalog) ✅ — официальный гайд по использованию Glue Catalog.
- [Hive Metastore / HiveCatalog](https://iceberg.apache.org/docs/latest/hive/) ✅ — глобальный каталог поверх Hive Metastore.

## Движки запросов и библиотеки

- [Движки запросов и экосистема](https://subquery.ru/blog/courses/iceberg/query-engines-and-ecosystem) — обзор Spark, Flink, Trino, облачных сервисов и Python-инструментов.
- [Trino](https://subquery.ru/blog/trino) — русскоязычный обзор Trino и его интеграций, включая Iceberg.
- [DuckDB Iceberg extension](https://duckdb.org/docs/current/core_extensions/iceberg/overview.html) ✅ — чтение и запись Iceberg, работа через ATTACH к REST-каталогу.
- [Trino Iceberg connector](https://trino.io/docs/current/connector/iceberg.html) ✅ — конфигурация, метатаблицы, процедуры оптимизации, time travel.
- [Spark Quickstart](https://iceberg.apache.org/spark-quickstart/) ✅ — быстрый старт со Spark через Docker Compose.
- [Flink Quickstart](https://iceberg.apache.org/flink-quickstart/) ✅ — быстрый старт интеграции Flink.
- [PyIceberg](https://py.iceberg.apache.org/) ✅ — Python-реализация без JVM: чтение/запись Arrow, Pandas, Polars, CLI.
- [iceberg-rust](https://github.com/apache/iceberg-rust) ✅ — реализация формата на Rust, основа Lakekeeper.
- [iceberg-go](https://github.com/apache/iceberg-go) ✅ — Go-реализация с поддержкой REST/Hive/Glue/SQL каталогов.
- [iceberg-cpp](https://github.com/apache/iceberg-cpp) ✅ — C++-реализация (C++23, CMake), интеграции с Arrow.
- [StarRocks Iceberg catalog](https://docs.starrocks.io/docs/data_source/catalog/iceberg/) ⚠️ — подключение внешнего Iceberg-каталога в StarRocks.
- [ClickHouse Iceberg table engine](https://clickhouse.com/docs/en/engines/table-engines/integrations/iceberg) ✅ — движок и табличная функция для чтения/записи Iceberg.

## Где попробовать (песочницы и демо)

- [Упражнение: каталоги](https://subquery.ru/blog/courses/iceberg/catalogs-exercise) — создание первой таблицы и изучение снапшотов.
- [Упражнение: эволюция схемы](https://subquery.ru/blog/courses/iceberg/schema-evolution-exercise) — добавление, удаление и переименование колонок.
- [Упражнение: партицирование](https://subquery.ru/blog/courses/iceberg/partitioning-exercise) — партицированная таблица, генерация данных, pruning.
- [Упражнение: time travel](https://subquery.ru/blog/courses/iceberg/timetravel-exercise) — путешествия во времени и снапшоты.
- [Упражнение: ветвление](https://subquery.ru/blog/courses/iceberg/branching-exercise) — практика Git-подобного workflow.
- [Упражнение: обслуживание](https://subquery.ru/blog/courses/iceberg/maintenance-exercise) — очистка и оптимизация таблиц.
- [docker-spark-iceberg](https://github.com/databricks/docker-spark-iceberg) ✅ — популярный демо-стенд Spark + Iceberg + MinIO.
- [Nessie: попробовать](https://projectnessie.org/guides/try-nessie/) ✅ — Docker-композ Nessie + MinIO и подключение Spark SQL.
- [Примеры Lakekeeper](https://github.com/lakekeeper/lakekeeper/tree/main/examples) ✅ — минимальные примеры с Jupyter-ноутбуками.

## Оптимизация и обслуживание таблиц

- [Партицирование и эволюция партиций](https://subquery.ru/blog/courses/iceberg/partitioning-and-partition-evolution) — hidden partitioning, трансформации и эволюция.
- [Кластеризация](https://subquery.ru/blog/courses/iceberg/clustering) — Z-ordering и сравнение с партицированием.
- [Метатаблицы](https://subquery.ru/blog/courses/iceberg/metadata-tables) — анализ файлов, партиций и entries для отладки производительности.
- [Обслуживание таблиц](https://subquery.ru/blog/courses/iceberg/table-maintenance) — удаление снапшотов, компактификация, очистка метаданных.
- [Пять причин медленных Iceberg-запросов](https://subquery.ru/blog/iceberg-queries-speedup) — диагностика мелких файлов, манифестов и партиций.
- [Maintenance (официальные доки)](https://iceberg.apache.org/docs/latest/maintenance/) ✅ — expire snapshots, orphan-файлы, компакция данных и манифестов.
- [RisingWave: small file problem](https://risingwave.com/blog/iceberg-small-file-problem/) ✅ — разбор проблемы мелких файлов и стратегии компакции.
- [Dremio: small files](https://www.dremio.com/blog/apache-iceberg-small-files-problem-causes-fixes-and-prevention/) ⚠️ — причины, лечение и профилактика мелких файлов.
- [Dremio: компакция](https://www.dremio.com/blog/compaction-in-apache-iceberg-fine-tuning-your-iceberg-tables-data-files/) ⚠️ — тонкая настройка компакции data-файлов.
- [Expire Snapshots / Orphan Files](https://iceberglakehouse.com/iceberg/iceberg-expire-snapshots/) ⚠️ — справочник по срокам жизни снапшотов и очистке.

## Time Travel, ветвление и версионирование

- [Time travel и откат изменений](https://subquery.ru/blog/courses/iceberg/timetravel-and-rollback) — запросы к прошлым версиям таблицы и rollback.
- [Тегирование и ветвление](https://subquery.ru/blog/courses/iceberg/tagging-and-branching) — Git-подобный workflow и Write-Audit-Publish.
- [Branching and Tagging (доки)](https://iceberg.apache.org/docs/latest/branching/) ✅ — официальная документация по веткам, тегам и WAP.
- [Time Travel (справочник)](https://iceberglakehouse.com/iceberg/iceberg-time-travel/) ✅ — синтаксис time travel в Spark, Trino, Dremio и PyIceberg.

## Сервисы и управляемые платформы

- [Лейкхаус как у Google](https://subquery.ru/blog/6-layer-lakehouse-from-google) — разбор шести слоёв производительности Iceberg по мотивам Borderless Lakehouse.
- [Snowflake: Apache Iceberg tables](https://docs.snowflake.com/en/user-guide/tables-iceberg) ⚠️ — Iceberg-таблицы, включая Snowflake в роли каталога.
- [BigQuery: managed Iceberg tables](https://cloud.google.com/bigquery/docs/iceberg-tables) ✅ — управляемые и внешние Iceberg-таблицы в BigQuery/BigLake.
- [AWS Athena: запросы к Iceberg](https://docs.aws.amazon.com/athena/latest/ug/querying-iceberg.html) ✅ — чтение, запись и time travel через Glue Catalog.
- [Databricks: Apache Iceberg](https://docs.databricks.com/gcp/en/iceberg/) ✅ — managed и foreign таблицы в Unity Catalog, Iceberg v3.
- [Microsoft Fabric / OneLake](https://learn.microsoft.com/en-us/fabric/onelake/onelake-iceberg-tables) ✅ — виртуализация Delta ↔ Iceberg и шорткаты.
- [Cloudera: Apache Iceberg](https://www.cloudera.com/open-source/apache-iceberg.html) ✅ — Iceberg в составе open data lakehouse CDP.
- [Google Cloud Blog: Borderless Lakehouse](https://cloud.google.com/blog/products/data-analytics/introducing-the-borderless-lakehouse) ✅ — федерация каталогов через Iceberg REST.

## CDC и стриминговая запись

- [Kafka Connect](https://iceberg.apache.org/docs/latest/kafka-connect/) ✅ — потоковая запись событий в Iceberg-таблицы.
- [Debezium → Iceberg](https://memiiso.github.io/debezium-server-iceberg/) ✅ — CDC из баз данных в Iceberg через Debezium Server.

## Инструменты и утилиты

- [Apache Amoro](https://amoro.network) ✅ — самооптимизация таблиц: автономная компакция и управление жизненным циклом.
- [apache/iceberg-rest-fixture](https://github.com/apache/iceberg-rest-fixture) ⚠️ — лёгкий REST-каталог для тестов и разработки.

## Топовые статьи блогов

- [DuckDB и Apache Iceberg](https://subquery.ru/blog/duckdb-iceberg) — лейкхаус без кластера: чтение, запись и подводные камни.
- [Работаем с Iceberg из Trino и DuckDB](https://subquery.ru/blog/iceberg-trino-duckdb) — практика работы с форматом без «большой» СУБД.
- [Ryan Blue: Iceberg — A High-Performance Format](https://www.dremio.com/blog/iceberg-a-high-performance-format-for-huge-analytic-tables/) ⚠️ — историческая статья одного из создателей Iceberg.
- [Architectural Look Under the Covers](https://www.dremio.com/blog/apache-iceberg-an-architectural-look-under-the-covers/) ⚠️ — внутреннее устройство формата: манифесты, метаданные, снапшоты.
- [Netflix: Iceberg and Spark in Production](https://netflixtechblog.com/iceberg-and-spark-in-netflix-production-b5d9eaad927b) ⚠️ — опыт переноса продакшена на Iceberg.
- [Iceberg Knowledge Base](https://iceberglakehouse.com/iceberg/) ✅ — независимая база знаний: термины, WAP, компакция.

## Книги

- [Apache Iceberg: The Definitive Guide](https://github.com/developer-advocacy-dremio/definitive-guide-to-apache-iceberg) ✅ — companion-репозиторий книги O'Reilly (авторы T. Shiran, A. Merced) с кодом примеров.

## Видео и конференции

- [Доклады Iceberg](https://iceberg.apache.org/talks/) ✅ — официальная подборка talks со ссылками на плейлисты Iceberg Summit.
- [YouTube @ApacheIceberg](https://www.youtube.com/@ApacheIceberg) ✅ — официальный канал проекта.

## Сообщества

- [Репозиторий apache/iceberg](https://github.com/apache/iceberg) ✅ — основной репозиторий (Java-реализация), issues и PR.
- [Dev mailing list](https://lists.apache.org/list.html?dev@iceberg.apache.org) ✅ — список рассылки разработчиков.
- [Slack-приглашение](https://s.apache.org/iceberg-slack) ✅ — вступление в Slack-сообщество.
- [X/Twitter @ApacheIceberg](https://x.com/ApacheIceberg) ⚠️ — аккаунт проекта.
- [Data Engineers (Telegram)](https://t.me/data_engineers) ⚠️ — русскоязычное сообщество инженеров данных.
- [BigData team (Telegram)](https://t.me/bigdata_team) ⚠️ — русскоязычный канал про большие данные.
- [DataHub RU (Telegram)](https://t.me/datahub_ru) ⚠️ — русскоязычное обсуждение дата-инструментов.

## Как добавить ссылку

Откройте pull request или issue с предложением — правила описаны в [CONTRIBUTING.md](CONTRIBUTING.md).