# Плагин для оповещений в Slack для Redmine

Этот плагин отправляет сообщения в Slack из Redmine при следующих условиях:

1. Создание задачи (в личные сообщения автору, исполнителю, наблюдателям)
2. Изминени задачи (в личные сообщения автору, исполнителю, наблюдателям)
3. Закрытие задачи (в личные сообщения автору, исполнителю, наблюдателям)
4. Изминения в Wiki (в общий канал или в личные сообщения из настроек плагина)

## Скриншоты

![screenshot](https://raw.github.com/sciyoshi/redmine-slack/gh-pages/screenshot.png)

## Установка

В корневой директории Redmine выполните команды:

```
cd plugins
git clone https://github.com/kaizer666/redmine-slack-direct.git redmine_slack
```

Вам так же понадобится `httpclient`, установить который можно командой

```
bundle install
```

находясь в директории `plugins`.

Перезапустите Redmine и перейдите в настройки плагина.

Укажите `Slack API URL` для `Incoming WebHook`, а так же иконку и канал по-умолчанию.

## Отправка оповещений

Создайте "Настраиваемое поле" (`Custom Field`) для проектов с именем "Slack Channel" для отправки оповещений от Wiki каждого проекта в свой канал.

Создайте "Настраиваемое поле" (`Custom Field`) для пользователей с именем "Slack name" для отправки оповещений о задачах лично каждому пользователю.

Что бы отключить уведомления для проекта - укажите в качестве Slack Channel для него "-" (тире).

Дополнительную информацию читайте тут http://www.redmine.org/projects/redmine/wiki/Plugins.
