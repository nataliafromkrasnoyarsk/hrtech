---
description: Интерактивный визард для создания экспертных колонок от спикеров VK WorkSpace для российских СМИ
agent: vk-workspace-column-wizard
agent_path: vk-workspace-column-agent/.claude/agents/vk-workspace-column-wizard.md
skills:
  - vk-workspace-column-agent/.claude/skills/vk-workspace-column-expertise/SKILL.md
  - vk-workspace-seo-agent/.claude/skills/vk-workspace-knowledge/SKILL.md
---

# Expert Column Wizard — VK WorkSpace

Запусти интерактивный визард для создания экспертной колонки от спикера VK WorkSpace для российских деловых и технологических СМИ.

## Инструкции

1. Загрузи скиллы:
   - `vk-workspace-column-expertise` — нарративы, спикеры, примеры реальных колонок, тематические кластеры, данные исследований
   - `vk-workspace-knowledge` — база знаний о платформе VK WorkSpace: 13 продуктов, позиционирование, аудитории, конкуренты, терминология

2. Действуй как агент `vk-workspace-column-wizard` — проведи пользователя через 10 шагов:
   - Шаг 1: Тема колонки
   - Шаг 2: Спикер / Автор (только VK WorkSpace)
   - Шаг 3: Издание (14 СМИ + рекомендация)
   - Шаг 4: Продукт VK WorkSpace в фокусе
   - Шаг 5: Источник материала
   - Шаг 6: Тип колонки
   - Шаг 7: План (⚠️ одобрение обязательно)
   - Шаг 8: Написание
   - Шаг 9: Ревью
   - Шаг 10: Сохранение

3. При выборе издания загрузи publication skill из `columnist-wizard/.claude/skills/media/`

4. Сохраняй в `content-hub/columns/drafts/`

## Аргумент $ARGUMENTS

Если передан аргумент, используй его как тему колонки и пропусти Шаг 1.
