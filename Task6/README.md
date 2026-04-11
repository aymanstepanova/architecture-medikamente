# Task 6 — Классификация данных (движок перед загрузкой в хранилище)

## Итоговые артефакты

- Диаграмма **C2** (уровень контейнеров в **C4**) решения — **движка**, реализующего **классификацию данных перед загрузкой** их в хранилище.

## Состав каталога

| Файл | Содержание |
|------|------------|
| [c2-classification-engine.drawio](c2-classification-engine.drawio) | **C4 Containers:** Ingestion API, Classification core, Policy & Tag Catalog, message bus, workers, trusted loader, PostgreSQL, метрики; внешние платформа и **ClickHouse DWH** |
| [c2-classification-engine.md](c2-classification-engine.md) | Роли контейнеров, слои **Bronze/Silver/Gold**, метрики, масштабирование, связь с Task 2–3 и 5 |

Согласование с Task 2: [Task2/c4-context-and-mvp.md](../Task2/c4-context-and-mvp.md).

## Дополнительно

- Слои/зоны хранилища для чувствительных данных — **раздел 3** в [c2-classification-engine.md](c2-classification-engine.md).
- Метрики эффективности классификации и оптимизация — **раздел 4**.
- Масштабируемость при росте объёма данных и числа пользователей — **раздел 5**.
