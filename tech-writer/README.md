# Tech Writer

Профессиональное написание технического контента для ведущих бизнес и технологических изданий на русском и английском языках.

## Что делает

- Opinion pieces и thought leadership статьи
- Технические туториалы и how-to guides
- Case studies и success stories
- Trend analysis и market commentary
- Research reports и whitepapers
- Билингвальное написание (RU/EN)

## Быстрый старт

```bash
/draft-article
```

Или с content brief:
```bash
/draft-article --brief=path/to/brief.md
```

## Агент

### Tech Content Writer

Старший технический писатель для высокотехнологичных компаний. Качество написания соответствует уровню контент-команд AWS, Azure, Google Cloud, OpenAI, Anthropic.

**Философия:**
- **Clarity above all** — сложные идеи объясняются просто
- **Show, don't tell** — конкретные примеры вместо абстракций
- **Narrative structure** — каждая статья рассказывает историю
- **Voice authenticity** — пишем как эксперт, не как продавец

## Skills

### enterprise-storytelling

Корпоративное повествование для B2B контента:
- Narrative arc для технического контента
- Human element в B2B storytelling
- Четыре фреймворка: CSR, Contrarian, Journey, How-To
- Культурные особенности (RU vs EN)

### technical-writing-standards

Стандарты технического письма:
- The Three Cs: Clear, Concise, Correct
- Sentence construction и paragraph structure
- Technical terminology guidelines
- Code examples и API documentation
- Russian language standards

## Форматы статей

| Формат | Объём | Описание |
|--------|-------|----------|
| Opinion Piece | 800-1,200 слов | Сильная позиция с аргументацией |
| Technical Tutorial | 1,500-2,500 слов | Пошаговое руководство |
| Trend Analysis | 1,000-1,800 слов | Data-driven insights |
| Case Study | 1,200-2,000 слов | Challenge-Solution-Results |
| Whitepaper | 2,500-5,000 слов | Глубокое исследование |

## Структура плагина

```
tech-writer/
├── .claude/
│   ├── agents/
│   │   └── tech-content-writer.md
│   ├── commands/
│   │   └── draft-article.md
│   └── skills/
│       ├── enterprise-storytelling/
│       │   └── SKILL.md
│       └── technical-writing-standards/
│           └── SKILL.md
└── README.md
```

## Связанные плагины

- [trend-researcher](../trend-researcher/) — исследование трендов
- [content-editor](../content-editor/) — редактура и фактчек
- [seo-publisher](../seo-publisher/) — SEO и публикация

## Лицензия

MIT
