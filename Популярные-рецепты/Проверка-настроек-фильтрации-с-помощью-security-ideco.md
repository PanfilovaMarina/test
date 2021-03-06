---
title: Проверка настроек фильтрации с помощью security.ideco.ru
description: 
published: true
date: 2021-05-26T11:41:35.774Z
tags: 
editor: markdown
dateCreated: 2021-04-02T07:21:31.956Z
---

Эффективность настроек контент-фильта вы можете проверить с помощью сервиса security.ideco.ru.

При правильной настройке общий уровень защиты должен показывать «зеленый» цвет. Если это не так, проверьте с помощью данной статьи настройки контент-фильтра и других служб фильтрации трафика.

## Предварительная проверка

Убедитесь в том, что службы, описанные ниже, включены и работают в веб-интерфейсе администратора Ideco UTM.

### Раздел «Правила трафика»

- Контент-фильтр;
- Контроль приложений;
- Антивирусы веб-трафика (включен антивирус ClamAV или антивирус Касперского);
- Предотвращение вторжений.

Данные службы полноценно работают только при активной подписке на обновления Ideco UTM. Проверьте актуальность лицензии на Ideco UTM и его модули в разделе **Лицензия**.

### Раздел «Сервисы»

Убедитесь в том, что в настройках раздела **Прокси -> Исключения**, в пункте **Сети источника** не указана сеть, куда входит IP-адрес компьютера, с которого вы заходите на сайт security.ideco.ru.

А в пункте **Сети назначения** не включены неизвестные вам ресурсы или не ограничены масками, куда входят тысячи или миллионы адресов.

> Помните, что любые исключения ресурсов в прокси-сервере исключают их также из проверки контент-фильтром.
{.is-info}

## Проверка настроек служб

### Контент-фильтр

Правилами, действующими на пользователя должны быть запрещены следующие категории сайтов:

- Анонимайзеры;
- Ботненты;
- Фишинг/мошенничество;
- Казино, лотереи, тотализаторы;
- Порнография;
- Список Минюста;
- Астрология и гороскопы;
- Знакомства;
- Компьютерные игры;
- Мультфильмы, аниме и комиксы;
- Развлекательные новости и сайты про знаменитостей;
- Онлайн-реклама и баннеры;
- Торрент-трекеры.

Кроме того, для возможности антивирусной проверки HTTPS-трафика должно быть создано правило по расшифровке всего HTTPS трафика для пользователей, в число которых входит пользователь, проверяющий настройки на security.ideco.ru.

Убедитесь, что контент-фильтр работает для вашего пользователя. Для этого попробуйте перейти на сайт: `sex.com`. Вы должны увидеть страницу блокировки.

### Предотвращение вторжений

В данной службе должны быть активны следующие группы правил:

- Анонимайзеры;
- GeoIP Страны Юго-Восточной Азии;
- GeoIP Территории Африки и зависимые территории;
- GeoIP Южная Америка и зависимые территории;
- Пулы криптомайнеров.

Некоторые правила системы работают с помощью блокировки DNS-запросов пользователей, поэтому если вы используете Ideco UTM в качестве прокси-сервера, убедитесь, что DNS-запросы также проходят через него (например, сделайте так, чтобы ваш контроллер домена Active Directory резолвил внешние адреса через Ideco UTM).

### Контроль приложений

Для защиты от «пожирателей времени и трафика» создайте правила  запрещением доступа следующих протоколов:

- Bittorrent;
- Steam;
- Worlofwarcraft;
- Mining.

Проведите повторное тестирование с помощью [security.ideco.ru](https://security.ideco.ru/) после изменения правил.