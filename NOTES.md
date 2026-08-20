# 📒 Мои заметки по автоматизации (JS/TS + Jest)

## ✅ Фаза 0 — Окружение

### День 1 — Node.js и редактор
- Node.js — запускает JavaScript на компьютере (плеер для кода).
- npm — менеджер пакетов, ставит чужие библиотеки.
- VS Code — редактор, где пишу код.
- console.log('hi') — выводит текст на экран.
- Запуск файла:
    node index.js

### День 2 — Терминал
- Терминал всегда "стоит" в какой-то папке.
- Навигация:
    cd                 // (Windows) показать текущую папку
    dir                // показать файлы в папке
    cd имя_папки       // зайти в папку
    cd ..              // выйти на уровень назад
    mkdir имя          // создать папку
- Лайфхаки: Tab — автодополнение, стрелка вверх ↑ — прошлые команды.
- PATH — список папок, где система ищет программы. Если "command not found" — программы нет в PATH (лечится перезапуском терминала).

- npm — работа с проектом:
    npm init -y            // создать package.json (паспорт проекта)
    npm install lodash     // поставить библиотеку
    npm run test           // запустить скрипт из package.json

- Три ключевые вещи:
    package.json       -> паспорт проекта (имя + список библиотек)
    package-lock.json  -> точные версии, НЕ трогаю руками
    node_modules/      -> скачанный чужой код, НИКОГДА не коммитить

### День 3 — Git и GitHub
- Git — история изменений на компьютере (сохранения, как в игре).
- GitHub — сайт-облако для кода + портфолио. Git ≠ GitHub.

- Настройка один раз:
    git config --global user.name "Имя"
    git config --global user.email "почта"
    git config --global --list     // проверить

- ⭐ ГЛАВНЫЙ ЦИКЛ (повторяю постоянно):
    git status                    // что изменилось
    git add .                     // подготовить всё
    git commit -m "что сделал"    // сохранить
    git push                      // отправить на GitHub

- Создать репозиторий:
    git init                      // папка -> репозиторий

- .gitignore создаю СРАЗУ, до первого add! Внутри:
    node_modules/
    *.log
    .env

- Если node_modules попал в Git по ошибке (моя ситуация):
    git rm -r --cached node_modules   // убрать из Git, оставить на диске
    git add .
    git commit -m "Remove node_modules from tracking"

- Ветки и Pull Request (как на работе):
    git checkout -b feature/имя   // создать ветку и перейти
    git add .
    git commit -m "..."
    git push -u origin feature/имя
    // дальше на GitHub: Compare & pull request -> Create -> Merge
    git checkout main             // вернуться в main
    git pull                      // забрать изменения на комп

## ⚠️ Грабли, на которые уже наступил
- npm в PowerShell не работал: "выполнение сценариев отключено".
  Решение: переключился на CMD (Terminal: Select Default Profile -> Command Prompt).
- node_modules закоммитился до .gitignore. Чинится через git rm -r --cached.
- Правило: .gitignore создавать ПЕРВЫМ, до git add.

## 🎯 Дальше
- [x] Фаза 0 — окружение готово
- [ ] Фаза 1 — JavaScript (5 недель)

Привет