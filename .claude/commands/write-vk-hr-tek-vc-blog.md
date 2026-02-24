---
description: Создать материал о VK HR Tek для блога VK Tech на VC.ru (кейс, мнение, гайд, тренд-разбор, сравнение)
agent: vk-hr-tek-vc-blog-wizard
agent_path: vk-hr-content-agent/.claude/agents/vk-hr-tek-vc-blog-wizard.md
skills:
  - vk-hr-content-agent/.claude/skills/vk-hr-tek-vc-blog-expertise/SKILL.md
  - vk-hr-content-agent/.claude/skills/vk-hr-tek-knowledge/SKILL.md
---

# VK HR Tek VC.ru Blog Wizard

Запусти интерактивный визард для создания контента о VK HR Tek для блога VK Tech на VC.ru.

## Инструкции

1. Загрузи скиллы:
   - `vk-hr-tek-vc-blog-expertise` — редполитика, форматы контента, алгоритм VC.ru, шаблоны, антипаттерны, примеры успешных постов
   - `vk-hr-tek-knowledge` — база знаний о VK HR Tek: модули, позиционирование, аудитории, конкуренты, кейсы, рыночные данные

2. Действуй как агент `vk-hr-tek-vc-blog-wizard` — проведи пользователя через 10 шагов:
   - Шаг 1: Формат материала (кейс, мнение, гайд, тренд-разбор, сравнение, разбор законодательства)
   - Шаг 2: Тема и угол
   - Шаг 3: Продукт VK HR Tek в фокусе
   - Шаг 4: Аудитория и автор
   - Шаг 5: Источник материала
   - Шаг 6: Заголовок + лид (3 варианта)
   - Шаг 7: План (⚠️ одобрение обязательно)
   - Шаг 8: Написание
   - Шаг 9: Ревью
   - Шаг 10: Финализация

3. Дополнительные скиллы доступны при необходимости:
   - `columnist-wizard/.claude/skills/media/tech/vc-ru.md` — стайл-гайд VC.ru
   - `columnist-wizard/.claude/skills/examples/vc-ru-examples.md` — примеры успешных статей

4. Сохраняй в `content-hub/vc-ru-blog/drafts/`

## Аргумент $ARGUMENTS

Если передан аргумент, используй его как тему материала и пропусти Шаг 2.
