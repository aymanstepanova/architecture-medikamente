# DFD в формате PlantUML

Здесь лежат те же потоки, что и в `*.drawio` в каталоге [Task1](../), в виде исходников **PlantUML** для рендеринга в PNG/SVG или встраивания в документацию.

| Файл | Процесс |
|------|---------|
| [dfd-p1-scheduling.puml](dfd-p1-scheduling.puml) | P1 |
| [dfd-p2-registration.puml](dfd-p2-registration.puml) | P2 |
| [dfd-p3-medical-record.puml](dfd-p3-medical-record.puml) | P3 |
| [dfd-p4-payment.puml](dfd-p4-payment.puml) | P4 |
| [dfd-p5-accounting.puml](dfd-p5-accounting.puml) | P5 |
| [dfd-p6-warehouse.puml](dfd-p6-warehouse.puml) | P6 |
| [dfd-p7-laboratory.puml](dfd-p7-laboratory.puml) | P7 |
| [dfd-p8-exchange.puml](dfd-p8-exchange.puml) | P8 |
| [dfd-analytics-as-is.puml](dfd-analytics-as-is.puml) | Аналитика As-Is (Task 1, PRV-010) |
| [_dfd-style.puml](_dfd-style.puml) | Общие `skinparam` (подключается через `!include`) |

**Как отрисовать**

- [Онлайн-сервер PlantUML](https://www.plantuml.com/plantuml/uml/) — вставить текст `.puml`.
- **Расширение VS Code** (или другого редактора) **PlantUML:** превью по `Alt+D` или из палитры команд.
- **CLI:** при установленном [PlantUML](https://plantuml.com/starting) и Graphviz:  
  `plantuml -tpng dfd-p1-scheduling.puml`

Красные стрелки (`#B85450`) соответствуют чувствительным потокам ПДн / проблемным зонам, как на draw.io.
