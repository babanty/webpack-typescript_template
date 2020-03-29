# Шаблон под TypeScript с webpack (UI - index.html)

## Что делает полезного?

- удобно собирает (билдит) проект на typescript готовя его к выкладке на продакшн с автоматическим перевариванием js/ts кода под стандарт поддерживаемый всеми браузерами;
- имена выходных файлов "динамические", что исключает проблему, когда браузер кеширует код и, соотвественно, игнориррует изменения;
- позволяет удобно работать в режиме разработчика с поддержкой source map (когда в браузере при дебаге читаемый код). Автоматически запускает сервер с сайтом и при изменении файлов автоматом всё перебилживает;
- поддерживает import, код можно разбивать на множество файлов;
- тут уже подключен normalize.css (чтобы css-стили по умолчанию во всех браузерах не отличались);
- все конфиги максимально приправлены комментариями на русском для снижения "порога входа"
- ни какие конфиги не спрятаны, т.е. они без проблем "перенастраиваются и дополняются под себя"

## Как использовать?
### Скачиваем шаблон
- скачиваете и устанавливаете NodeJS;
- скачиваете этот шаблон;
- откройте консоль, чтобы она смотрела в кореневую папку шаблона (не важно какая консоль, cmd, powershell, bash и т.д.)
- исполняем команду:
```sh
$ npm install
```
### Разрабатываем с шаблоном
Теперь можно пользоваться шаблоном. Для этого, для удобства откройте удобную IDE (например VS Code) глядящую на папку "src" (можно и на коренемую папку шаблона, но тогда Вы будете видеть кучу не интересных файлов и папок)

Протестируйте, все ли работает:
- в открытой ранее консоли напишите:
```sh
$ npm run dev
```
### Билдим готовый проект
Чтобы сбилдить проект, готовый к вакладке на продакшн:
- в открытой ранее консоли напишите:
```sh
$ npm run build
```
- готово, файлы лежат в папке ui_artefacts

## Структура файлов
- node_modules - папка с модулями (появится только после npm install, см. выше)
- src - тут лежит весь код Вашего проекта
-- images - папка, для примера как копируются файлы в выходной каталог
-- index.html - стандартный html, ни в чем не ограничен. Он же будет в выходном каталоге
-- styles.css - стандартные css-стили, их не нужно добавлять в index.html, они добавляются автоматом
-- testBabel.ts - файл для тестирования import-а и для тестирования "переваривания кода под работоспособность почти на всех браузерах"
- ui_artefacts - папка с готовыми для выкладки на продакшн файлами
- package-с комментами.txt - файл можно удалить, тут закомментированный package.json
- package-lock.json - системный файл для npm, создается живет автоматически
- package.json - содержит в себе описание проекта и подключенные модули (необходим для их подгрузки с помощью npm install)
- webpack.config.js - главный файл webpack-а содержащий в себе все настройки (там куча комментов внутри)
