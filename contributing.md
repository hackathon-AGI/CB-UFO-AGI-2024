# CB-UFO-AGI-2024

## Установка инструментов

Установите PDM, например, `sudo apt install python3-pdm`

Далее выполнитете в каталоге репозитория `pdm install`

Убедитесь, что постоянно находитесь в виртуальном окружении, чтоб перейти в него вручную выполните, например, `source .venv/Scripts/activate`

## Методология внедрения репозитория

Пожалуйста, не делайте много комитов, пусть дерево будет чистым

Пока коммидте в develop-<your_name>

## Структура проекта

* `/.mypy_cache", "/.pdm-build", "/.ruff_cache", "/.venv" - не хранятся в репозитории, временные файлы (не редактируются вручную)
* `/данные/внешние/<имя_источника>/<имя_набора данных>/` - не хранятся в хранилище, набор данных с именем `<имя_набора данных>` получен из внешнего ресурса `<имя_источника>'
* `/data/interim/<имя_набора данных>/` - не хранится в хранилище, набор данных с именем `<имя_набора данных>` получен во время предварительной обработки данных.
* `/данные/обработаны/<имя_набора данных>/` - не хранятся в хранилище, обработанный набор данных с именем `<имя_набора данных>`
* `/data/raw/<имя_набора данных>/` - не хранится в репозитории, внутренний набор необработанных данных с именем `<имя_набора данных>`
* `/dist/` - нет в репозитории, место хранения скомпилированных пакетов python
* `/docs/` - место хранения файлов документации .md и их ресурсов (commit использует `docs`)
* `/models/<имя_модели>/` - не хранится в репозитории, модель с именем `<имя_модели>`
* `/notebooks/` - папка для хранения записных книжек jupyter для исследований, ее содержимое используется для создания документации (commit использует `chore(notebooks)`)
* `/src/` - исходный код пакетов, новые файлы или папки добавлять не нужно.
* `/src/cb_ufo_agi_2024/` - исходный код, который будет встроен в библиотеку для производства, его содержимое используется для создания документации (commit использует различные типы коммитов)
* `/tests/` - тесты для исходного кода (commit использует `test`)
* `/.dockerignore`, `/.gitignore` - файлы исключений, должны быть идентичными (при фиксации используется `chore(ignore)`).
* `/contributing.md` - этот файл с вводным описанием проекта, его содержимое используется для создания документации (commit использует `docs`)
* `/LICENSE.txt` - лицензия, его содержимое используется для создания документации (commit использует `feat(лицензия)!`)
* `/pdm.lock` - зависимости проекта заморожены (не редактируются вручную)
* `/pyproject.toml` - настройки сборки проекта, компоновщики, зависимости и т.д. (commit использует различные типы коммитов)
* `/README.md` - файл описания проекта, его содержимое используется для создания документации (commit использует `docs`)
* `/requirements.dev.txt`, `requirements.txt` - зависимости в формате pip (не редактируются вручную)
* `docs/tasks.md` - задачи, которые нужно выполнить с подробностями и прогресс (commit использует `docs`)
* `docs/other.md` - весь остальной текст (commit использует `docs`)
