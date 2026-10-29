# Решение ДЗ TeamCity

## Инфраструктура
- TeamCity Server: `<IP>`
- TeamCity Agent: `<IP>`
- Ansible VM: `<IP>`

## Настройка TeamCity
- Сервер запущен в Docker: `jetbrains/teamcity-server:2023.11.1`
- Агент подключён и одобрен.
- Конфигурация сборки мигрирована в репозиторий (папка `.teamcity`).

## Сборка и артефакты
- Ветка `master`: `mvn clean deploy` → артефакт в Nexus.
- Feature‑ветки: `mvn clean test` → только тесты.
- Новый метод `Welcomer.getReply()` содержит слово `hunter`, тесты проходят.

## Скриншоты
![Agents](screenshots/agents.png)
![Build](screenshots/build.png)
![Nexus](screenshots/nexus.png)

## Ссылка на репозиторий
[https://github.com/Chehlov1M/ваш-репозиторий](https://github.com/Chehlov1M/ваш-репозиторий)
