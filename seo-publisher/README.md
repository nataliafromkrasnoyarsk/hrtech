# SEO Publisher

SEO-оптимизация и подготовка контента к публикации в ведущих бизнес и технологических изданиях.

## Что делает

- Оптимизация заголовков и A/B варианты
- Создание мета-описаний
- Стратегия ключевых слов
- Улучшение читаемости и сканируемости
- Оптимизация для соцсетей
- Планирование дистрибуции
- Оркестрация полного workflow создания статьи

## Быстрый старт

### Полный workflow
```bash
/article-workflow
```

Проводит через все этапы: Research → Ideation → Draft → Fact-check → Edit → SEO.

## Агент

### SEO Content Optimizer

SEO и контент-оптимизатор для технического thought leadership. Обеспечивает максимальную discoverability без потери редакторского качества.

**Философия:**
- Reader-first optimization — SEO помогает читателям находить ценный контент
- Editorial integrity — никаких компромиссов с качеством ради SEO
- Platform awareness — разные платформы требуют разных подходов

**Возможности:**
- Headline optimization и A/B variants
- Meta description creation
- Keyword strategy и placement
- Social media optimization
- Distribution strategy planning

## Skill: media-publishing-guidelines

Comprehensive guidelines для публикации в топовых медиа:

### Глобальные издания
- **Forbes** — Executive audience, business impact focus
- **Harvard Business Review** — Research-backed insights
- **TechCrunch** — Innovation and product focus
- **Wired** — Deep-dive technology and culture

### Российские издания
- **Ведомости** — Business leaders, formal tone
- **РБК** — Market analysis, professional audience
- **Хабр** — Technical community, deep-dive tutorials
- **VC.ru** — Startup ecosystem, business model analysis

### Содержание skill
- Publication landscape overview (Tier 1-4 outlets)
- Publication-specific requirements
- Pitching to editors
- Editorial relationships building
- Legal and ethical considerations

## Workflow команда

`/article-workflow` оркестрирует все плагины:

```
┌─────────────────────────────────────────────────────────────┐
│  1. RESEARCH          trend-researcher                      │
│     Исследование трендов и выбор темы                       │
├─────────────────────────────────────────────────────────────┤
│  2. DRAFT             tech-writer                           │
│     Написание черновика статьи                              │
├─────────────────────────────────────────────────────────────┤
│  3. FACT-CHECK        content-editor (fact-checker)         │
│     Проверка фактов и утверждений                           │
├─────────────────────────────────────────────────────────────┤
│  4. EDIT              content-editor (editor)               │
│     Редактура и улучшение текста                            │
├─────────────────────────────────────────────────────────────┤
│  5. SEO               seo-publisher                         │
│     SEO-оптимизация и подготовка к публикации               │
└─────────────────────────────────────────────────────────────┘
```

## Структура плагина

```
seo-publisher/
├── .claude/
│   ├── agents/
│   │   └── seo-content-optimizer.md
│   ├── commands/
│   │   └── article-workflow.md
│   └── skills/
│       └── media-publishing-guidelines/
│           └── SKILL.md
└── README.md
```

## Связанные плагины

- [trend-researcher](../trend-researcher/) — исследование трендов
- [tech-writer](../tech-writer/) — написание статей
- [content-editor](../content-editor/) — редактура и фактчек

## Лицензия

MIT
