# Task 1 — Анализ безопасности системы (As-Is)

## Итоговые артефакты

- **Список проблем компании** в разрезе работы с данными.
- **Диаграммы потоков данных** (DFD).

## Состав каталога

| Файл | Назначение                                                                                                                                            |
|------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [data-privacy-problems-and-dfd-index.md](data-privacy-problems-and-dfd-index.md) | **Основной артефакт:** резюме, таблица проблем **PRV-001…PRV-010** с трассировкой к процессам P* и категориям данных, вопросы к DPO, связь с Task 2–6 |
| [dfd-p1-scheduling.drawio](dfd-p1-scheduling.drawio) | DFD **P1** — запись на приём, Journals / Journal-Doctor-FIO                                                                                           |
| [dfd-p2-registration.drawio](dfd-p2-registration.drawio) | DFD **P2** — регистрация, Patients.xlsx, Patients                                                                                                     |
| [dfd-p3-medical-record.drawio](dfd-p3-medical-record.drawio) | DFD **P3** — дело пациента, подпапки и сканы                                                                                                          |
| [dfd-p4-payment.drawio](dfd-p4-payment.drawio) | DFD **P4** — оплата, **ККМ** (контрольно-кассовая машина), 1С, **теневой Excel** (двойной учёт)                                                       |
| [dfd-p5-accounting.drawio](dfd-p5-accounting.drawio) | DFD **P5** — бухгалтерия и кадры в 1С:Бухгалтерия                                                                                                     |
| [dfd-p6-warehouse.drawio](dfd-p6-warehouse.drawio) | DFD **P6** — ТМЦ, обмен 1С <->1С (OLE)                                                                                                                |
| [dfd-p7-laboratory.drawio](dfd-p7-laboratory.drawio) | DFD **P7** — лаборатория, **неформализованный** поток от внешней Lab                                                                                  |
| [dfd-p8-exchange.drawio](dfd-p8-exchange.drawio) | DFD **P8** — Exchange как канал ПДн                                                                                                                   |
| [dfd-analytics-as-is.drawio](dfd-analytics-as-is.drawio) | DFD **аналитический контур As-Is**, Jupyter по Excel с FileServer (PRV-010)                                                                           |
| [dfd-analytics-to-be.drawio](dfd-analytics-to-be.drawio) | DFD **аналитический контур To-Be**: явный **Classification Engine**, Data Lake, DLP, аудит, шифрование, RLS/маскирование |

**Те же DFD в PlantUML:** каталог [plantuml/](plantuml/) — исходники `.puml`, общий стиль `_dfd-style.puml`, см. [plantuml/README.md](plantuml/README.md). Формулировки **`title`** и подписей потоков в `.puml` — эталон; в [dfd-drawio-title-recommendations.md](dfd-drawio-title-recommendations.md) описано выравнивание с `*.drawio`.

Диаграммы **draw.io** открываются в [diagrams.net](https://app.diagrams.net/) или в VS Code с расширением draw.io. **PlantUML** — превью в IDE или рендер через [plantuml.com](https://www.plantuml.com/plantuml/uml/).

## Как читать DFD

- Процессы **P1–P8** заданы в [data-privacy-problems-and-dfd-index.md](data-privacy-problems-and-dfd-index.md) и в DFD этого каталога.
- На схемах **красным** выделены подписи потоков с **ПДн/чувствительными медданными** или **проблемные/теневые** потоки (двойной учёт, ручной лабораторный контур).
- Дополнительная DFD по аналитике не заменяет P1–P8, а фиксирует отдельный риск **PRV-010** для согласования с Task 6.
- В To-Be DFD для аналитики добавлены технические меры: **Classification Engine** (rules + ML), **Policy & Tag Catalog**, **DLP**, централизованный **SIEM/audit**, шифрование и доступ по ролям.

## Рекомендации по выполнению

- Процессы для отдельных DFD: см. описание P1–P8 в [data-privacy-problems-and-dfd-index.md](data-privacy-problems-and-dfd-index.md).
- Нотация: [гайд Lucidchart по DFD](https://www.lucidchart.com/pages/data-flow-diagram).

## Дополнительно (по желанию)

- Доработанные DFD с мерами на этапах потока.
- Аудит мер по безопасности данных.
- Матрица: данные × шифрование / обфускация / обезличивание.
- Механизм тегирования и список инструментов для конфиденциальности в потоках.
