# Task 5 — Cutover-план миграции

## Итоговые артефакты

- **Обоснование** выбора стратегии миграции.
- **Чётко структурированный cutover-план**.
- Описание **мер по управлению рисками**.

## Состав каталога

| Файл | Содержание |
|------|------------|
| [migration-strategy-cutover-and-risks.md](migration-strategy-cutover-and-risks.md) | Обоснование **phased + parallel run + strangler**; **таблица cutover** C0–C8; меры по рискам; rollback; связь с Task 1–4 и 6 |

Контекст монолита и процессов: [Task 1](../Task1/data-privacy-problems-and-dfd-index.md). Узкие места: [Task 4](../Task4/migration-ishikawa-notes.md).

## Формат cutover-плана

В основном документе использованы колонки: **Этап | Описание | Ключевые задачи | Ответственные | Время/сроки | Риски и меры**.

Стратегии: поэтапная миграция, параллельный прогон для финансов, strangler для постепенной подмены Legacy — см. раздел 1 в [migration-strategy-cutover-and-risks.md](migration-strategy-cutover-and-risks.md).
