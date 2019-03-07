# vk-raidbot

## Команды

* `.raid {'Сообщение'} вложения через запятую без пробелов и прочей хуйни` — бот будет флудить сообщением с вложениями

* `.join ссылка на конфу` — заходит в конфу по ссылке

* `.packs` — список паков

* `.pack имя пака` — флудит рандомными картинками из пака, если он существует, конечно. Интервал — 4,7 секунды, актуально для чатов, где бот выпидоривает за флуд

## Установка

0. Клонируем репозиторий
1. Ставим Node.js и npm
2. Заходим в директорию `bot`
3. Копируем файл `config.example.js` в `config.js` и редактируем под свои нужды
4. Устанавливаем зависимости с помощью `npm install`
5. При необходимости поднятия веб-сервера для ввода капчи собираем фронтенд
	1. Заходим в директорию `www`, копируем `Config.example.js` в `Config.js` и редактируем
	2. Собираем с помощью `npm install`, `npm run build`
	3. Если сервер запущен на ~~холокосте~~ локалхосте, проксируем локальный сервер, например, с помощью nginx
6. Снова заходим в директорию `bot` и запускаем бота командой `npm run start`

## Внутреннее WebAPI

### Методы

#### getCaptchas

Выводит доступные для ввода капчи

#### submitCaptcha

Вводит капчу

Параметры:

* `key` — содержимое капчи
* `sid` — ID капчи

## Обновление

1. Обновляем репозиторий с помощью `git pull`
2. Переписываем конфиг, если он обновился, устанавливаем зависимости бота и фронтенда, пересобираем