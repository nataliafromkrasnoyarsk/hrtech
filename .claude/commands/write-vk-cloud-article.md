---
description: Interactive wizard for writing technical articles about VK Cloud services based on official documentation
---

# VK Cloud Article Wizard

## Usage

```bash
/write-vk-cloud-article
```

## What This Command Does

Запускает интерактивный wizard для создания технических статей о сервисах VK Cloud. Агент автоматически обращается к официальной документации (https://github.com/vk-cs/docs-public) для получения актуальной информации.

## Workflow

### STEP 1: Article Type Selection / Выбор типа статьи

Ask: "Какой тип статьи хотите создать?"

Present options:

| Тип | Описание |
|-----|----------|
| **Обзорная статья** | Обзор возможностей сервиса для новых пользователей |
| **Туториал / How-to** | Пошаговая инструкция по решению конкретной задачи |
| **Сравнение** | Сравнение VK Cloud с AWS/GCP/Azure или между сервисами |
| **Best Practices** | Рекомендации по оптимальному использованию |
| **Миграция** | Гайд по переносу с других платформ |
| **Интеграция** | Настройка совместной работы сервисов |

Interactive buttons:
```
[Обзорная статья](claude:Обзорная статья о сервисе)
[Туториал](claude:Пошаговый туториал с практикой)
[Сравнение](claude:Сравнительный обзор)
[Best Practices](claude:Лучшие практики)
[Миграция](claude:Гайд по миграции)
[Интеграция](claude:Интеграция сервисов)
```

### STEP 2: Service Selection / Выбор сервиса VK Cloud

Ask: "О каком сервисе VK Cloud пишем?"

Present services by category:

**Compute & Containers:**
```
[Cloud Servers](claude:Cloud Servers - виртуальные машины)
[Kubernetes aaS](claude:Kubernetes - managed K8s)
[Serverless](claude:Serverless Containers)
```

**Databases:**
```
[PostgreSQL](claude:PostgreSQL managed)
[MySQL](claude:MySQL managed)
[MongoDB](claude:MongoDB managed)
[Redis](claude:Redis managed)
[ClickHouse](claude:ClickHouse OLAP)
[Kafka](claude:Kafka streaming)
```

**Storage:**
```
[Object Storage (S3)](claude:S3-совместимое хранилище)
[File Storage](claude:NFS/CIFS хранилище)
[Backup](claude:Резервное копирование)
```

**Networks:**
```
[Virtual Networks](claude:Сети и VPC)
[Load Balancers](claude:Балансировка нагрузки)
[CDN](claude:Content Delivery Network)
```

**Data & ML:**
```
[Big Data](claude:Hadoop/Spark кластеры)
[ML Platform](claude:JupyterHub, MLflow)
[Cloud Vision](claude:Computer Vision API)
[Cloud Voice](claude:Speech-to-Text/TTS)
```

**Security & Monitoring:**
```
[WAF](claude:Web Application Firewall)
[Cloud Monitoring](claude:Мониторинг и алертинг)
[Cloud Logging](claude:Централизованные логи)
```

Or let user specify: "Или укажите свой сервис..."

### STEP 3: Documentation Research / Исследование документации

**ОБЯЗАТЕЛЬНЫЙ ШАГ:**

1. Определи путь к документации сервиса:
   ```
   https://github.com/vk-cs/docs-public/tree/master/docs/ru/{service-folder}
   ```

2. Загрузи и изучи релевантные страницы:
   - Overview (обзор)
   - Quick Start (быстрый старт)
   - Concepts (концепции)
   - How-to guides (инструкции)
   - API Reference
   - Limits & Quotas (ограничения)

3. Извлеки ключевую информацию:
   - Возможности и функции
   - Поддерживаемые версии/конфигурации
   - Примеры команд и конфигураций
   - Требования и prerequisites
   - Типичные проблемы и решения

Show user: "Изучаю документацию VK Cloud по выбранному сервису..."

### STEP 4: Target Audience / Целевая аудитория

Ask: "Для кого пишем статью?"

```
[DevOps-инженеры](claude:Высокий технический уровень, фокус на автоматизации)
[Backend-разработчики](claude:Средний уровень, интеграция с приложениями)
[Data Engineers](claude:Работа с данными и аналитикой)
[IT-менеджеры](claude:Обзорный уровень, бизнес-ценность)
[Начинающие](claude:Базовый уровень, подробные объяснения)
```

### STEP 5: Outline Creation / План статьи

На основе собранной информации создай структуру:

```markdown
## Предлагаемая структура

1. **Введение**
   - Описание проблемы/задачи
   - Почему VK Cloud {service}

2. **Предпосылки**
   - Требования к учётной записи
   - Необходимые инструменты

3. **{Основная часть - зависит от типа статьи}**
   - ...

4. **Практика**
   - Пошаговые инструкции
   - Примеры кода

5. **Проверка результата**

6. **Troubleshooting**

7. **Полезные ссылки**
```

Ask: "Одобряете структуру? Или хотите изменить?"

```
[Одобряю](claude:Структура подходит, начинаем писать)
[Изменить](claude:Хочу изменить структуру)
[Добавить раздел](claude:Нужен дополнительный раздел)
```

### STEP 6: Content Writing / Написание

Напиши статью следуя правилам:

**Формат:**
- Markdown с правильной разметкой
- Код в блоках с указанием языка
- Заголовки для навигации
- Содержание в начале

**Контент:**
- Краткое введение (2-3 предложения)
- Точные версии и требования
- Копируемые команды
- Пояснения к параметрам
- Примеры вывода команд
- Предупреждения об ошибках

**Ссылки:**
- На официальную документацию VK Cloud
- Формат: `[Текст](https://cloud.vk.com/docs/ru/{path})`

### STEP 7: Review & Save / Проверка и сохранение

После завершения:

1. Покажи полный текст статьи
2. Проведи самопроверку:
   - Техническая корректность
   - Актуальность информации
   - Работоспособность ссылок

3. Предложи варианты сохранения:

```
Статья готова! Как сохранить?

[Сохранить в content-hub](claude:Сохранить как .md в content-hub/vk-cloud-articles/drafts/)
[Показать для копирования](claude:Вывести полный текст)
[Доработать](claude:Внести правки)
```

## Output Location

Статьи сохраняются в:
```
content-hub/vk-cloud-articles/drafts/{YYYY-MM-DD}-{slug}.md
```

## Notes

- Агент ОБЯЗАТЕЛЬНО сверяется с официальной документацией VK Cloud
- Используется репозиторий: https://github.com/vk-cs/docs-public
- Терминология соответствует официальной документации
- Примеры кода проверяются на синтаксическую корректность
