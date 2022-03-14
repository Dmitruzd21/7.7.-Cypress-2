[![7.7. Cypress 2](https://img.shields.io/endpoint?url=https://dashboard.cypress.io/badge/simple/46f622&style=flat&logo=cypress)](https://dashboard.cypress.io/projects/46f622/runs)
[![7.7. Cypress 2](https://img.shields.io/endpoint?url=https://dashboard.cypress.io/badge/detailed/46f622&style=flat&logo=cypress)](https://dashboard.cypress.io/projects/46f622/runs)
[![7.7. Cypress 2](https://img.shields.io/endpoint?url=https://dashboard.cypress.io/badge/count/46f622&style=flat&logo=cypress)](https://dashboard.cypress.io/projects/46f622/runs)

**Доступ к dashboard**

Ссылка на последний запуск: https://dashboard.cypress.io/projects/46f622/runs/3

Ссылка на проект:
https://dashboard.cypress.io/projects/46f622

https://dashboard.cypress.io/projects/46f622/runs?branches=%5B%5D&committers=%5B%5D&flaky=%5B%5D&page=1&status=%5B%5D&tags=%5B%5D&timeRange=%7B%22startDate%22%3A%221970-01-01%22%2C%22endDate%22%3A%222038-01-19%22%7D

projectId: "46f622"

Примечание1:
hook after падал, поскольку пытался удалять залы, которые уже были удалены.
Падение хука расценивалось как падение тестов.
Вероятно хук выполнялся не в самом конце, а после каждого теста.

Примечание2: хук after по удалению залов будет несколько иным, если будет исправлен баг по перемещению фильма на ленту времени зала (для этого необходимо дополнительно приостановить продажу). Пока для демонтрации того, что хук в целом работает описал более простое поведение, которое учитывает баг.

Примечание3: метод foreach в идеале в тесте должен быть одним: создание зала, настрока, открытие продаж. Но, учитывая баг, для демонстрации того, что метод foreach хорошо работает с фикстурами сделал отдельный foreach для добавления зала (без настроек)
