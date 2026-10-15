# Навчальний проєкт «Нова пошта»

**Дисципліна:** Архітектура програмного забезпечення

**Автор:** Рудяк Богдан Миколайович

**Заклад освіти:** IT STEP University, магістратура «Комп'ютерні науки»

## Про проєкт

Репозиторій містить архітектурну документацію навчальної системи доставки відправлень, створеної за прикладом служби «Нова пошта». Система дозволяє клієнтам оформлювати й оплачувати відправлення та відстежувати посилки. Персонал через неї приймає, сортує та видає посилки, кур'єри виконують доставку, а бізнес-клієнти інтегрують свої CRM та інтернет-магазини через API.

Запропонована архітектура складається з вебзастосунку (React / TypeScript), мобільного застосунку (iOS / Android), одного Backend API (Node.js / REST), бази даних PostgreSQL та окремого Notification Worker для надійного надсилання сповіщень.

## Навігація

| Завдання | Зміст | Документ |
|---|---|---|
| ДЗ-1 | Актори, обмеження, unhappy paths, функціональні та нефункціональні вимоги | [requirements.md](docs/homework-1/requirements.md) |
| ДЗ-2 | C4-модель системи: рівні 1–3 з поясненнями | [c4-explanations.md](docs/homework-2/c4-explanations.md) |
| ДЗ-3 | Architecture Decision Records | [ADR-001](docs/homework-3/ADR-001.md), [ADR-002](docs/homework-3/ADR-002.md), [ADR-003](docs/homework-3/ADR-003.md) |

### ДЗ-1. Вимоги

[docs/homework-1/requirements.md](docs/homework-1/requirements.md)

1. Actors — основні та допоміжні актори системи.
2. Constraints — законодавчі, бізнесові, технічні та операційні обмеження з прив'язкою до компонентів.
3. Unhappy paths — проблемні сценарії, зокрема 10 архітектурних (конкурентні зміни, повторні запити, збої мережі та зовнішніх сервісів).
4. Functional requirements — функціональні вимоги.
5. Non-functional requirements — вимірювані нефункціональні вимоги з умовами перевірки.

### ДЗ-2. C4-модель

[docs/homework-2/c4-explanations.md](docs/homework-2/c4-explanations.md) — пояснення всіх трьох рівнів разом із діаграмами.

Редагований файл діаграм: [docs/homework-2/C4_1-3_Levels.drawio](docs/homework-2/C4_1-3_Levels.drawio).

**Level 1 — System Context**

![C4 Level 1](docs/homework-2/previews/Level_1.png)

**Level 2 — Container Diagram**

![C4 Level 2](docs/homework-2/previews/Level_2.png)

**Level 3 — Component Diagram**

![C4 Level 3](docs/homework-2/previews/Level_3.png)

### ДЗ-3. Architecture Decision Records

1. [ADR-001 — Зберігання поточного статусу посилки разом з історією змін](docs/homework-3/ADR-001.md)
2. [ADR-002 — Контроль переходів статусів та захист від одночасних змін](docs/homework-3/ADR-002.md)
3. [ADR-003 — Надійне асинхронне надсилання сповіщень через Notification Worker](docs/homework-3/ADR-003.md)

## Як відкрити Draw.io-файл

Файл [C4_1-3_Levels.drawio](docs/homework-2/C4_1-3_Levels.drawio) містить три вкладки — Level 1, Level 2 і Level 3.

**Варіант 1. У браузері**

1. Завантажте файл: відкрийте його на GitHub і натисніть «Download raw file».
2. Перейдіть на [app.diagrams.net](https://app.diagrams.net).
3. Виберіть «File → Open from → Device» і вкажіть завантажений файл.

**Варіант 2. Без завантаження**

На [app.diagrams.net](https://app.diagrams.net) виберіть «File → Open from → URL» і вставте посилання на raw-версію файлу:

```text
https://raw.githubusercontent.com/BodiaRudiak/Nova_Poshta-Rudiak_Bohdan/main/docs/homework-2/C4_1-3_Levels.drawio
```

**Варіант 3. Локально**

Відкрийте файл у застосунку [draw.io Desktop](https://github.com/jgraph/drawio-desktop/releases) або в VS Code з розширенням «Draw.io Integration».

Між рівнями перемикаються вкладками внизу вікна.

## Структура репозиторію

```text
Nova_Poshta-Rudiak_Bohdan/
├── README.md
└── docs/
    ├── homework-1/
    │   └── requirements.md
    ├── homework-2/
    │   ├── c4-explanations.md
    │   ├── C4_1-3_Levels.drawio
    │   └── previews/
    │       ├── Level_1.png
    │       ├── Level_2.png
    │       └── Level_3.png
    └── homework-3/
        ├── ADR-001.md
        ├── ADR-002.md
        └── ADR-003.md
```
