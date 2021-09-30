# SoftwareEngineering
Группа 3530904/90103

* akulackovan - Кулачкова Анастасия

* tkachenkoalexandra - Ткаченко Александра

* AnasStep - Степаненко Анастасия

* gmreyer - Мишин Александр

### Проблема

Цели:

1. Создать Telegram бота для учета личных финансов для достижения экономической осознанности

> не как самостоятельного аналитика, а в качестве MVP (минимальный жизнеспособный функционал), который будет выполнять основную возложенную на него роль: а именно учета расходов. В последствии на основе данного функционала можно развить имеющегося бота вплоть до прогнозов финансового состояния, однако текущей проблеме это не удовлетворяет, поэтому не может быть признано основной целью

2. Реализовать базовую аналитику расходов и возможность категоризации различных трат

> траты фиксируются на обязательные и на нефиксированные. Соответственно, бот будет учитывать максимальный порог ежедневных трат

### Задачи участников

- Архитектура проекта - *gmreyer*

- Разработать основную «бизнес-логику» программы - *tkachenkoalexandra*

- Написать контроллер для работы с «бизнес-логикой» - *akulackovan*

- Провести тестирование имеющегося функционала (QA) - *AnasStep*

### Формулировка проблемы

**Финансовый план поможет не остаться без денег в самый ответственный момент.**

Основная задача при составлении личного бюджета — не просто свести дебет с кредитом, а грамотно распределить траты. Хотя уровень ежемесячных доходов – величина довольно стабильная, и повлиять на неё весьма не просто, однако с расходами дело обстоит несколько иначе – их можно и нужно оптимизировать, и для этого есть множество способов.

Наши траты бывают необходимыми и опциональными. Именно на последние можно при необходимости повлиять. Однако отслуживание и тех, и других позволяет грамотно управлять финансами и осозновать степень консьюмеризма.

Сегодня есть множество вариантов отслеживания трат, они разнообразны, и, фактически, разнородны. Некоторые банки, к примеру, Тинькофф, предлагают уже готовую аналитику на основании ваших трат по счетам, открытых в организации. Несмотря на наличие готового анализа расходов в мобильном банковском приложении, он может не соответствовать запросам пользователей, так как разбить крупные покупки в гипермаркетах на отдельные категории самостоятельно невозможно, поэтому приходится довольствоввться автоматическим распределением.

Существует множество приложений для контроля над тем, сколько средств и на что вы тратите, как CoinKeeper. Однако такой вариант может показаться негоибким, к тому же, ограничивается исключительно мобильным решением, что, возможно, удобно при внесении некотрой информации, но может оказаться весьма ограничивающим фактором.

Использовать приложения же просто для ведения отчетности весьма утомительно, так как делегировать аналитику будет некому, вносить данные, например, в таблицу самостоятельно весьма рутинно и мало эффективно, парсинг же заметок в данном случае гораздо быстрее и продуктивнее.

Хотелось бы настроить учет под себя, выделить свои категории и подкатегории, проводить аналитику во всевозможных разрезах, строить графики и диаграммы на основании имеющихся данных. Учесть необходимость доступности работы с различных устройств.

### Рассматриваемые технологии

- Python (язык программирования)

- Aiogram (библиотека – удобна, т.к. достаточно удобная обертка над Asyncio)

- SQLite (небольшой движок баз данных, умещается практически в одном исполнительном файле, да и сама БД хранится тоже в одном файле (что удобно для дальнейшей аналитики), но при этом обладает всем необходимым: join, внешние ключи, первичные ключи, таблицы. Для такой программы – это оптимальное решение)

- Docker (платформа/ПО для контейнеров) – обязательный элемент по требованиям курса
