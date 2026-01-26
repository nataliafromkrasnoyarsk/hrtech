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
  launch_time: "Развёртывание за 2-3 минуты"
  sla: "99.95% с финансовыми гарантиями"
  billing: "Посекундная тарификация (pay-as-you-go)"
  bonus: "5000 ₽ на тестирование (60 дней)"

  key_benefits:
    - "Автоматическое резервное копирование"
    - "Гибкое масштабирование по мере роста"
    - "Геораспределённые реплики"
    - "Шифрование данных"
    - "Мониторинг и алерты"
    - "Приватные сети (VPC)"
    - "Terraform provider"
    - "API для автоматизации"
```

### PostgreSQL в VK Cloud

```yaml
vk_cloud_postgresql:
  name: "Cloud Databases PostgreSQL"
  type: "Managed PostgreSQL"
  versions: ["12", "13", "14", "15", "16"]

  configurations:
    single:
      description: "Один инстанс"
      use_case: "Разработка, тестирование"
    master_replica:
      description: "Primary + Read Replica"
      use_case: "Масштабирование чтения"
    cluster:
      description: "HA-кластер с автоматическим failover"
      use_case: "Production, высокая доступность"

  features:
    pitr:
      name: "Point-in-Time Recovery (PITR)"
      description: "Восстановление на любой момент времени"
      how_it_works: "Непрерывное копирование WAL-журналов"
      requirement: "Настроенное расписание резервного копирования"
    connection_pooling:
      name: "PgBouncer"
      modes:
        - name: "Transaction mode"
          default: true
          description: "Соединение удерживается на время транзакции"
        - name: "Session mode"
          description: "Соединение удерживается на время сессии"
      benefit: "Снижение нагрузки на RAM"
    extensions:
      supported: true
      examples: ["PostGIS", "pg_stat_statements", "pgvector"]
    monitoring:
      prometheus: true
      grafana: true
      custom_alerts: true

  replication:
    type: "Потоковая репликация"
    sync_modes: ["Асинхронная", "Синхронная (кворум)"]
    read_replicas: "Поддерживаются"

  backup:
    automatic: true
    schedule: "Настраиваемое"
    retention: "До 35 дней"
    storage: "Отказоустойчивое хранилище"

  update:
    in_place: true
    supported_paths: "12→13→14→15→16"
```

### Postgres Pro Enterprise в VK Cloud

```yaml
vk_cloud_postgres_pro:
  name: "Postgres Pro Enterprise"
  vendor: "Postgres Professional"
  launch_date: "20 сентября 2022"
  status: "Доступен на платформе VK Cloud"

  description: "Enterprise-версия PostgreSQL с расширенными возможностями"

  advantages_over_postgresql:
    - "Более 100 функций для надёжности, производительности, безопасности"
    - "Оптимизированный формат хранения"
    - "Инструменты целостности базы данных"
    - "Резервные копии без остановки системы"
    - "Multimaster репликация"
    - "Автономные транзакции"
    - "Шардирование (shardman)"

  compliance:
    - "Единый реестр российского ПО Минцифры"
    - "Совместимость с Astra Linux"
    - "Сертификация ФСТЭК"

  use_cases:
    - "Проекты с большими объёмами данных"
    - "Высокие требования к производительности"
    - "Требования к надёжности и отказоустойчивости"
    - "Импортозамещение Oracle"

  pricing:
    model: "Посекундная тарификация"
    benefit: "Без капитальных затрат"
```

### MySQL в VK Cloud

```yaml
vk_cloud_mysql:
  name: "Cloud Databases MySQL"
  type: "Managed MySQL"
  versions: ["5.7", "8.0"]

  configurations:
    single: "Один инстанс"
    master_slave: "Primary + Replica"
    cluster: "HA-кластер"

  features:
    - "InnoDB storage engine"
    - "Автоматические бэкапы"
    - "Read Replicas"
    - "Мониторинг производительности"
    - "Расширения и флаги (параметры)"
    - "Prometheus мониторинг"

  use_cases:
    - "Веб-приложения"
    - "CMS (WordPress, Drupal, Joomla)"
    - "E-commerce платформы"
    - "Legacy-системы"
```

### MongoDB в VK Cloud

```yaml
vk_cloud_mongodb:
  name: "Cloud Databases MongoDB"
  type: "Managed MongoDB"
  versions: ["4.4", "5.0", "6.0"]

  configurations:
    replica_set:
      description: "Replica Set из коробки"
      nodes: "3+ узла для кворума"
    sharded_cluster:
      description: "Шардированные кластеры"
      use_case: "Большие объёмы данных"

  features:
    - "Автоматические бэкапы"
    - "Репликация для HA"
    - "Шардирование для масштабирования"
    - "Агрегационный фреймворк"

  use_cases:
    - "Каталоги продуктов"
    - "Управление контентом (CMS)"
    - "IoT данные"
    - "Гибкие схемы данных"
```

### Redis в VK Cloud

```yaml
vk_cloud_redis:
  name: "Cloud Databases Redis"
  type: "Managed Redis"
  versions: ["6.x", "7.x"]

  configurations:
    single:
      description: "Один инстанс"
      note: "Базовая конфигурация"
    sentinel:
      description: "Redis Sentinel для HA"
      features:
        - "Автоматический failover"
        - "Мониторинг master/replica"
        - "Провайдер конфигурации для клиентов"
    cluster:
      description: "Redis Cluster"
      features:
        - "Горизонтальное масштабирование"
        - "Шардирование данных"
        - "Высокая пропускная способность"

  features:
    - "Persistence настройки (RDB, AOF)"
    - "Pub/Sub messaging"
    - "Различные структуры данных"
    - "SSL/TLS шифрование"

  use_cases:
    - "Кэширование"
    - "Сессии пользователей"
    - "Очереди задач"
    - "Real-time leaderboards"
    - "Rate limiting"
```

### ClickHouse в VK Cloud

```yaml
vk_cloud_clickhouse:
  name: "Cloud Databases ClickHouse"
  type: "Managed ClickHouse"
  description: "Колоночная OLAP СУБД для аналитики"

  cluster:
    name: "cluster"
    note: "Имя кластера всегда 'cluster' в VK Cloud"

  configurations:
    single: "Один инстанс"
    replicated:
      description: "Репликация между узлами"
      replication_level: "На уровне таблиц (не БД)"
      coordinator: "ZooKeeper"
    sharded:
      description: "Шардирование для масштабирования"
      note: "Данные распределяются между шардами"

  features:
    - "Репликация через ZooKeeper"
    - "Шардирование"
    - "Материализованные представления"
    - "Реплицируемые и распределённые таблицы"
    - "Внешние словари (PostgreSQL, MySQL, Redis, MongoDB)"

  sql_dialect:
    extensions:
      - "Внешние key-value словари"
      - "Агрегатные функции для приближённых вычислений"
    limitations:
      - "Нет транзакций"
      - "Нет точечных UPDATE/DELETE (только пакетные)"
      - "Ограниченная поддержка JOIN"

  use_cases:
    - "Web-аналитика"
    - "Логирование и мониторинг"
    - "Business Intelligence"
    - "Real-time дашборды"
    - "Ad tech"
```

### Tarantool в VK Cloud

```yaml
vk_cloud_tarantool:
  name: "Tarantool Cloud"
  vendor: "VK Tech"
  type: "Managed In-Memory Database"
  description: "Высокопроизводительная in-memory платформа"

  performance:
    requests_per_second: "До 1 млн RPS"
    latency: "Предсказуемая, не зависит от диска"

  editions:
    community:
      name: "Community Edition"
      configurations: ["Single", "Кластер"]
      open_source: true
    enterprise:
      name: "Enterprise Edition"
      pricing: "По запросу"
      features:
        - "Проприетарные модули"
        - "Официальная поддержка"
        - "Расширенная аналитика"
        - "Работа с данными из разных источников"
    data_grid:
      name: "Tarantool Data Grid"
      pricing: "По запросу"
      description: "Система интеграции данных"
      use_case: "Хранение и аналитика сложных бизнес-объектов"

  cloud_benefits:
    - "Запуск одной кнопкой"
    - "Преднастроенная конфигурация"
    - "Не нужно программировать на Lua"
    - "Не нужно разбираться в шардировании"
    - "Автоматический failover с консистентностью данных"
    - "Квалифицированная поддержка VK Cloud"

  certifications:
    fstec:
      certificate: "№4727"
      valid_until: "Октябрь 2028"
      level: "4 уровень доверия"
      date: "27 апреля 2024"
    astra_linux:
      compatible: "Astra Linux Special Edition 1.7"
      verified: "30 января 2024"

  versions:
    current: "Tarantool 2.11"
    latest: "Tarantool DB 3.0 (октябрь 2025)"

  use_cases:
    - "Телеком-биллинг"
    - "Финтех и банкинг"
    - "Игровые серверы"
    - "Session storage"
    - "Кэширование с отложенной записью"
    - "OLTP-системы"
```

### Arenadata DB в VK Cloud

```yaml
vk_cloud_arenadata:
  name: "Arenadata DB (ADB)"
  base: "Greenplum"
  type: "MPP Data Warehouse"
  launch: "Март 2024 (Казахстан), ранее доступен в России"

  description: "Массивно-параллельная аналитическая СУБД"

  editions:
    community:
      name: "Community"
      support: "Без поддержки"
    enterprise:
      name: "Enterprise"
      features:
        - "Расширенный набор функций"
        - "Техподдержка Arenadata"

  capacity:
    range: "От десятков терабайт до десятков петабайт"

  features:
    - "MPP архитектура"
    - "PostgreSQL-совместимость"
    - "Высокая скорость аналитических запросов"
    - "Интеграция с Hadoop/Spark"
    - "Интеграция с Cloud Big Data"
    - "Совместимость с Cloud Streams"

  replaces:
    - "Oracle Exadata"
    - "Teradata"
    - "SAP HANA"

  use_cases:
    - "Enterprise Data Warehouse"
    - "Единое корпоративное хранилище"
    - "BI и отчётность"
    - "Аналитика продаж"
    - "Планирование закупок"
    - "Данные для ML-моделей"

  pricing:
    model: "Аренда на месяц/день/час"
    benefit: "Без затрат на внедрение инфраструктуры"
```

### OpenSearch в VK Cloud

```yaml
vk_cloud_opensearch:
  name: "Cloud Databases OpenSearch"
  launch_date: "8 июня 2023"
  type: "Managed Search & Analytics Engine"
  description: "Система поиска и анализа информации"

  components:
    - "OpenSearch (search engine)"
    - "OpenSearch Dashboards (визуализация)"

  deployment:
    time: "Пара минут"
    status: "Преднастроен и готов к работе"

  features:
    search:
      - "Полнотекстовый поиск"
      - "Распознавание синтаксиса"
      - "Быстрый поиск по текстовой информации"
    analytics:
      - "Анализ логов"
      - "Поиск аномалий"
      - "Корреляционный анализ"
      - "Machine Learning аналитика"
    monitoring:
      - "Мониторинг безопасности в реальном времени"

  use_cases:
    - "Аналитика трафика сайта"
    - "Поиск в приложениях"
    - "Рекомендательные системы"
    - "Мониторинг безопасности"
    - "Логирование и observability"
    - "E-commerce поиск"

  benefit: "Сокращение затрат на разработку поисковых решений"
```

### Cloud Streams (Kafka)

```yaml
vk_cloud_streams:
  name: "Cloud Streams"
  type: "Managed Apache Kafka"
  description: "Сервис потоковой обработки данных"

  integrations:
    vk_cloud:
      - "Все управляемые СУБД VK Cloud"
      - "Cloud Big Data"
    external:
      - "Elasticsearch"
      - "Couchbase"
      - "Cassandra"
    arenadata:
      - "Arenadata Hadoop"
      - "Arenadata DB (Greenplum)"

  use_cases:
    - "Event streaming"
    - "Real-time data pipelines"
    - "Интеграция микросервисов"
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

### Тарификация VK Cloud Databases

```yaml
vk_cloud_pricing:
  model: "Pay-as-you-go"
  billing: "Посекундная тарификация"
  currencies:
    russia: "Рубли (₽)"
    kazakhstan: "Тенге (₸)"

  trial:
    bonus: "5000 ₽ / 24000 ₸"
    duration: "60 дней"
    note: "Для тестирования сервисов"

  what_you_pay_for:
    - "Вычислительные ресурсы (vCPU, RAM)"
    - "Дисковое пространство"
    - "Резервные копии (Cloud Storage)"
    - "Сетевой трафик"

  calculators:
    russia: "https://mcs.mail.ru/pricing"
    kazakhstan: "https://vkcloud.kz/pricelist/"

  enterprise_pricing:
    tarantool_enterprise: "По запросу"
    tarantool_data_grid: "По запросу"
    postgres_pro_enterprise: "По запросу"
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

## ИССЛЕДОВАНИЯ И РЕЙТИНГИ 2024-2025

### Мировой рынок СУБД (Gartner)

```yaml
gartner_dbms_market_2024_2025:
  market_size_2024:
    total: "$119.7 млрд"
    growth_yoy: "+13.4%"

  market_forecast_2025:
    total: "$137 млрд"
    growth: "+16%"

  cloud_vs_onprem:
    cloud_share: "64%"
    onprem_share: "36%"
    trend: "Облачные DBaaS захватывают большую часть рынка"

  segments_growth_2024:
    nonrelational_dbms: "+22.7%"
    relational_dbms: "+10.8%"

  fastest_growing:
    category: "Graph Databases"
    cagr_5year: "26.4%"

  key_trends_2025:
    - "GenAI интеграция в управление данными"
    - "Data Fabric для интеграции разрозненных данных"
    - "Рост self-service аналитики (30% workforce к 2025)"

  source: "Gartner Market Share Analysis 2024-2025"
```

### DB-Engines Ranking 2025

```yaml
db_engines_ranking_2025:
  description: "Рейтинг популярности СУБД по данным DB-Engines (Q1 2025)"

  top_10:
    - rank: 1
      name: "Oracle Database"
      trend: "Стабильно"
    - rank: 2
      name: "MySQL"
      trend: "Снижение (-125 очков в 2024)"
    - rank: 3
      name: "Microsoft SQL Server"
      trend: "Стабильно"
    - rank: 4
      name: "PostgreSQL"
      trend: "Рост (top climber 4 из 6 месяцев)"
    - rank: 5
      name: "MongoDB"
      trend: "Замедление роста"
    - rank: 6
      name: "Snowflake"
      trend: "Впервые в top-6, обогнал Redis"
    - rank: 7
      name: "Redis"
      trend: "Стабильно"
    - rank: 8
      name: "Databricks"
      trend: "Рост"
    - rank: 9
      name: "IBM Db2"
      trend: "Стабильно"
    - rank: 10
      name: "Elasticsearch"
      trend: "Стабильно"

  dbms_of_the_year:
    2024: "Snowflake"
    2023: "PostgreSQL"

  notable_climbers:
    - name: "PostgreSQL"
      change: "Рост продолжается, особенно для cloud и AI-приложений"
    - name: "Snowflake"
      change: "Крупнейший рост, №1 в рейтинге climbers"
    - name: "ClickHouse"
      change: "С 37 на 31 место, взрывной рост в аналитике"

  open_source_vs_proprietary:
    open_source: "49.8%"
    proprietary: "50.2%"
    tracked_databases: 423

  source: "DB-Engines.com / Redgate Software"
```

### Stack Overflow Developer Survey 2024

```yaml
stackoverflow_survey_2024:
  survey_details:
    respondents: "65,000+"
    countries: 185
    date: "Май 2024"

  database_usage_professional_developers:
    - name: "PostgreSQL"
      usage: "51.9%"
      note: "№1 третий год подряд, впервые >50%"
    - name: "MySQL"
      usage: "39.4%"
      note: "Разрыв с PostgreSQL: 12.5 п.п."
    - name: "SQLite"
      usage: "32.1%"
    - name: "Microsoft SQL Server"
      usage: "~25%"
    - name: "MongoDB"
      usage: "~24%"
    - name: "Redis"
      usage: "~20%"

  postgresql_stats:
    usage_2018: "33%"
    usage_2024: "49%"
    growth: "+16 п.п. за 6 лет"
    admiration_rate: "74.5%"
    demand_growth: "19% (2022) → 47% (2024)"

  learning_to_code_preferences:
    mysql: "45%"
    sqlite: "36%"
    postgresql: "33%"
    note: "Начинающие предпочитают MySQL"

  source: "Stack Overflow Developer Survey 2024"
```

### Тренды NoSQL и аналитических СУБД

```yaml
nosql_analytics_trends_2024_2025:
  clickhouse:
    trend: "Взрывной рост"
    ranking_change: "С #37 на #31 в DB-Engines"
    drivers:
      - "Real-time аналитика"
      - "BI и телеметрия"
      - "Переход от batch к interactive processing"
    2025_highlights:
      - "SharedCatalog инфраструктура"
      - "Warehouses как новая возможность"
      - "Расширенные функции безопасности"
      - "CDC для MySQL в private preview"

  redis:
    position: "Стабильная 7-я позиция"
    trend: "Обогнан Snowflake"
    role: "Invisible infrastructure для кэширования"
    use_pattern: "Часто в паре с MongoDB/PostgreSQL"

  mongodb:
    position: "#5 в рейтинге"
    trend: "Замедление роста"
    challenge: "SQL-движки добавили JSON-поддержку"
    peak_popularity: "~2013 год"

  market_shifts:
    - "NoSQL дополняет, а не заменяет RDBMS (reciprocity 50-69%)"
    - "Cloud-native решения растут (Snowflake, Databricks)"
    - "Специализация под AI/ML workloads"

  emerging_databases:
    - "DuckDB (аналитика в-памяти)"
    - "Supabase (PostgreSQL-as-a-service)"
    - "PlanetScale (MySQL serverless)"
    - "Neon (PostgreSQL serverless)"
```

### Cloud Database Market 2024-2025

```yaml
cloud_database_market:
  market_size:
    forecast_2034: "$91.41 млрд"
    alternative_forecast_2032: "$123.4 млрд"
    cagr: "20.6% (2024-2032)"

  market_share_by_provider:
    aws: "30%"
    azure: "20%"
    gcp: "13%"

  aws_services:
    rds:
      description: "Managed relational databases"
      engines: ["PostgreSQL", "MySQL", "MariaDB", "Oracle", "SQL Server"]
      pricing_example: "db.t3.micro MySQL ~$0.017/час"
    aurora:
      description: "High-performance MySQL/PostgreSQL compatible"
    dynamodb:
      description: "Fully managed NoSQL"
    redshift:
      description: "Data warehouse"

  azure_services:
    sql_database:
      description: "Flagship relational DBaaS"
      feature: "Auto-scaling pricing"
    cosmos_db:
      description: "Multi-model globally distributed"
      highlight: "Low-latency guarantees"
    total_services: 12

  gcp_services:
    cloud_sql:
      engines: ["MySQL", "PostgreSQL", "SQL Server"]
    cloud_spanner:
      description: "Horizontally scalable, strongly consistent"
      unique: "Уникальное предложение на рынке"
    bigquery:
      description: "Serverless data warehouse"

  discounts:
    aws_azure: "Reserved Instances до 72% скидки"
    gcp: "Committed Use Discounts до 70%"

  compliance:
    all_providers: ["SOC 2", "ISO 27001", "PCI DSS", "HIPAA", "GDPR", "FedRAMP"]
```

---

## РОССИЙСКИЙ РЫНОК СУБД 2024-2025

### Объём рынка и динамика

```yaml
russian_dbms_market_2024:
  market_size_2024:
    csr_estimate: "89.5 млрд ₽"
    growth_yoy: "+34%"
    vs_global: "Опережает мировой показатель в 2.5 раза"

  alternative_estimates:
    range: "37-51 млрд ₽"
    growth_2025: "+20%"
    growth_5y_forecast: "~15% CAGR"

  forecast:
    2030: "Рост в 3.5 раза (ЦСР)"
    2031: ">251 млрд ₽"
    cagr_russia: "~16% (на уровне мирового)"

  growth_phases:
    until_2027:
      driver: "Импортозамещение"
      cagr: "21.6%"
    after_2027:
      driver: "AI и рост объёма данных"
      cagr: "11.9%"
```

### Лидеры российского рынка СУБД 2024

```yaml
russian_dbms_leaders_2024:
  ranking:
    - rank: 1
      vendor: "Postgres Professional"
      product: "Postgres Pro"
      revenue_2024: "~9.3 млрд ₽"
      market_share: "10.4%"

    - rank: 2
      vendor: "Arenadata"
      products: ["Arenadata DB", "Arenadata Hadoop"]
      revenue_2024: "~5.6 млрд ₽"
      market_share: "6.7%"

    - rank: 3
      vendor: "Yandex B2B Tech"
      products: ["YDB", "Yandex Cloud DBaaS"]
      revenue_2024: "~3.9 млрд ₽"

    - rank: 4
      vendor: "VK Tech"
      products: ["Tarantool", "VK Cloud Databases"]

    - rank: 5
      vendor: "DIS Group"

  top_10_combined:
    share_of_market: "28.3%"

  source: "CNews, ЦСР, TAdviser 2024"
```

### Импортозамещение СУБД

```yaml
import_substitution_status:
  current_state_2024:
    foreign_systems_installed: ">60%"
    note: "Большинство эксплуатируемых систем — зарубежные"

  progress:
    2021: "64% зависимость от Запада"
    2023: "80% — российские решения (по данным ЦСР)"

  forecast_2031:
    western_new_sales: "<1%"
    return_probability: "58.3% считают возможным возвращение западных игроков"
    dominance: "Не смогут занять доминирующие позиции"

  adoption_by_segment:
    government:
      status: ">50% используют отечественные СУБД"
      critical_services: "Переведены на российские решения"
    enterprise:
      status: "Только 3.5% используют отечественные решения"
      note: "Из 2000+ опрошенных корпоративных клиентов"
    mid_business:
      status: "Очень низкая степень использования"

  legacy_systems:
    oracle: "До сих пор используется >50% респондентов"
    microsoft_sql: "Широко распространён"
```

### Регуляторные требования

```yaml
regulatory_requirements:
  mincifry_guidelines_2024:
    target: "Госкорпорации и компании с госучастием"
    deadlines:
      os_office_antivirus_virtualization: "1 января 2025"
      dbms: "1 января 2026"

  sector_requests:
    banking:
      request: "Перенос сроков на 2027 год"
      reason: "Банковские системы адаптированы под Oracle"

  growth_drivers:
    - "Требования заказчиков и регуляторов к кибербезопасности"
    - "Устойчивый спрос на импортозамещение западного ПО"
    - "Рост профессионализма команд и зрелости продуктов"
    - "Государственная поддержка"
```

### Российские СУБД и их специализация

```yaml
russian_dbms_specialization:
  postgresql_forks:
    postgres_pro:
      vendor: "Postgres Professional"
      specialization: "Enterprise, интеграция с банковскими АБС"
      certifications: ["ФСТЭК", "Реестр российского ПО"]
    tantor:
      vendor: "Тантор Лабс (ГК Астра)"
      specialization: "Работа с 1С"
    arenadata_prosperity:
      vendor: "Arenadata"
      specialization: "Enterprise PostgreSQL"
    pangolin:
      vendor: "Сбер"
      specialization: "Внутренние системы банка"
    jatoba:
      vendor: "Газинформсервис"
      specialization: "Безопасность, сертификация"

  analytics:
    arenadata_db:
      base: "Greenplum"
      type: "MPP-СУБД для аналитики"
      replaces: ["Oracle Exadata", "Teradata", "SAP HANA"]
      use_case: "Критически важные системы с большими данными"

  in_memory:
    tarantool:
      vendor: "VK Tech"
      type: "In-Memory + Application Server"
      role: "Дополнение к классической СУБД"
      use_case: "Real-time транзакции, аналитика на миллисекундах"
```

---

## ИМПОРТОЗАМЕЩЕНИЕ ORACLE И MS SQL

### Переход с Oracle

```yaml
oracle_migration:
  drivers:
    - "Уход Oracle из России"
    - "Высокая стоимость лицензий"
    - "Санкционные риски"
    - "Требования 187-ФЗ о КИИ"

  target_platforms:
    primary:
      - "PostgreSQL / Postgres Pro"
      - "Arenadata DB (для OLAP)"
    secondary:
      - "MySQL / Percona"
      - "YDB (Yandex)"

  migration_tools:
    - name: "Ora2Pg"
      type: "Open Source"
      capabilities: "DDL, DML, PL/SQL конвертация"
    - name: "Postgres Pro Migration Toolkit"
      type: "Enterprise"
      capabilities: "Полный цикл миграции"
    - name: "AWS SCT"
      type: "Cloud"
      note: "Schema Conversion Tool"

  challenges:
    - "PL/SQL → PL/pgSQL конвертация"
    - "Проприетарные типы данных Oracle"
    - "Sequences и identity columns"
    - "Materialized views синтаксис"
    - "Stored procedures портирование"

  timeline_typical:
    assessment: "2-4 недели"
    schema_migration: "1-3 месяца"
    data_migration: "Зависит от объёма"
    testing: "2-4 месяца"
    total: "6-12 месяцев для крупных систем"
```

### Переход с Microsoft SQL Server

```yaml
mssql_migration:
  drivers:
    - "Санкционные ограничения"
    - "Лицензионные риски"

  target_platforms:
    - "PostgreSQL / Postgres Pro"
    - "MySQL / MariaDB"

  key_differences:
    - from: "T-SQL"
      to: "PL/pgSQL или стандартный SQL"
    - from: "IDENTITY"
      to: "SERIAL / GENERATED"
    - from: "TOP N"
      to: "LIMIT N"
    - from: "GETDATE()"
      to: "NOW() / CURRENT_TIMESTAMP"
```

---

## СЕРТИФИЦИРОВАННЫЕ РОССИЙСКИЕ СУБД

```yaml
certified_russian_databases:
  fstec_certified:
    postgres_pro:
      vendor: "Postgres Professional"
      editions: ["Standard", "Enterprise", "Certified"]
      certifications:
        - "ФСТЭК России (до 1 класса защищённости)"
        - "Реестр российского ПО"
      features_certified:
        - "Мандатный контроль доступа"
        - "Защита от НСД"
        - "Аудит действий"

    arenadata_db:
      vendor: "Arenadata"
      certifications:
        - "Реестр российского ПО"
        - "В процессе сертификации ФСТЭК"

    tarantool:
      vendor: "VK Tech"
      certifications:
        - "Реестр российского ПО"

    jatoba:
      vendor: "Газинформсервис"
      base: "PostgreSQL"
      certifications:
        - "ФСТЭК России"
        - "Реестр российского ПО"
      specialization: "ГИС, КИИ, ИСПДн"

  registry_only:
    clickhouse:
      note: "Open source, российского происхождения"
      status: "Отдельные дистрибутивы в реестре"

    greenplum_forks:
      - "Arenadata DB"
      - "Greenplum от Arenadata"

  compliance_requirements:
    152_fz: "Персональные данные"
    187_fz: "Критическая информационная инфраструктура"
    pci_dss: "Платёжные данные"
    gost: "ГОСТ Р 57580 (финансовый сектор)"
```

---

## ПРОГНОЗЫ И ТРЕНДЫ 2025-2030

```yaml
market_trends_2025_2030:
  global:
    ai_integration:
      description: "GenAI меняет работу с данными"
      impact: "Автоматизация DBA-задач, query optimization"

    vector_databases:
      description: "Рост спроса для AI/ML приложений"
      growth: "PostgreSQL pgvector популярность +150%"

    data_fabric:
      description: "Интеграция разрозненных источников"
      benefit: "-30% времени на data integration (Forrester)"

    serverless_databases:
      description: "Pay-per-query модели"
      examples: ["Aurora Serverless", "Neon", "PlanetScale"]

  russia:
    import_substitution_completion:
      timeline: "2026-2027"
      driver: "Регуляторные требования"

    ai_driven_growth:
      timeline: "После 2027"
      driver: "ИИ и рост объёмов данных"

    market_consolidation:
      description: "Укрупнение вендоров"
      leaders: ["Postgres Pro", "Arenadata", "VK Tech", "Yandex"]

    specialization:
      oltp: "PostgreSQL-форки (Postgres Pro, Tantor, Pangolin)"
      olap: "Arenadata DB, ClickHouse"
      in_memory: "Tarantool, Redis"
      ai_ml: "YDB, ClickHouse + ML"

  sources:
    - "Gartner Data & Analytics Trends 2025"
    - "ЦСР прогноз рынка СУБД России"
    - "IDC Worldwide Data Platform Forecast"
    - "Forrester Data Fabric Report"
```

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
  - "рынок СУБД 2024"
  - "DB-Engines рейтинг"
  - "Postgres Pro vs PostgreSQL"
  - "Arenadata DB отзывы"
  - "переход с Oracle на PostgreSQL"
  - "российские СУБД для КИИ"
  - "ФСТЭК сертификация СУБД"
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
  market_research:
    - url: "https://www.gartner.com/en/documents/6588602"
      description: "Gartner Market Share Analysis: DBMS 2024"
    - url: "https://db-engines.com/en/ranking"
      description: "DB-Engines Ranking"
    - url: "https://survey.stackoverflow.co/2024/"
      description: "Stack Overflow Developer Survey 2024"
    - url: "https://www.tadviser.ru/"
      description: "TAdviser: Российский рынок СУБД"
    - url: "https://www.cnews.ru/reviews/rynok_subd_2025"
      description: "CNews: Рынок СУБД 2025"
    - url: "https://www.csr.ru/"
      description: "ЦСР: Исследования рынка данных"

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
    - url: "https://ydb.tech/"
      description: "YDB (Yandex)"

  vk_cloud:
    - url: "https://cloud.vk.com/docs/dbs"
      description: "VK Cloud Databases Documentation"

  community:
    - url: "https://habr.com/ru/hub/postgresql/"
      description: "Хабр: PostgreSQL"
    - url: "https://habr.com/ru/hub/mysql/"
      description: "Хабр: MySQL"
    - url: "https://www.anti-malware.ru/analytics/"
      description: "Anti-Malware: Аналитика рынка СУБД"
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
