---
name: databases-expert
description: Эксперт по базам данных, СУБД и управляемым сервисам данных
activation:
  - выбран как эксперт в seo-wizard
---

# Databases Expert Skill

Роль эксперта по базам данных, системам управления данными и облачным DBaaS-сервисам для генерации экспертного контента.

---

## БИЗНЕС-ПРОБЛЕМЫ И VALUE PROPOSITION

### Какие проблемы решают управляемые базы данных

```yaml
pain_points:
  operational_burden:
    problem: "Высокая операционная нагрузка"
    description: "DBA тратят время на рутину: бэкапы, патчи, мониторинг, масштабирование"
    solution: "Managed Database — провайдер берёт на себя администрирование"

  scaling_challenges:
    problem: "Сложность масштабирования"
    description: "Рост данных требует ручного шардирования и репликации"
    solution: "Автоматическое масштабирование в облаке, read replicas по кнопке"

  high_availability:
    problem: "Обеспечение отказоустойчивости"
    description: "Настройка кластеров, failover, репликация требуют экспертизы"
    solution: "Встроенная HA с автоматическим failover в managed-сервисах"

  performance_tuning:
    problem: "Оптимизация производительности"
    description: "Медленные запросы, блокировки, неэффективные индексы"
    solution: "Встроенный мониторинг, Query Insights, рекомендации по оптимизации"

  data_migration:
    problem: "Миграция данных"
    description: "Перенос БД между системами с минимальным downtime"
    solution: "Инструменты миграции, репликация для zero-downtime переезда"

  vendor_lock:
    problem: "Зависимость от вендора"
    description: "Проприетарные СУБД ограничивают выбор и увеличивают затраты"
    solution: "Open Source СУБД (PostgreSQL, MySQL) с полным контролем"
```

### Ценность для разных аудиторий

```yaml
value_proposition:
  developers:
    audience: "Разработчики"
    benefits:
      - "Быстрое развёртывание БД для разработки и тестирования"
      - "API и SDK для автоматизации"
      - "Connection pooling из коробки"
      - "Интеграция с CI/CD"

  dba:
    audience: "Администраторы баз данных"
    benefits:
      - "Автоматизация рутинных задач"
      - "Централизованный мониторинг"
      - "Автоматические бэкапы и PITR"
      - "Управление через Terraform/IaC"

  architects:
    audience: "Архитекторы"
    benefits:
      - "Выбор оптимальной СУБД под задачу"
      - "Горизонтальное и вертикальное масштабирование"
      - "Multi-region репликация"
      - "Гибридные сценарии (on-premise + cloud)"

  business:
    audience: "Бизнес-руководители"
    benefits:
      - "Снижение TCO на инфраструктуру данных"
      - "Предсказуемые расходы (pay-as-you-go)"
      - "Соответствие требованиям безопасности"
      - "Быстрый time-to-market"
```

---

## EXPERT PROFILE

```yaml
name: Эксперт по базам данных
role: Специалист по СУБД, архитектуре данных и облачным DBaaS-сервисам
expertise:
  - Реляционные СУБД (PostgreSQL, MySQL, Oracle, MS SQL)
  - NoSQL базы данных (MongoDB, Redis, Cassandra)
  - Аналитические СУБД (ClickHouse, Greenplum, Vertica)
  - NewSQL и распределённые БД (CockroachDB, TiDB, YugabyteDB)
  - Managed Database сервисы (DBaaS)
  - Репликация, шардирование, кластеризация
  - Резервное копирование и восстановление
  - Миграция баз данных
  - Оптимизация производительности
  - Российские СУБД (Postgres Pro, Tarantool, Arenadata)
tone: Технический, практико-ориентированный, с глубоким пониманием архитектуры данных
```

---

## ТИПЫ БАЗ ДАННЫХ

### Реляционные СУБД (RDBMS)

```yaml
relational_databases:
  description: "Классические SQL-базы с ACID-гарантиями"

  postgresql:
    name: "PostgreSQL"
    type: "Open Source RDBMS"
    description: "Самая продвинутая open source реляционная СУБД"
    strengths:
      - "Полная поддержка ACID"
      - "Расширяемость (extensions, custom types)"
      - "JSON/JSONB для полуструктурированных данных"
      - "Полнотекстовый поиск"
      - "Геопространственные данные (PostGIS)"
      - "Партиционирование таблиц"
      - "Логическая репликация"
    use_cases:
      - "OLTP-системы"
      - "Веб-приложения"
      - "Геоинформационные системы"
      - "Финансовые приложения"
    versions:
      current: "PostgreSQL 16 (2023)"
      lts: "PostgreSQL 14, 15"
    keywords:
      - PostgreSQL
      - Postgres
      - реляционная база данных

  mysql:
    name: "MySQL"
    type: "Open Source RDBMS"
    owner: "Oracle Corporation"
    description: "Самая популярная open source СУБД в мире"
    strengths:
      - "Простота использования"
      - "Высокая производительность для чтения"
      - "Широкая экосистема инструментов"
      - "InnoDB storage engine с ACID"
      - "Group Replication для HA"
    forks:
      - name: "MariaDB"
        description: "Community-fork с дополнительными функциями"
      - name: "Percona Server"
        description: "Enterprise-версия с улучшениями производительности"
    use_cases:
      - "Веб-приложения"
      - "CMS (WordPress, Drupal)"
      - "E-commerce"
    keywords:
      - MySQL
      - MariaDB
      - веб-база данных

  postgres_pro:
    name: "Postgres Pro"
    type: "Enterprise PostgreSQL"
    vendor: "Postgres Professional (Россия)"
    description: "Российская enterprise-версия PostgreSQL"
    editions:
      standard:
        name: "Postgres Pro Standard"
        features:
          - "Оптимизированное ядро"
          - "Улучшенная производительность"
          - "Расширенная диагностика"
      enterprise:
        name: "Postgres Pro Enterprise"
        features:
          - "Multimaster репликация"
          - "Автономные транзакции"
          - "Шардирование (shardman)"
          - "Сертификация ФСТЭК"
    compliance:
      - "Реестр российского ПО"
      - "Сертификат ФСТЭК"
      - "Соответствие 152-ФЗ"
    keywords:
      - Postgres Pro
      - российская СУБД
      - импортозамещение БД
```

### NoSQL базы данных

```yaml
nosql_databases:
  description: "Нереляционные БД для специфических задач"

  mongodb:
    name: "MongoDB"
    type: "Document Database"
    description: "Лидер среди документных NoSQL баз данных"
    data_model: "JSON-подобные документы (BSON)"
    strengths:
      - "Гибкая схема данных"
      - "Горизонтальное масштабирование (шардирование)"
      - "Replica Sets для HA"
      - "Агрегационный фреймворк"
      - "Full-text search"
      - "Транзакции (с версии 4.0)"
    use_cases:
      - "Каталоги продуктов"
      - "Управление контентом"
      - "IoT данные"
      - "Real-time аналитика"
    keywords:
      - MongoDB
      - документная база данных
      - NoSQL

  redis:
    name: "Redis"
    type: "In-Memory Key-Value Store"
    description: "Высокопроизводительное in-memory хранилище"
    data_structures:
      - "Strings"
      - "Lists"
      - "Sets"
      - "Sorted Sets"
      - "Hashes"
      - "Streams"
      - "HyperLogLog"
    strengths:
      - "Сверхнизкая задержка (<1ms)"
      - "Pub/Sub messaging"
      - "Lua scripting"
      - "Redis Cluster для шардирования"
      - "Persistence (RDB, AOF)"
    use_cases:
      - "Кэширование"
      - "Сессии пользователей"
      - "Очереди задач"
      - "Real-time leaderboards"
      - "Rate limiting"
    keywords:
      - Redis
      - кэширование
      - in-memory база данных

  tarantool:
    name: "Tarantool"
    type: "In-Memory Database + Application Server"
    vendor: "VK (Россия)"
    description: "Российская in-memory платформа для высоконагруженных приложений"
    strengths:
      - "In-memory с персистентностью"
      - "Встроенный Lua application server"
      - "ACID-транзакции"
      - "Синхронная репликация"
      - "Высокая производительность (сотни тысяч RPS)"
    use_cases:
      - "Телеком-биллинг"
      - "Финтех"
      - "Игровые серверы"
      - "Session storage"
    vk_cloud:
      service: "Tarantool Cloud"
      features:
        - "Managed Tarantool"
        - "Автоматическое масштабирование"
        - "Встроенный мониторинг"
    keywords:
      - Tarantool
      - VK база данных
      - российская in-memory СУБД

  cassandra:
    name: "Apache Cassandra"
    type: "Wide-Column Store"
    description: "Распределённая БД для больших объёмов данных"
    strengths:
      - "Линейное масштабирование"
      - "Нет единой точки отказа"
      - "Tunable consistency"
      - "Multi-datacenter репликация"
    use_cases:
      - "Time-series данные"
      - "IoT"
      - "Messaging системы"
    keywords:
      - Cassandra
      - wide-column database
```

### Аналитические СУБД (OLAP)

```yaml
analytical_databases:
  description: "СУБД для аналитики и хранилищ данных"

  clickhouse:
    name: "ClickHouse"
    type: "Column-Oriented OLAP Database"
    vendor: "ClickHouse Inc. (изначально Яндекс)"
    description: "Сверхбыстрая колоночная СУБД для аналитики"
    strengths:
      - "Экстремальная скорость аналитических запросов"
      - "Колоночное хранение с компрессией"
      - "Векторизованное выполнение запросов"
      - "SQL-совместимость"
      - "Репликация и шардирование"
      - "Материализованные представления"
    performance:
      - "Миллиарды строк в секунду"
      - "Компрессия данных 10-20x"
    use_cases:
      - "Web-аналитика"
      - "Логирование и мониторинг"
      - "Business Intelligence"
      - "Real-time дашборды"
      - "Ad tech"
    vk_cloud:
      service: "Cloud Databases ClickHouse"
      features:
        - "Managed ClickHouse"
        - "Автоматическое масштабирование"
        - "Резервное копирование"
    keywords:
      - ClickHouse
      - колоночная база данных
      - OLAP
      - аналитическая СУБД

  greenplum:
    name: "Greenplum / Arenadata DB"
    type: "MPP Data Warehouse"
    description: "Массивно-параллельное хранилище данных"
    arenadata:
      name: "Arenadata DB (ADB)"
      vendor: "Arenadata (Россия)"
      description: "Российская enterprise-платформа на базе Greenplum"
      compliance:
        - "Реестр российского ПО"
        - "Сертификация ФСТЭК"
    strengths:
      - "MPP архитектура"
      - "Петабайтные хранилища"
      - "PostgreSQL-совместимость"
      - "Интеграция с Hadoop/Spark"
    use_cases:
      - "Enterprise Data Warehouse"
      - "BI и отчётность"
      - "Data Lake"
    vk_cloud:
      service: "Arenadata DB (март 2024)"
      features:
        - "Managed Arenadata DB"
        - "Единое корпоративное хранилище"
    keywords:
      - Greenplum
      - Arenadata
      - data warehouse
      - хранилище данных
```

### NewSQL и распределённые БД

```yaml
newsql_databases:
  description: "Распределённые SQL-базы с горизонтальным масштабированием"

  cockroachdb:
    name: "CockroachDB"
    type: "Distributed SQL"
    description: "Распределённая SQL-база с автоматическим шардированием"
    strengths:
      - "Глобальное распределение данных"
      - "Serializable isolation"
      - "Автоматический ребаланс"
      - "PostgreSQL-совместимый протокол"
    use_cases:
      - "Глобальные приложения"
      - "Multi-region deployment"

  tidb:
    name: "TiDB"
    type: "Distributed SQL (HTAP)"
    description: "Гибридная OLTP/OLAP распределённая БД"
    strengths:
      - "MySQL-совместимость"
      - "Горизонтальное масштабирование"
      - "HTAP (транзакции + аналитика)"

  yugabytedb:
    name: "YugabyteDB"
    type: "Distributed SQL"
    description: "Распределённая PostgreSQL-совместимая БД"
    strengths:
      - "PostgreSQL-совместимость"
      - "Низкая задержка"
      - "Geo-распределение"
```

---

## MANAGED DATABASE СЕРВИСЫ VK CLOUD

### Обзор Cloud Databases

```yaml
vk_cloud_databases:
  service_name: "Cloud Databases"
  description: "Управляемые базы данных в облаке VK Cloud"

  available_databases:
    postgresql:
      versions: ["12", "13", "14", "15", "16"]
      features:
        - "Автоматические бэкапы"
        - "Point-in-Time Recovery (PITR)"
        - "Read Replicas"
        - "Connection Pooling (PgBouncer)"
        - "Extensions поддержка"
        - "Мониторинг и алерты"

    mysql:
      versions: ["5.7", "8.0"]
      features:
        - "InnoDB storage engine"
        - "Автоматические бэкапы"
        - "Read Replicas"
        - "Мониторинг производительности"

    mongodb:
      versions: ["4.4", "5.0", "6.0"]
      features:
        - "Replica Set из коробки"
        - "Шардированные кластеры"
        - "Автоматические бэкапы"

    redis:
      versions: ["6.x", "7.x"]
      features:
        - "Sentinel для HA"
        - "Cluster mode"
        - "Persistence настройки"

    clickhouse:
      features:
        - "Репликация через ZooKeeper"
        - "Шардирование"
        - "Материализованные представления"

    tarantool:
      service: "Tarantool Cloud"
      features:
        - "Managed Tarantool"
        - "Интеграция с VK Cloud"

    arenadata_db:
      launch: "Март 2024"
      features:
        - "MPP Data Warehouse"
        - "PostgreSQL-совместимость"
        - "Для аналитических задач"

  common_features:
    - "SLA 99.95%"
    - "Автоматическое резервное копирование"
    - "Шифрование данных"
    - "Мониторинг и алерты"
    - "Вертикальное масштабирование"
    - "Приватные сети (VPC)"
    - "Terraform provider"

  pricing:
    model: "Pay-as-you-go"
    billing: "Посекундная тарификация"
    currency: "Рубли / Тенге (Казахстан)"
```

### VDP Lakehouse

```yaml
vdp_lakehouse:
  name: "VDP Lakehouse"
  description: "Платформа больших данных на управляемых облачных сервисах"

  benefits:
    - "Снижение стоимости хранения и обработки данных в 10 раз"
    - "Unified analytics (batch + streaming)"
    - "Delta Lake формат"

  components:
    - "Spark"
    - "Delta Lake"
    - "Object Storage"

  use_cases:
    - "Data Lake"
    - "ETL/ELT пайплайны"
    - "ML Feature Store"
```

---

## АРХИТЕКТУРНЫЕ ПАТТЕРНЫ

### Репликация

```yaml
replication_patterns:
  master_slave:
    name: "Master-Slave (Primary-Replica)"
    description: "Один мастер для записи, реплики для чтения"
    use_cases:
      - "Масштабирование чтения"
      - "Отказоустойчивость"
      - "Географическое распределение"
    considerations:
      - "Асинхронная репликация — возможна потеря данных"
      - "Синхронная репликация — выше задержка"

  multi_master:
    name: "Multi-Master"
    description: "Несколько узлов принимают запись"
    examples:
      - "Galera Cluster (MySQL)"
      - "Postgres Pro Enterprise Multimaster"
      - "CockroachDB"
    considerations:
      - "Конфликты при одновременной записи"
      - "Сложность администрирования"

  logical_replication:
    name: "Логическая репликация"
    description: "Репликация на уровне изменений данных"
    use_cases:
      - "Миграция между версиями"
      - "Выборочная репликация таблиц"
      - "Data integration"
```

### Шардирование

```yaml
sharding_patterns:
  horizontal_sharding:
    name: "Горизонтальное шардирование"
    description: "Разделение данных по строкам между узлами"
    strategies:
      range:
        name: "Range-based"
        description: "По диапазону ключа"
        pros: "Простота, последовательный доступ"
        cons: "Hotspots, неравномерность"
      hash:
        name: "Hash-based"
        description: "По хешу ключа"
        pros: "Равномерное распределение"
        cons: "Сложность range-запросов"
      directory:
        name: "Directory-based"
        description: "Lookup-таблица для маршрутизации"

  considerations:
    - "Cross-shard запросы дорогие"
    - "Distributed transactions сложны"
    - "Ребалансировка при добавлении шардов"
```

### Высокая доступность

```yaml
high_availability:
  failover:
    automatic:
      description: "Автоматическое переключение на реплику"
      tools:
        - "Patroni (PostgreSQL)"
        - "MySQL Group Replication"
        - "MongoDB Replica Set elections"
        - "Redis Sentinel"

  connection_pooling:
    description: "Пул соединений для эффективного использования"
    tools:
      - name: "PgBouncer"
        for: "PostgreSQL"
      - name: "ProxySQL"
        for: "MySQL"
      - name: "Odyssey"
        for: "PostgreSQL (Яндекс)"

  load_balancing:
    description: "Распределение нагрузки между репликами"
    strategies:
      - "Round-robin"
      - "Least connections"
      - "Read/Write split"
```

---

## МИГРАЦИЯ БАЗ ДАННЫХ

### Стратегии миграции

```yaml
migration_strategies:
  lift_and_shift:
    name: "Lift and Shift"
    description: "Перенос БД без изменений"
    tools:
      - "pg_dump/pg_restore"
      - "mysqldump"
      - "mongodump/mongorestore"
    downtime: "Требуется окно простоя"

  online_migration:
    name: "Online Migration"
    description: "Миграция без простоя через репликацию"
    approach:
      - "Настроить репликацию на целевую БД"
      - "Синхронизировать данные"
      - "Переключить приложение"
    tools:
      - "pgloader"
      - "AWS DMS"
      - "Debezium (CDC)"

  dual_write:
    name: "Dual Write"
    description: "Запись в обе БД одновременно"
    considerations:
      - "Изменения в коде приложения"
      - "Возможные расхождения данных"

  strangler_fig:
    name: "Strangler Fig Pattern"
    description: "Постепенный перенос по частям"
    approach:
      - "Новые фичи на новой БД"
      - "Постепенный перенос старых данных"
```

### Инструменты миграции

```yaml
migration_tools:
  postgresql:
    - name: "pg_dump / pg_restore"
      type: "Native tools"
    - name: "pgloader"
      type: "ETL tool"
      features: "Миграция из MySQL, SQLite и др."
    - name: "Ora2Pg"
      type: "Oracle to PostgreSQL"

  mysql:
    - name: "mysqldump"
      type: "Native tool"
    - name: "mysqlpump"
      type: "Parallel dump"
    - name: "Percona XtraBackup"
      type: "Hot backup"

  mongodb:
    - name: "mongodump / mongorestore"
      type: "Native tools"
    - name: "mongomirror"
      type: "Live migration"

  universal:
    - name: "Debezium"
      type: "Change Data Capture"
      description: "Стриминг изменений для online-миграции"
    - name: "AWS Database Migration Service"
      type: "Cloud migration service"
```

---

## ОПТИМИЗАЦИЯ ПРОИЗВОДИТЕЛЬНОСТИ

### Индексирование

```yaml
indexing:
  types:
    btree:
      name: "B-Tree"
      use_cases: ["Equality", "Range queries", "ORDER BY"]
      default: true
    hash:
      name: "Hash"
      use_cases: ["Equality only"]
    gin:
      name: "GIN (Generalized Inverted Index)"
      use_cases: ["Full-text search", "JSONB", "Arrays"]
    gist:
      name: "GiST (Generalized Search Tree)"
      use_cases: ["Геоданные", "Full-text search"]
    brin:
      name: "BRIN (Block Range Index)"
      use_cases: ["Большие таблицы с упорядоченными данными"]

  best_practices:
    - "Индексы на колонки в WHERE, JOIN, ORDER BY"
    - "Составные индексы для частых комбинаций"
    - "Partial indexes для подмножества данных"
    - "Covering indexes для index-only scans"
    - "Регулярный ANALYZE для актуальной статистики"
    - "Мониторинг неиспользуемых индексов"
```

### Query Optimization

```yaml
query_optimization:
  explain_analyze:
    description: "Анализ плана выполнения запроса"
    postgresql: "EXPLAIN (ANALYZE, BUFFERS, FORMAT TEXT)"
    mysql: "EXPLAIN ANALYZE"

  common_issues:
    sequential_scan:
      problem: "Полный просмотр таблицы"
      solution: "Добавить индекс, проверить статистику"
    nested_loop:
      problem: "Неэффективные соединения"
      solution: "Индексы на join-колонки, увеличить work_mem"
    sort_disk:
      problem: "Сортировка на диске"
      solution: "Увеличить work_mem, добавить индекс"

  postgresql_tuning:
    - "shared_buffers: 25% RAM"
    - "effective_cache_size: 75% RAM"
    - "work_mem: зависит от concurrent queries"
    - "maintenance_work_mem: для VACUUM, CREATE INDEX"
    - "checkpoint_completion_target: 0.9"
```

---

## РЕЗЕРВНОЕ КОПИРОВАНИЕ

### Стратегии бэкапов

```yaml
backup_strategies:
  full_backup:
    description: "Полная копия всей базы данных"
    frequency: "Еженедельно"
    tools:
      postgresql: "pg_basebackup"
      mysql: "mysqldump, Percona XtraBackup"

  incremental_backup:
    description: "Только изменения с последнего бэкапа"
    frequency: "Ежедневно"
    tools:
      postgresql: "pgBackRest, Barman"
      mysql: "Percona XtraBackup"

  continuous_archiving:
    description: "Архивирование WAL/binlog для PITR"
    postgresql: "WAL archiving"
    mysql: "Binary log"
    benefit: "Point-in-Time Recovery"

  pitr:
    name: "Point-in-Time Recovery"
    description: "Восстановление на любой момент времени"
    requirement: "Full backup + archived logs"
```

### Managed Backup в VK Cloud

```yaml
vk_cloud_backup:
  features:
    - "Автоматические ежедневные бэкапы"
    - "Настраиваемое расписание"
    - "Retention policy"
    - "Point-in-Time Recovery"
    - "Cross-region копирование"
    - "Восстановление в один клик"

  retention:
    default: "7 дней"
    configurable: "До 35 дней"
```

---

## БЕЗОПАСНОСТЬ БАЗ ДАННЫХ

### Защита данных

```yaml
database_security:
  encryption:
    at_rest:
      description: "Шифрование данных на диске"
      methods:
        - "Transparent Data Encryption (TDE)"
        - "Encrypted tablespaces"
        - "Disk-level encryption"
    in_transit:
      description: "Шифрование соединений"
      methods:
        - "SSL/TLS"
        - "Требование sslmode=require"

  access_control:
    authentication:
      - "Password authentication"
      - "Certificate authentication"
      - "LDAP/AD integration"
      - "IAM integration (cloud)"
    authorization:
      - "Role-Based Access Control (RBAC)"
      - "Row-Level Security (RLS)"
      - "Column-Level Security"

  audit:
    postgresql: "pgAudit extension"
    mysql: "Audit Plugin"
    logging:
      - "Connection logs"
      - "Query logs"
      - "DDL/DML logs"

  compliance:
    - "152-ФЗ (персональные данные)"
    - "PCI DSS (платёжные данные)"
    - "GDPR"
    - "SOC 2"
```

---

## МОНИТОРИНГ И OBSERVABILITY

### Метрики производительности

```yaml
monitoring_metrics:
  database_level:
    - "Connections (active, idle, waiting)"
    - "Transactions per second (TPS)"
    - "Queries per second (QPS)"
    - "Cache hit ratio"
    - "Replication lag"
    - "Deadlocks"
    - "Lock waits"

  query_level:
    - "Slow queries"
    - "Query execution time"
    - "Rows examined vs returned"
    - "Index usage"

  system_level:
    - "CPU utilization"
    - "Memory usage"
    - "Disk I/O"
    - "Network throughput"

  tools:
    postgresql:
      - "pg_stat_statements"
      - "pg_stat_activity"
      - "pgBadger"
    mysql:
      - "Performance Schema"
      - "sys schema"
      - "Percona Monitoring and Management"
    universal:
      - "Prometheus + Grafana"
      - "Datadog"
      - "VK Cloud Monitoring"
```

---

## РОССИЙСКИЙ РЫНОК СУБД

### Импортозамещение

```yaml
russian_databases:
  context:
    description: "Переход на российские СУБД в госсекторе и КИИ"
    drivers:
      - "Требования законодательства"
      - "Санкционные риски"
      - "Реестр российского ПО"

  certified_databases:
    postgres_pro:
      vendor: "Postgres Professional"
      certifications:
        - "ФСТЭК России"
        - "Реестр российского ПО"
      editions: ["Standard", "Enterprise", "Certified"]

    arenadata:
      vendor: "Arenadata"
      products:
        - "Arenadata DB (Greenplum)"
        - "Arenadata Hadoop"
        - "Arenadata Streaming"
      certifications:
        - "Реестр российского ПО"

    tarantool:
      vendor: "VK"
      certifications:
        - "Реестр российского ПО"

    clickhouse:
      note: "Open source, российского происхождения"
      certifications:
        - "Реестр российского ПО (отдельные дистрибутивы)"

  migration_from_oracle:
    drivers:
      - "Уход Oracle из России"
      - "Высокая стоимость лицензий"
    targets:
      - "PostgreSQL / Postgres Pro"
      - "MySQL / Percona"
    tools:
      - "Ora2Pg"
      - "Postgres Pro Migration Toolkit"

  keywords:
    - импортозамещение СУБД
    - российские базы данных
    - ФСТЭК сертификация
    - реестр российского ПО
```

---

## КЛЮЧЕВЫЕ СЛОВА И SEO

### Основные ключевые слова

```yaml
primary_keywords:
  - "базы данных"
  - "СУБД"
  - "PostgreSQL"
  - "MySQL"
  - "MongoDB"
  - "Redis"
  - "ClickHouse"
  - "managed database"
  - "облачная база данных"
  - "DBaaS"

secondary_keywords:
  - "репликация БД"
  - "шардирование"
  - "миграция базы данных"
  - "резервное копирование БД"
  - "оптимизация запросов"
  - "высокая доступность БД"
  - "Postgres Pro"
  - "Tarantool"
  - "Arenadata"
  - "импортозамещение СУБД"

long_tail_keywords:
  - "как выбрать базу данных для проекта"
  - "PostgreSQL vs MySQL сравнение"
  - "миграция с Oracle на PostgreSQL"
  - "настройка репликации PostgreSQL"
  - "оптимизация производительности MySQL"
  - "managed PostgreSQL в облаке"
  - "ClickHouse для аналитики"
  - "Redis для кэширования"
```

---

## WRITING GUIDELINES

### Стиль написания

```yaml
writing_style:
  tone: "Технический, глубокий, практико-ориентированный"
  audience:
    primary: "DBA, DevOps, Backend-разработчики"
    secondary: "Архитекторы, технические руководители"

  principles:
    - "Конкретные технические детали и примеры"
    - "Сравнение альтернатив с плюсами и минусами"
    - "Практические рекомендации по выбору"
    - "Примеры SQL-запросов и конфигураций"
    - "Метрики производительности и бенчмарки"

  avoid:
    - "Устаревшая информация о версиях"
    - "Общие фразы без технической конкретики"
    - "Игнорирование trade-offs"
    - "Рекомендации без учёта контекста"
```

### Структура статей

```yaml
article_structure:
  technical_articles:
    sections:
      - "Введение и постановка задачи"
      - "Обзор вариантов решения"
      - "Сравнительный анализ"
      - "Пошаговая реализация"
      - "Примеры кода/конфигурации"
      - "Мониторинг и troubleshooting"
      - "Заключение"

  comparison_articles:
    sections:
      - "Критерии сравнения"
      - "Обзор каждого решения"
      - "Таблица сравнения"
      - "Рекомендации по выбору"
      - "Use cases для каждого"
```

---

## ИСТОЧНИКИ И ССЫЛКИ

```yaml
sources:
  official_documentation:
    - url: "https://www.postgresql.org/docs/"
      description: "PostgreSQL Documentation"
    - url: "https://dev.mysql.com/doc/"
      description: "MySQL Documentation"
    - url: "https://www.mongodb.com/docs/"
      description: "MongoDB Documentation"
    - url: "https://redis.io/documentation"
      description: "Redis Documentation"
    - url: "https://clickhouse.com/docs/"
      description: "ClickHouse Documentation"

  russian_vendors:
    - url: "https://postgrespro.ru/"
      description: "Postgres Professional"
    - url: "https://arenadata.tech/"
      description: "Arenadata"
    - url: "https://www.tarantool.io/"
      description: "Tarantool"

  vk_cloud:
    - url: "https://cloud.vk.com/docs/dbs"
      description: "VK Cloud Databases Documentation"

  community:
    - url: "https://habr.com/ru/hub/postgresql/"
      description: "Хабр: PostgreSQL"
    - url: "https://habr.com/ru/hub/mysql/"
      description: "Хабр: MySQL"
```

---

## СЛОВАРЬ ТЕРМИНОВ

```yaml
glossary:
  acid:
    term: "ACID"
    definition: "Atomicity, Consistency, Isolation, Durability — свойства транзакций, гарантирующие надёжность"

  cap_theorem:
    term: "CAP-теорема"
    definition: "В распределённой системе можно одновременно обеспечить только два из трёх свойств: Consistency, Availability, Partition tolerance"

  mvcc:
    term: "MVCC"
    definition: "Multi-Version Concurrency Control — механизм управления конкурентным доступом через версионирование строк"

  wal:
    term: "WAL (Write-Ahead Log)"
    definition: "Журнал упреждающей записи для обеспечения durability и recovery"

  pitr:
    term: "PITR (Point-in-Time Recovery)"
    definition: "Восстановление базы данных на любой момент времени"

  sharding:
    term: "Шардирование"
    definition: "Горизонтальное разделение данных между несколькими серверами"

  replica:
    term: "Реплика"
    definition: "Копия базы данных для отказоустойчивости или масштабирования чтения"

  connection_pooling:
    term: "Connection Pooling"
    definition: "Пул соединений для переиспользования подключений к БД"

  dbaas:
    term: "DBaaS"
    definition: "Database as a Service — управляемая база данных в облаке"
```
