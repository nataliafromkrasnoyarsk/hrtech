# Content Hub

Централизованное хранилище всех материалов, создаваемых агентами.

## Структура

```
content-hub/
├── columns/              # Columnist Wizard
│   ├── drafts/           # Черновики колонок
│   └── published/        # Опубликованные колонки
│
├── seo-articles/         # SEO Wizard
│   ├── drafts/           # Черновики SEO-статей
│   └── published/        # Опубликованные статьи
│
├── tech-articles/        # Tech Content Writer
│   ├── drafts/           # Черновики технических статей
│   └── published/        # Опубликованные статьи
│
├── landings/             # Landing Content Creator
│   ├── drafts/           # Черновики лендингов
│   └── published/        # Готовые лендинги
│
├── events/               # Event Wizard
│   ├── drafts/           # Черновики страниц мероприятий
│   └── published/        # Опубликованные страницы
│
├── press-releases/       # Press Release Wizard
│   ├── drafts/           # Черновики пресс-релизов
│   └── published/        # Опубликованные пресс-релизы
│
├── research/             # Tech Content Strategist
│   ├── drafts/           # Черновики исследований
│   └── published/        # Финальные отчёты
│
└── vk-cloud-articles/    # VK Cloud Docs Writer
    ├── drafts/           # Черновики статей о VK Cloud
    └── published/        # Опубликованные статьи
```

## Агенты и категории

| Агент | Категория | Описание |
|-------|-----------|----------|
| **Columnist Wizard** | `columns/` | Экспертные колонки для Forbes, RBC, Habr и др. |
| **SEO Wizard** | `seo-articles/` | SEO-оптимизированные статьи |
| **Tech Content Writer** | `tech-articles/` | Технические статьи и thought leadership |
| **Landing Content Creator** | `landings/` | Контент для лендингов |
| **Event Wizard** | `events/` | Страницы мероприятий |
| **Press Release Wizard** | `press-releases/` | Пресс-релизы |
| **Tech Content Strategist** | `research/` | Исследования трендов и идеи контента |
| **VK Cloud Docs Writer** | `vk-cloud-articles/` | Технические статьи о сервисах VK Cloud |

## Workflow

1. **Создание** - агент сохраняет материал в `{категория}/drafts/`
2. **Редактура** - используйте Content Editor для доработки
3. **Проверка** - используйте Tech Fact-Checker для верификации
4. **SEO** - используйте SEO Content Optimizer для оптимизации
5. **Публикация** - переместите в `{категория}/published/`

## Именование файлов

Рекомендуемый формат: `{YYYY-MM-DD}-{slug}.md`

Примеры:
- `2026-01-27-cloud-security-trends.md`
- `2026-01-27-forbes-ai-governance.md`
- `2026-01-27-vk-cloud-conf.md`

## Вспомогательные агенты

Эти агенты не создают новый контент, но помогают с существующим:

| Агент | Функция |
|-------|---------|
| **Content Editor** | Редактура и улучшение текста |
| **Tech Fact-Checker** | Проверка фактов и источников |
| **SEO Content Optimizer** | SEO-оптимизация |
| **Landing Updater Wizard** | Обновление существующих лендингов |
