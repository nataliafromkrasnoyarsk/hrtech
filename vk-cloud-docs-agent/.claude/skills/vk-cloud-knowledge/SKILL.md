---
name: vk-cloud-knowledge
description: Comprehensive knowledge base about VK Cloud platform, services, and documentation structure
---

# VK Cloud Knowledge Base

## When to Use This Skill

Используй этот skill когда нужно:
- Написать статью о любом сервисе VK Cloud
- Найти информацию в официальной документации
- Объяснить архитектуру или возможности VK Cloud
- Сравнить сервисы VK Cloud с аналогами
- Создать туториал или how-to guide

## VK Cloud Platform Overview / Обзор платформы

**VK Cloud** (ранее MCS — Mail.ru Cloud Solutions) — российская облачная платформа, предоставляющая IaaS, PaaS и SaaS решения.

### Ключевые характеристики:
- Российские дата-центры (соответствие ФЗ-152)
- Сертификация ФСТЭК, ФСБ, PCI DSS
- S3-совместимое хранилище
- Managed Kubernetes (CNCF certified)
- Широкий выбор managed databases
- ML-платформа и AI-сервисы
- 24/7 техническая поддержка на русском языке

## Documentation Source / Источник документации

**Официальный репозиторий:** https://github.com/vk-cs/docs-public

### Структура репозитория:

```
docs-public/
├── docs/
│   ├── ru/                          # Русская документация
│   │   ├── applications-and-services/  # Приложения и сервисы
│   │   ├── computing/                   # Вычисления (Cloud Servers)
│   │   ├── kubernetes/                  # Kubernetes aaS
│   │   ├── dbs/                         # Managed Databases
│   │   ├── storage/                     # Хранилища данных
│   │   ├── networks/                    # Сетевые сервисы
│   │   ├── data-platform/               # Big Data & Analytics
│   │   ├── ml/                          # Machine Learning
│   │   ├── monitoring-services/         # Мониторинг
│   │   ├── security/                    # Безопасность
│   │   ├── tools-for-using-services/    # CLI, API, Terraform
│   │   ├── cases/                       # Примеры и кейсы
│   │   ├── intro/                       # Введение
│   │   └── start/                       # Быстрый старт
│   └── en/                          # English documentation
├── guides/                          # Contribution guides
└── README.md
```

### Как получить документацию:

**GitHub API (рекомендуется):**
```
https://api.github.com/repos/vk-cs/docs-public/contents/docs/ru/{service}
```

**Raw файлы:**
```
https://raw.githubusercontent.com/vk-cs/docs-public/master/docs/ru/{service}/{file}.md
```

**Публичная документация:**
```
https://cloud.vk.com/docs/ru/{service}
```

## Service Catalog / Каталог сервисов

### 1. Computing / Вычисления

#### Cloud Servers (Виртуальные машины)
- **Путь в доке:** `docs/ru/computing/`
- **Типы инстансов:** Standard, CPU-Optimized, Memory-Optimized, GPU
- **ОС:** Ubuntu, Debian, CentOS, AlmaLinux, Windows Server, Astra Linux
- **Функции:** Live Migration, Auto-scaling, Placement Groups

#### Cloud Containers
- **Путь в доке:** `docs/ru/computing/cloud-containers/`
- **Описание:** Serverless containers без управления инфраструктурой

### 2. Kubernetes

#### Kubernetes aaS
- **Путь в доке:** `docs/ru/kubernetes/`
- **Версии:** 1.25, 1.26, 1.27, 1.28+ (актуальные)
- **Особенности:**
  - CNCF Certified
  - Auto-scaling (Cluster Autoscaler, HPA, VPA)
  - Managed Ingress (NGINX, Traefik)
  - Persistent Volumes (Cinder, Manila)
  - Интеграция с Container Registry

#### Container Registry
- **Путь в доке:** `docs/ru/kubernetes/registry/`
- **Совместимость:** Docker Registry API v2
- **Функции:** Vulnerability scanning, Image signing

### 3. Databases / Базы данных

#### Реляционные БД
| Сервис | Путь в доке | Особенности |
|--------|-------------|-------------|
| PostgreSQL | `docs/ru/dbs/postgresql/` | Extensions, Replication, Backup |
| MySQL | `docs/ru/dbs/mysql/` | InnoDB, Replication |
| PostgreSQL Pro | `docs/ru/dbs/postgrespro/` | Enterprise features |

#### NoSQL БД
| Сервис | Путь в доке | Особенности |
|--------|-------------|-------------|
| MongoDB | `docs/ru/dbs/mongodb/` | Replica Set, Sharding |
| Redis | `docs/ru/dbs/redis/` | Cluster mode, Sentinel |
| Tarantool | `docs/ru/dbs/tarantool/` | In-memory, Lua |

#### Аналитические БД
| Сервис | Путь в доке | Особенности |
|--------|-------------|-------------|
| ClickHouse | `docs/ru/dbs/clickhouse/` | OLAP, Column-oriented |
| Greenplum | `docs/ru/dbs/greenplum/` | MPP, Analytics |
| OpenSearch | `docs/ru/dbs/opensearch/` | Full-text search, Logs |

#### Специализированные
| Сервис | Путь в доке | Особенности |
|--------|-------------|-------------|
| Kafka | `docs/ru/dbs/kafka/` | Message streaming |
| RabbitMQ | `docs/ru/dbs/rabbitmq/` | Message broker |
| Memcached | `docs/ru/dbs/memcached/` | Caching |

### 4. Storage / Хранилища

#### Cloud Storage (S3)
- **Путь в доке:** `docs/ru/storage/s3/`
- **Совместимость:** AWS S3 API
- **Классы хранения:** Standard, Cold (Glacier-like)
- **Функции:** Versioning, Lifecycle policies, Static website hosting

#### Cloud File Storage
- **Путь в доке:** `docs/ru/storage/nfs/`
- **Протоколы:** NFS, CIFS/SMB
- **Use cases:** Shared storage для VM и Kubernetes

#### Backup
- **Путь в доке:** `docs/ru/storage/backups/`
- **Типы:** VM snapshots, Database backups, File-level backup
- **Политики:** Scheduled, Retention rules

### 5. Networks / Сети

#### Virtual Networks (SDN)
- **Путь в доке:** `docs/ru/networks/`
- **Компоненты:**
  - VPC (Virtual Private Cloud)
  - Subnets
  - Security Groups
  - Floating IPs
  - NAT Gateway

#### Load Balancers
- **Путь в доке:** `docs/ru/networks/balancing/`
- **Типы:**
  - Application LB (L7)
  - Network LB (L4)
- **Функции:** Health checks, SSL termination, Sticky sessions

#### DNS
- **Путь в доке:** `docs/ru/networks/dns/`
- **Функции:** Public/Private zones, A, AAAA, CNAME, MX, TXT records

#### VPN
- **Путь в доке:** `docs/ru/networks/vpn/`
- **Типы:** Site-to-Site VPN, Client VPN

#### CDN
- **Путь в доке:** `docs/ru/networks/cdn/`
- **Функции:** Edge caching, SSL, Custom domains

### 6. Data Platform / Платформа данных

#### Cloud Big Data
- **Путь в доке:** `docs/ru/data-platform/bigdata/`
- **Компоненты:** Hadoop, Spark, Hive, HBase, Airflow

#### Cloud Spark
- **Путь в доке:** `docs/ru/data-platform/spark/`
- **Интеграции:** S3, Kafka, Jupyter

#### Arenadata DB
- **Путь в доке:** `docs/ru/data-platform/arenadata/`
- **Описание:** MPP СУБД на базе Greenplum

### 7. Machine Learning

#### ML Platform
- **Путь в доке:** `docs/ru/ml/mlplatform/`
- **Компоненты:**
  - JupyterHub
  - MLflow
  - Kubeflow (опционально)
  - GPU instances (NVIDIA A100, V100)

#### Cloud Vision
- **Путь в доке:** `docs/ru/ml/vision/`
- **API:** Распознавание лиц, объектов, текста (OCR)

#### Cloud Voice
- **Путь в доке:** `docs/ru/ml/voice/`
- **API:** Speech-to-Text, Text-to-Speech

### 8. Security / Безопасность

#### Web Application Firewall (WAF)
- **Путь в доке:** `docs/ru/security/waf/`
- **Функции:** OWASP Top 10 protection, Bot mitigation

#### DDoS Protection
- **Путь в доке:** `docs/ru/security/ddos/`
- **Уровни:** L3/L4, L7

#### Key Manager
- **Путь в доке:** `docs/ru/security/keys/`
- **Функции:** Управление ключами шифрования, HSM

### 9. Monitoring / Мониторинг

#### Cloud Monitoring
- **Путь в доке:** `docs/ru/monitoring-services/monitoring/`
- **Метрики:** Infrastructure, Application, Custom
- **Алертинг:** Email, SMS, Webhooks

#### Cloud Logging
- **Путь в доке:** `docs/ru/monitoring-services/logging/`
- **Интеграции:** Filebeat, Fluentd, Vector

### 10. Tools / Инструменты

#### OpenStack CLI
- **Путь в доке:** `docs/ru/tools-for-using-services/cli/`
- **Команды:** openstack server, volume, network...

#### Terraform Provider
- **Путь в доке:** `docs/ru/tools-for-using-services/terraform/`
- **Provider:** vkcs/vkcs
- **Registry:** https://registry.terraform.io/providers/vk-cs/vkcs/

#### API
- **Путь в доке:** `docs/ru/tools-for-using-services/api/`
- **Типы:** OpenStack API, VK Cloud API
- **Аутентификация:** Keystone tokens

## Writing Guidelines / Правила написания

### Терминология VK Cloud

| Используй | Не используй |
|-----------|--------------|
| Cloud Servers | ВМ, виртуалки, instances |
| Object Storage | S3, S3-хранилище |
| Kubernetes aaS | K8s, managed k8s |
| Load Balancer | балансировщик |
| Security Group | файрвол, SG |
| Floating IP | внешний IP, публичный IP |

### Структура типовой статьи

```markdown
# {Название}

{Вводный абзац — что решает статья}

## Содержание
[Автогенерация или ручной список]

## Предпосылки

- Учётная запись VK Cloud ([регистрация](https://cloud.vk.com/))
- {Специфические требования}

## Шаг 1: {Действие}

{Описание}

```bash
# Команда
openstack server create ...
```

{Объяснение параметров}

## Шаг N: {Действие}

...

## Проверка результата

{Как убедиться что всё работает}

## Troubleshooting

### Проблема: {описание}

**Причина:** {почему возникает}

**Решение:** {как исправить}

## Полезные ссылки

- [Официальная документация](https://cloud.vk.com/docs/)
- {Другие ресурсы}
```

### Примеры кода

**Terraform (рекомендуемый стиль):**
```hcl
resource "vkcs_compute_instance" "example" {
  name              = "my-server"
  flavor_id         = data.vkcs_compute_flavor.basic.id
  availability_zone = "MS1"

  block_device {
    uuid                  = data.vkcs_images_image.ubuntu.id
    source_type           = "image"
    destination_type      = "volume"
    volume_size           = 10
    delete_on_termination = true
  }

  network {
    uuid = vkcs_networking_network.example.id
  }
}
```

**OpenStack CLI:**
```bash
# Создание виртуальной машины
openstack server create \
  --image ubuntu-22.04 \
  --flavor STD3-2-4 \
  --network my-network \
  --security-group default \
  --key-name my-key \
  my-server

# Проверка статуса
openstack server show my-server -f value -c status
```

**Python SDK:**
```python
from openstack import connection

conn = connection.Connection(
    auth_url="https://infra.mail.ru:35357/v3/",
    project_name="your-project",
    username="your-username",
    password="your-password",
    user_domain_name="users",
    project_domain_name="your-project-domain"
)

# Создание сервера
server = conn.compute.create_server(
    name="my-server",
    flavor_id="<flavor-id>",
    image_id="<image-id>",
    networks=[{"uuid": "<network-id>"}]
)
```

## Research Methodology / Методология исследования

### При написании статьи:

1. **Определи раздел документации**
   ```
   Сервис → Путь в репозитории → Релевантные файлы
   ```

2. **Загрузи актуальную документацию**
   - Используй WebFetch для получения markdown файлов
   - Проверь дату последнего обновления

3. **Извлеки ключевую информацию:**
   - Обзор сервиса (что делает, для чего)
   - Архитектура и компоненты
   - Ограничения и квоты
   - Pricing model (без конкретных цен)
   - Prerequisites
   - Step-by-step инструкции
   - Примеры команд/конфигураций
   - Troubleshooting

4. **Валидируй информацию:**
   - Синтаксис команд корректен
   - Версии актуальны
   - Ссылки работают

## Quality Metrics / Метрики качества

### Статья считается качественной если:

| Критерий | Проверка |
|----------|----------|
| Техническая точность | Все команды работают |
| Актуальность | Информация из текущей версии доки |
| Полнота | Покрыты prerequisites, steps, troubleshooting |
| Читаемость | Логичная структура, понятный язык |
| Практичность | Есть реальные примеры использования |
| Навигация | Содержание, якорные ссылки |
| Источники | Ссылки на официальную документацию |

## Common Patterns / Типовые паттерны

### Паттерн: Quick Start

```markdown
## Быстрый старт: {Сервис} за 5 минут

### 1. Создайте ресурс
{Минимальная команда/конфиг}

### 2. Проверьте статус
{Команда проверки}

### 3. Подключитесь
{Команда подключения}

Готово! Теперь у вас есть работающий {сервис}.
```

### Паттерн: Migration Guide

```markdown
## Миграция с {источник} на VK Cloud {сервис}

### Совместимость
{Таблица совместимости версий/фич}

### Шаг 1: Подготовка
{Экспорт данных из источника}

### Шаг 2: Создание ресурса в VK Cloud
{Команды создания}

### Шаг 3: Импорт данных
{Команды импорта}

### Шаг 4: Переключение
{Обновление connection strings}

### Откат
{Как вернуться назад при проблемах}
```

### Паттерн: Best Practices

```markdown
## Best Practices: {Сервис}

### Производительность
- {Рекомендация 1}
- {Рекомендация 2}

### Безопасность
- {Рекомендация 1}
- {Рекомендация 2}

### Стоимость
- {Рекомендация по оптимизации}

### Мониторинг
- {Какие метрики отслеживать}

### Backup & DR
- {Стратегия резервного копирования}
```

## Alerts & Warnings / Предупреждения

При написании используй callouts для важной информации:

```markdown
> **Note:** Дополнительная информация для контекста.

> **Important:** Критически важная информация, которую нельзя пропустить.

> **Warning:** Предупреждение о возможных проблемах или потере данных.

> **Tip:** Полезный совет для улучшения результата.
```

## Updates & Versioning / Обновления

**Важно:** Документация VK Cloud регулярно обновляется.

При работе с документацией:
1. Проверяй дату последнего коммита в репозитории
2. Сравнивай с версией на cloud.vk.com/docs
3. При расхождениях — приоритет у репозитория (более актуальный)
4. Указывай дату написания статьи
