---
type: doc
status: active
created: 2026-01-14
updated: 2026-01-14
family: F0
scope: repository
---

# 0.5. AI Reports

Автоматические AI-проверки и отчёты по состоянию хранилища.

## Содержимое

| Папка | Описание |
|-------|----------|
| [Validation-Specs/](Validation-Specs/) | Технические задания на автоматические проверки |
| [Validation-Results/](Validation-Results/) | Результаты выполненных проверок |

## Расписание проверок

| Проверка | Расписание | Режим |
|----------|------------|-------|
| Формальная проверка | Воскресенье, 9:00 | Авто / Ручной |
| Содержательная проверка | Воскресенье, 9:00 | Авто / Ручной |
| Анализ развития | Воскресенье, 9:00 | Авто / Ручной |

## Как запустить проверку вручную

```
/validate formal     # Формальная проверка
/validate content    # Содержательная проверка
/validate develop    # Анализ предложений по развитию
/validate all        # Все проверки
```

## Структура результатов

Результаты проверок сохраняются в `Validation-Results/` с именем:

```
{YYYY-MM-DD}-{тип-проверки}.md
```

Например:
- `2026-01-14-formal.md`
- `2026-01-14-content.md`
- `2026-01-14-develop.md`

## Формат отчёта

```markdown
# [Тип отчёта]

**Дата:** YYYY-MM-DD
**Сгенерировано:** Claude Code

## Резюме

[Краткие выводы]

## Детали

[Подробный анализ]

## Рекомендации

- [ ] Рекомендация 1
- [ ] Рекомендация 2
```

## Спецификации проверок

- [Validation-Specs/01-formal-checks.md](Validation-Specs/01-formal-checks.md) — формальные проверки
- [Validation-Specs/02-content-checks.md](Validation-Specs/02-content-checks.md) — содержательные проверки
- [Validation-Specs/03-development-analysis.md](Validation-Specs/03-development-analysis.md) — анализ развития
