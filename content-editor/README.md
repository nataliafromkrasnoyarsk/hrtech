# Content Editor

Профессиональная редактура и проверка фактов для технического контента. Два специализированных агента: фактчекер и редактор.

## Что делает

### Fact-Checker
- Проверка статистики и технических утверждений
- Валидация источников по иерархии Tier 1-4
- Тестирование примеров кода
- Верификация цитат

### Content Editor
- Структурное редактирование (macro-level)
- Paragraph и sentence-level refinement
- Language precision и clarity enhancement
- Readability optimization
- Адаптация под конкретные издания

## Агенты

### Tech Fact-Checker

Специалист по проверке фактов с журналистскими стандартами точности. Трёхуровневая модель верификации.

**Что проверяет:**
- Statistical claims (источник, актуальность, контекст)
- Technical assertions (accuracy, completeness)
- Code examples (работоспособность, best practices)
- Quotes and attributions

### Content Editor

Главный редактор для технического контента. Качество редактуры соответствует Forbes, HBR, TechCrunch, Ведомости.

**Уровни редактирования:**
1. Structural editing — организация и flow
2. Paragraph editing — логика и связность
3. Sentence editing — ясность и сила
4. Word-level — точность и стиль

## Skills

### fact-checking-methodology

Rigorous fact-checking methodology:
- Three-layer verification model
- Source hierarchy (Tier 1-4)
- Verification checklists
- Common fact-checking scenarios
- Tools and techniques

### editorial-excellence

Advanced editorial techniques:
- The editorial process
- Common content problems and fixes
- Editorial standards by publication type
- Russian vs English considerations
- Giving editorial feedback

## Иерархия источников

| Tier | Источники | Надёжность |
|------|-----------|------------|
| Tier 1 | Официальная документация, peer-reviewed | Высшая |
| Tier 2 | Аналитики (Gartner, IDC), официальные блоги | Высокая |
| Tier 3 | Tech media, industry reports | Средняя |
| Tier 4 | Блоги, форумы, соцсети | Требует верификации |

## Структура плагина

```
content-editor/
├── .claude/
│   ├── agents/
│   │   ├── tech-fact-checker.md
│   │   └── content-editor.md
│   └── skills/
│       ├── fact-checking-methodology/
│       │   └── SKILL.md
│       └── editorial-excellence/
│           └── SKILL.md
└── README.md
```

## Связанные плагины

- [trend-researcher](../trend-researcher/) — исследование трендов
- [tech-writer](../tech-writer/) — написание статей
- [seo-publisher](../seo-publisher/) — SEO и публикация

## Лицензия

MIT
