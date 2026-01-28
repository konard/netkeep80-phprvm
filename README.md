# phprvm — PHP Relations (Model) Virtual Machine

[English](#english) | [Русский](#russian)

```
            R
         S__|__O
       O   _|_   S     Fractal
    R__|__/_|_\__|__R  Triune
       |  \_|_/  |     Entity
       S    |    O
          __|__
         /  |  \
        /___|___\
```

---

<a name="english"></a>
## English

### Overview

**phprvm** is an experimental implementation of the **Relations Model** (RM) — a meta-programming language based on the concept of triune entities. Unlike traditional programming languages that use linear text representation, the Relations Model represents programs as an interconnected set of entities.

### Key Concepts

Each **entity** in the Relations Model is defined by three other entities:
- **Subject** — where the result is projected (view/representation)
- **Relation** — the controller/algorithm of transformation
- **Object** — what is being projected (model/data)

This creates a **triune structure** that implements the MVC pattern at the entity level.

### Features

- Web-based entity editor and viewer
- Tree and table views of entity hierarchies
- Built-in PHP-based virtual machine (`PHPExec`)
- Debug mode for tracing entity execution
- AJAX API for CRUD operations
- XML import/export support

### Documentation

- **[Analysis (Russian)](analysis.md)** — Detailed analysis of the project's current state, strengths, and weaknesses
- **[Development Plan (Russian)](plan.md)** — Roadmap with multiple development directions and prioritized tasks

### Requirements

- PHP 5.6+ (requires updates for PHP 7+)
- MySQL 5.5+
- Web server (Apache/Nginx)

### Installation

1. Clone the repository
2. Import `rmodel.sql` into MySQL
3. Configure database connection in `public_html/includes/project_config.php`
4. Point your web server to `public_html/`

### Project Structure

```
public_html/
├── includes/
│   ├── classes/        # PHP classes
│   │   ├── Rmodel/     # Core RM implementation
│   │   ├── DB/         # Database layer
│   │   └── Utils/      # Utilities
│   └── Core.php        # Application bootstrap
├── Entity_*.php        # Entity manipulation pages
├── rmodel_*.php        # Model view pages
├── axcall.php          # AJAX API endpoint
└── index.php           # Main page
```

---

<a name="russian"></a>
## Русский

### Обзор

**phprvm** — экспериментальная реализация **Модели Отношений** (МО) — языка метапрограммирования, основанного на концепции триединых сущностей. В отличие от традиционных языков программирования, использующих линейно-текстовое представление, Модель Отношений представляет программу в виде взаимосвязанного множества сущностей.

### Основные концепции

Каждая **сущность** в Модели Отношений определяется тремя другими сущностями:
- **Субъект (Subject)** — куда проецируется результат (представление)
- **Отношение (Relation)** — контроллер/алгоритм преобразования
- **Объект (Object)** — что проецируется (модель/данные)

Это создаёт **триединую структуру**, реализующую паттерн MVC на уровне каждой сущности.

### Возможности

- Веб-редактор и просмотрщик сущностей
- Древовидное и табличное представление иерархий
- Встроенная виртуальная машина на PHP (`PHPExec`)
- Режим отладки для трассировки исполнения
- AJAX API для CRUD-операций
- Поддержка импорта/экспорта в XML

### Документация

- **[Анализ проекта](analysis.md)** — Подробный анализ текущего состояния, сильных и слабых сторон проекта
- **[План развития](plan.md)** — Дорожная карта с несколькими направлениями развития и приоритизированными задачами

### Требования

- PHP 5.6+ (требует обновлений для PHP 7+)
- MySQL 5.5+
- Веб-сервер (Apache/Nginx)

### Установка

1. Клонируйте репозиторий
2. Импортируйте `rmodel.sql` в MySQL
3. Настройте подключение к БД в `public_html/includes/project_config.php`
4. Направьте веб-сервер на папку `public_html/`

### Теоретическая основа

Модель Отношений — это язык метапрограммирования, в основе которого лежит единая концепция **триединой сущности**:

- В МО одновременно присутствуют три иерархии: агрегирования (субъект), типов (отношение), использования (объект)
- Пространство МО является нульмерным — отношения порядка определяются явно в модели
- Сущность можно либо **прочитать** (спроецировать), либо **исполнить** (активировать)
- Сохранение состояния обеспечивается самоотображением сущности в саму себя

Подробное теоретическое описание доступно в сущности 10000 через веб-интерфейс.

---

## License / Лицензия

<img align="right" src="https://opensource.org/trademarks/opensource/OSI-Approved-License-100x137.png">

The project is licensed under the [MIT License](https://opensource.org/licenses/MIT):

Copyright &copy; 2016-2021 [Vertushkin Roman Pavlovich](https://vk.com/earthbirthbook)

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.

## Thanks / Благодарности

I deeply appreciate the help of the following people. / Выражаю глубокую благодарность следующим людям:

- [Sergio] — helped to develop some classes / помог в разработке некоторых классов
