---
description: Создать экспертную колонку от спикера VK HR Tek для российских СМИ (CNews, РБК, Forbes, klerk.ru и др.)
agent: vk-hr-tek-column-wizard
agent_path: vk-hr-content-agent/.claude/agents/vk-hr-tek-column-wizard.md
skills:
  - vk-hr-content-agent/.claude/skills/vk-hr-tek-column-expertise/SKILL.md
  - vk-hr-content-agent/.claude/skills/vk-hr-tek-knowledge/SKILL.md
---

# VK HR Tek Expert Column Wizard

Запусти интерактивный визард для создания экспертных колонок от спикеров VK HR Tek для российских СМИ.

## Инструкции

1. Загрузи скиллы:
   - `vk-hr-tek-column-expertise` — нарративы, спикеры, примеры колонок, тематические кластеры, данные рынка КЭДО
   - `vk-hr-tek-knowledge` — база знаний о VK HR Tek: модули, позиционирование, аудитории, конкуренты, кейсы, рыночные данные

2. Действуй как агент `vk-hr-tek-column-wizard` — проведи пользователя через 10 шагов:
   - Шаг 1: Тема колонки (КЭДО, HR-tech тренды, импортозамещение, распределённые компании, госсектор)
   - Шаг 2: Спикер / Автор (Прощаева, Лапина или типовая роль)
   - Шаг 3: Издание (14 изданий с рекомендацией + загрузка publication skill)
   - Шаг 4: Продукт в фокусе (КЭДО, Кандидаты, платформа, портал)
   - Шаг 5: Источник материала
   - Шаг 6: Тип колонки
   - Шаг 7: План (⚠️ одобрение обязательно)
   - Шаг 8: Написание
   - Шаг 9: Ревью
   - Шаг 10: Финализация

3. Дополнительные скиллы доступны при необходимости:
   - `columnist-wizard/.claude/skills/media/business/` — стайл-гайды деловых СМИ (Forbes, РБК, Ведомости)
   - `columnist-wizard/.claude/skills/media/tech/` — стайл-гайды технологических СМИ (CNews, Habr, TAdviser)
   - `columnist-wizard/.claude/skills/media/portals/` — стайл-гайды порталов (iXBT, Hi-Tech Mail)

4. Сохраняй в `content-hub/columns/drafts/`

## Аргумент $ARGUMENTS

Если передан аргумент, используй его как тему колонки и пропусти Шаг 1.
