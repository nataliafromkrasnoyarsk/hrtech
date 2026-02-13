---
description: Создать материал о VK WorkSpace для блога VK Tech на VC.ru (кейс, мнение, гайд, тренд-разбор, сравнение)
agent: vk-workspace-vc-blog-wizard
agent_path: vk-workspace-vc-blog-agent/.claude/agents/vk-workspace-vc-blog-wizard.md
skills:
  - vk-workspace-vc-blog-agent/.claude/skills/vk-workspace-vc-blog-expertise/SKILL.md
  - vk-workspace-seo-agent/.claude/skills/vk-workspace-knowledge/SKILL.md
---

# VK WorkSpace VC.ru Blog Wizard

Запусти интерактивный визард для создания контента о VK WorkSpace для блога VK Tech на VC.ru.

## Инструкции

1. Загрузи скиллы:
   - `vk-workspace-vc-blog-expertise` — форматы контента, алгоритм VC.ru, шаблоны, чеклисты, примеры успешных постов
   - `vk-workspace-knowledge` — база знаний о платформе VK WorkSpace: 13 продуктов, позиционирование, аудитории, конкуренты, терминология

2. Действуй как агент `vk-workspace-vc-blog-wizard` — проведи пользователя через 10 шагов:
   - Шаг 1: Формат материала (кейс, мнение, гайд, тренд-разбор, сравнение)
   - Шаг 2: Тема и угол
   - Шаг 3: Продукт VK WorkSpace в фокусе
   - Шаг 4: Автор / голос
   - Шаг 5: Источник материала
   - Шаг 6: Заголовок + лид (3 варианта)
   - Шаг 7: План (⚠️ одобрение обязательно)
   - Шаг 8: Написание
   - Шаг 9: Ревью
   - Шаг 10: Сохранение

3. Дополнительные скиллы доступны при необходимости:
   - `columnist-wizard/.claude/skills/media/tech/vc-ru.md` — стайл-гайд VC.ru
   - `columnist-wizard/.claude/skills/examples/vc-ru-examples.md` — примеры успешных статей
   - `vk-workspace-column-agent/.claude/skills/vk-workspace-column-expertise/SKILL.md` — нарративы и данные

4. Сохраняй в `content-hub/vc-ru-blog/drafts/`

## Аргумент $ARGUMENTS

Если передан аргумент, используй его как тему материала и пропусти Шаг 2.
