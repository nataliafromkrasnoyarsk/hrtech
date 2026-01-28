# Prompt Contents

Модульная система AI-агентов для Claude Code — профессиональное создание технического контента, экспертных колонок, пресс-релизов и маркетинговых материалов.

**[Канал в Telegram](https://t.me/proitru)** — промты, новости ИИ, техноконтентское

---

## Содержание

- [Архитектура системы](#архитектура-системы)
- [Агенты](#агенты)
- [Команды](#команды)
- [Skills](#skills)
- [Модули](#модули)
  - [Content Creation Suite](#content-creation-suite)
  - [Columnist Wizard](#columnist-wizard)
  - [Press Release Wizard](#press-release-wizard)
  - [Event Page Wizard](#event-page-wizard)
  - [SEO Content Creator](#seo-content-creator)
  - [Landing Creator](#landing-creator)
  - [Landing Page Updater](#landing-page-updater)
  - [VK Cloud Docs Agent](#vk-cloud-docs-agent)
- [YAML-промты](#yaml-промты)
- [Структура репозитория](#структура-репозитория)

---

## Архитектура системы

Система построена на трёх уровнях: **агенты** (специализированные AI-роли), **команды** (интерактивные workflows) и **skills** (экспертные знания).

```
┌─────────────────────────────────────────────────────────────────┐
│                        COMMANDS (10)                            │
│  /article-workflow  /draft-article  /trend-research            │
│  /write-column  /write-press-release  /create-event            │
│  /seo-create-article  /create-landing  /update-landing         │
│  /write-vk-cloud-article                                        │
└───────────────────────────┬─────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────────┐
│                        AGENTS (12)                              │
├─────────────────────────────────────────────────────────────────┤
│  RESEARCH        │  CREATION           │  QUALITY CONTROL      │
│  ────────────    │  ─────────          │  ───────────────      │
│  Tech Content    │  Tech Content       │  Tech Fact-Checker    │
│  Strategist      │  Writer             │  Content Editor       │
│                  │  Columnist Wizard   │  SEO Content          │
│                  │  Press Release      │  Optimizer            │
│                  │  Event Wizard       │                       │
│                  │  SEO Wizard         │                       │
│                  │  Landing Creator    │                       │
│                  │  Landing Updater    │                       │
│                  │  VK Cloud Docs      │                       │
└───────────────────────────┬─────────────────────────────────────┘
                            ↓
┌─────────────────────────────────────────────────────────────────┐
│                        SKILLS (25+)                             │
│  editorial-excellence    enterprise-storytelling                │
│  fact-checking-methodology    tech-trends-research              │
│  media-publishing-guidelines    14 publication-specific skills  │
└─────────────────────────────────────────────────────────────────┘
```

---

## Агенты

12 специализированных AI-агентов, каждый с уникальной ролью:

| Агент | Модуль | Назначение |
|-------|--------|------------|
| **Tech Content Strategist** | trend-researcher | Исследование трендов, IMPACT-скоринг, стратегия контента |
| **Tech Content Writer** | tech-writer | Написание технических статей и черновиков |
| **Tech Fact-Checker** | content-editor | Проверка фактов, верификация источников |
| **Content Editor** | content-editor | Редактура, структурирование, полировка текста |
| **SEO Content Optimizer** | seo-publisher | SEO-оптимизация, мета-данные, дистрибуция |
| **Columnist Wizard** | columnist-wizard | Экспертные колонки для 14 российских СМИ |
| **Press Release Wizard** | press-release-wizard | Профессиональные пресс-релизы |
| **Event Wizard** | event-page-wizard | Страницы мероприятий (вебинары, конференции) |
| **SEO Wizard** | seo-content-creator | SEO-статьи через интерактивный wizard |
| **Landing Content Creator** | landing-creator | Создание контента лендингов (7 типов, 30+ блоков) |
| **Landing Updater Wizard** | landing-updater | Обновление текстов лендингов |
| **VK Cloud Docs Writer** | vk-cloud-docs-agent | Технические статьи о VK Cloud на основе официальной документации |

---

## Команды

10 интерактивных команд для запуска workflows:

| Команда | Агенты | Описание |
|---------|--------|----------|
| `/article-workflow` | 5 агентов | Полный цикл: исследование → написание → фактчек → редактура → SEO |
| `/draft-article` | Tech Content Writer | Быстрое создание черновика статьи |
| `/trend-research` | Tech Content Strategist | Исследование трендов с IMPACT-скорингом |
| `/write-column` | Columnist Wizard | Экспертная колонка для выбранного издания |
| `/write-press-release` | Press Release Wizard | Пресс-релиз с пошаговой генерацией |
| `/create-event` | Event Wizard | Страница мероприятия (MD + JSON) |
| `/seo-create-article` | SEO Wizard | SEO-статья через wizard |
| `/create-landing` | Landing Content Creator | Создание контента лендинга (7 типов) |
| `/update-landing` | Landing Updater | Обновление текста лендинга |
| `/write-vk-cloud-article` | VK Cloud Docs Writer | Статья о сервисах VK Cloud |

---

## Skills

25+ экспертных knowledge bases, встроенных в агентов:

### Универсальные skills

| Skill | Описание |
|-------|----------|
| `editorial-excellence` | Техники редактирования (структурный, параграф, предложение) |
| `enterprise-storytelling` | Нарративные техники, PRFAQ, case study templates |
| `technical-writing-standards` | Стандарты технического письма |
| `fact-checking-methodology` | Трёхуровневая верификация (Tier 1-3 источники) |
| `tech-trends-research` | IMPACT framework, методология исследования |
| `media-publishing-guidelines` | Требования Forbes, HBR, TechCrunch, Habr, VC.ru |

### Publication-specific skills (14 изданий)

**Деловые СМИ:** Forbes Russia, РБК, Ведомости, Коммерсантъ, Эксперт, Профиль

**Технологические СМИ:** Хабр, VC.ru, CNews, TAdviser

**Tech-порталы:** iXBT, 3DNews, Ferra, Hi-Tech Mail.ru

Каждый skill содержит: требования к формату, стилистику, примеры статей, чеклист.

---

## Модули

### Content Creation Suite

Ядро системы — 4 модуля, работающих вместе через `/article-workflow`:

```
┌─────────────────────────────────────────────────────────────────┐
│  PHASE 1: RESEARCH                                              │
│  Agent: Tech Content Strategist                                 │
│  Output: Trend report + 3-5 content briefs с IMPACT scores     │
└────────────────────────────────┬────────────────────────────────┘
                                 ↓
┌─────────────────────────────────────────────────────────────────┐
│  PHASE 2: DRAFTING                                              │
│  Agent: Tech Content Writer                                     │
│  Output: Outline → Draft v1 + Editorial notes                  │
└────────────────────────────────┬────────────────────────────────┘
                                 ↓
┌─────────────────────────────────────────────────────────────────┐
│  PHASE 3: FACT-CHECK & EDIT                                     │
│  Agents: Tech Fact-Checker + Content Editor                     │
│  Output: Verified draft + Edit report                          │
└────────────────────────────────┬────────────────────────────────┘
                                 ↓
┌─────────────────────────────────────────────────────────────────┐
│  PHASE 4: SEO & PUBLISH                                         │
│  Agent: SEO Content Optimizer                                   │
│  Output: Publication-ready article + SEO report                │
└─────────────────────────────────────────────────────────────────┘
```

#### Trend Researcher

**Агент:** Tech Content Strategist
**Команда:** `/trend-research`

- Анализ технологических трендов
- IMPACT-скоринг для приоритизации тем
- Конкурентный анализ контента
- Подготовка питчей для изданий

**Skill:** `tech-trends-research`

#### Tech Writer

**Агент:** Tech Content Writer
**Команда:** `/draft-article`

**Форматы:**
- Opinion pieces (800-1,200 слов)
- Технические туториалы (1,500-2,500 слов)
- Case studies (1,200-2,000 слов)
- Trend analysis (1,000-1,800 слов)
- Whitepapers (2,500-5,000 слов)

**Skills:** `enterprise-storytelling`, `technical-writing-standards`

#### Content Editor

**Агенты:** Tech Fact-Checker, Content Editor

**Уровни редактирования:**
- Light Edit — грамматика, выбор слов
- Medium Edit — ясность, flow, консистентность
- Heavy Edit — структура, аргументация

**Иерархия источников:**

| Tier | Источники |
|------|-----------|
| Tier 1 | Официальная документация, peer-reviewed |
| Tier 2 | Gartner, IDC, официальные блоги |
| Tier 3 | Tech media, industry reports |

**Skills:** `fact-checking-methodology`, `editorial-excellence`

#### SEO Publisher

**Агент:** SEO Content Optimizer
**Команда:** `/article-workflow`

- Оптимизация заголовков (3-5 вариантов)
- Мета-описания и ключевые слова
- IMPACT scoring (100 баллов)
- Стратегия дистрибуции

**Skill:** `media-publishing-guidelines`

---

### Columnist Wizard

**Агент:** Columnist Wizard
**Команда:** `/write-column`

Создание экспертных колонок от лица руководителей для российских СМИ.

```
ШАГ 1: Выбор персоны (CTO, CPO, CEO, CISO, CFO)
    ↓
ШАГ 2: Выбор издания → загрузка skill
    ↓
ШАГ 3: Источник (текст / PDF / URL / тема)
    ↓
ШАГ 4: План колонки на согласование
    ↓
ШАГ 5: Написание по стилю издания
    ↓
ШАГ 6: Сохранение как пример
```

**14 поддерживаемых изданий:**

| Категория | Издания |
|-----------|---------|
| Деловые СМИ | Forbes Russia, РБК, Ведомости, Коммерсантъ, Эксперт, Профиль |
| Tech СМИ | Хабр, VC.ru, CNews, TAdviser |
| Tech-порталы | iXBT, 3DNews, Ferra, Hi-Tech Mail.ru |

**Типы колонок:**
- Трендовый анализ
- Контринтуитивный взгляд
- Из опыта (уроки проектов)
- Стратегический комментарий
- Методология / How-To

---

### Press Release Wizard

**Агент:** Press Release Wizard
**Команда:** `/write-press-release`

```
ШАГ 1: Приём материалов
ШАГ 2: Анализ и исследование
ШАГ 3: Уточняющие вопросы
ШАГ 4: 3 варианта заголовков
ШАГ 5: Варианты лидов
ШАГ 6: Генерация текста
ШАГ 7: Сборка и валидация
```

**Типы:** Запуск продукта, Партнёрство, Линейка продуктов, Обновление

**Skill:** `press-release-knowledge`

---

### Event Page Wizard

**Агент:** Event Wizard
**Команда:** `/create-event`

10-шаговый wizard для создания страниц мероприятий.

**Типы:** Вебинар, Конференция, Митап, Воркшоп, Хакатон, Демо-день

**Выход:** Markdown + JSON файлы

**Skill:** `event-templates`

---

### SEO Content Creator

**Агент:** SEO Wizard
**Команда:** `/seo-create-article`

Интерактивный wizard для SEO-статей.

**Режимы:**
- `balanced` — баланс SEO и читаемости
- `deep_expert` — технический экспертный контент
- `strict_seo` — максимальная SEO-оптимизация

**Skills:** `seo-knowledge`, `vk-cloud-security-expert`

---

### Landing Creator

**Агент:** Landing Content Creator
**Команда:** `/create-landing`

7-шаговый wizard для создания контента лендингов с автоматическим определением типа.

```
ШАГ 1: Получение брифа (текст / файл / вопросы)
ШАГ 2: Анализ и уточнение
ШАГ 3: Предложение структуры (автоопределение типа + блоки)
ШАГ 4: SEO-параметры
ШАГ 5: Генерация контента
ШАГ 6: Выбор формата (Markdown / HTML / JSON)
ШАГ 7: Доработка и сохранение
```

**7 типов лендингов:**

| Тип | Описание |
|-----|----------|
| Product Landing | Страница продукта (8-17 секций) |
| Security Product | ИБ-продукт (SIEM, защита) |
| Beta Product | Продукт в бета-тесте |
| Solution Navigator | Навигатор по сценариям |
| Industry Solution | Отраслевое решение |
| Special Project | Спецпроект / контент-хаб |
| Referral Program | Партнёрская программа |

**Skills:** `landing-knowledge`

---

### Landing Page Updater

**Агент:** Landing Updater Wizard
**Команда:** `/update-landing`

Обновление текстов лендингов с сохранением структуры.

```
СОХРАНЯЕМ:                 ОБНОВЛЯЕМ:
- Количество блоков        - Формулировки
- Иерархию H1→H2→текст     - SEO-оптимизацию
- Общий смысл              - Актуальность данных
```

**Skill:** `landing-knowledge`

---

### VK Cloud Docs Agent

**Агент:** VK Cloud Docs Writer
**Команда:** `/write-vk-cloud-article`

Создание технических статей о сервисах VK Cloud на основе официальной документации.

**Источник данных:** [github.com/vk-cs/docs-public](https://github.com/vk-cs/docs-public)

```
ШАГ 1: Выбор типа статьи (обзор / туториал / сравнение / best practices)
    ↓
ШАГ 2: Выбор сервиса VK Cloud
    ↓
ШАГ 3: Исследование официальной документации
    ↓
ШАГ 4: Определение целевой аудитории
    ↓
ШАГ 5: Создание и одобрение плана
    ↓
ШАГ 6: Написание статьи
    ↓
ШАГ 7: Проверка и сохранение
```

**Покрытые сервисы VK Cloud:**

| Категория | Сервисы |
|-----------|---------|
| Compute | Cloud Servers, Kubernetes aaS, Serverless |
| Databases | PostgreSQL, MySQL, MongoDB, Redis, ClickHouse, Kafka |
| Storage | Object Storage (S3), File Storage, Backup |
| Networks | Virtual Networks, Load Balancers, CDN, VPN |
| Data & ML | Big Data, ML Platform, Cloud Vision, Cloud Voice |
| Security | WAF, DDoS Protection, Key Manager |
| Monitoring | Cloud Monitoring, Cloud Logging |

**Типы статей:**
- Обзорная статья
- Туториал / How-to
- Сравнение сервисов
- Best Practices
- Гайд по миграции
- Интеграция с другими сервисами

**Skill:** `vk-cloud-knowledge`

---

## YAML-промты

**Расположение:** `prompts/`

Standalone промты для использования без Claude Code:

| Файл | Описание |
|------|----------|
| `prompt_seo_1_analyze_and_build_params.yaml` | Аналитик параметров |
| `prompt_seo_2_generate_article.yaml` | Генератор статей |
| `prompt_seo_3_infostyle_transformer_2_0.yaml` | Инфостайл-трансформер |

---

## Структура репозитория

```
prompt-contents/
├── .claude/
│   └── commands/                        # Глобальные slash-команды (10)
│
├── trend-researcher/                    # Research & Strategy
│   └── .claude/
│       ├── agents/tech-content-strategist.md
│       └── skills/tech-trends-research/
│
├── tech-writer/                         # Content Creation
│   └── .claude/
│       ├── agents/tech-content-writer.md
│       └── skills/
│           ├── enterprise-storytelling/
│           └── technical-writing-standards/
│
├── content-editor/                      # Quality Control
│   └── .claude/
│       ├── agents/
│       │   ├── tech-fact-checker.md
│       │   └── content-editor.md
│       └── skills/
│           ├── fact-checking-methodology/
│           └── editorial-excellence/
│
├── seo-publisher/                       # SEO & Distribution
│   └── .claude/
│       ├── agents/seo-content-optimizer.md
│       └── skills/media-publishing-guidelines/
│
├── columnist-wizard/                    # Expert Columns
│   └── .claude/
│       ├── agents/columnist-wizard.md
│       └── skills/media/
│           ├── business/               # 6 изданий
│           ├── tech/                   # 4 издания
│           └── portals/                # 4 портала
│
├── press-release-wizard/                # PR Communications
│   └── .claude/
│       ├── agents/press-release-wizard.md
│       └── skills/press-release-knowledge/
│
├── event-page-wizard/                   # Event Marketing
│   └── .claude/
│       ├── agents/event-wizard.md
│       └── skills/event-templates/
│
├── seo-content-creator/                 # SEO Articles
│   └── .claude/
│       ├── agents/seo-wizard.md
│       └── skills/
│           ├── seo-knowledge/
│           └── vk-cloud-security-expert/
│
├── landing-creator/                     # Landing Pages (Create)
│   └── .claude/
│       ├── agents/landing-content-creator.md
│       └── skills/landing-knowledge/
│
├── landing-updater/                     # Landing Pages (Update)
│   └── .claude/
│       ├── agents/landing-updater-wizard.md
│       └── skills/landing-knowledge/
│
├── vk-cloud-docs-agent/                 # VK Cloud Documentation
│   └── .claude/
│       ├── agents/vk-cloud-docs-writer.md
│       └── skills/vk-cloud-knowledge/
│
├── content-hub/                         # Централизованное хранилище
│   ├── columns/
│   ├── tech-articles/
│   ├── seo-articles/
│   ├── landings/
│   ├── events/
│   ├── press-releases/
│   ├── research/
│   └── vk-cloud-articles/
│
├── prompts/                             # Standalone YAML
├── articles/                            # Examples
└── README.md
```

---

## Статистика

| Метрика | Значение |
|---------|----------|
| Агентов | 12 |
| Команд | 10 |
| Skills | 26+ |
| Изданий (Columnist) | 14 |
| Модулей | 11 |

---

## Лицензия

MIT

---

**Автор:** [levashove](https://github.com/levashove)
