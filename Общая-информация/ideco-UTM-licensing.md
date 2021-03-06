---
title: Лицензирование Ideco UTM
description: 
published: true
date: 2021-06-21T07:23:38.421Z
tags: 
editor: markdown
dateCreated: 2021-04-02T07:20:54.664Z
---

## Схема лицензирования
У лицензии Ideco UTM есть три основные характеристики.

**Количество пользователей Ideco UTM**: одновременно авторизованные (подключенные к Интернет) пользователи локальной сети клиента или VPN-подключения пользователей, трафик которых проверяется и контролируется шлюзом.

**Редакция Ideco UTM (SMB, и Enterprise)**: набор доступных к использованию модулей в системе и особенности их работы.

**Срок действия лицензии**: не ограничен в редакциях SMB и Enterprise (20 лет). По окончании срока действия лицензии отключена авторизация пользователей и фильтрация трафика.

Различия между редакциями Ideco UTM опубликованы на сайте: <a href="https://ideco.ru/products/ics/editions" target="_blank">https://ideco.ru/products/ics/editions</a>
## Срок действия лицензии Enterprise
Право на использование лицензии действует 5 лет с момента приобретения (согласно п.4, статья 1235 ГК РФ). С 2020 года лицензии по договору бессрочные.
Лицензия имеет подписку, по окончании которой начинают действовать ограничения:

1. Перестает оказываться техническая поддержка сервера по этой лицензии.
2. Обновления сервера до версий, вышедших после даты окончания подписки, становятся невозможны.
3. Перестают работать модули, привязанные к сроку действия подписки на лицензию (система предотвращения вторжений, расширенные базы контент-фильтра, контроль приложений, антивирус и антиспам Касперского).

На остальную функциональность сервера ограничения подписки не распространяются.

Стандартная стоимость лицензии включает годовую подписку. Иные сроки подписки и результирующая стоимость лицензии обсуждаются в отделе продаж компании «Айдеко».
## Контроль и учет сетевых устройств на UTM
- Для доступа сетевого устройства (хоста) в Интернет через UTM с возможностью контроля его трафика, оно должно быть авторизовано на UTM под учетной записью пользователя.
- Под одной учетной записью пользователя на Ideco UTM можно авторизовать до трех хостов с помощью различных методов авторизации.
- Количество приобретенных по лицензии учетных записей ограничивает число одновременно авторизованных пользователей.
- Учетная запись поддерживает одновременную авторизацию только трех хостов.
- Сессия авторизации учетной записи привязана к IP-адресам хостов на протяжении действия сессии.
- Учетная запись может быть авторизована несколькими способами авторизации (но только одно устройство может быть авторизовано по IP под одной учетной записью пользователя).
- Неавторизованный на UTM хост не имеет доступа во внешние сети.
- Сессии авторизации пользователя не проявляющие активность более 15 минут завершаются и могут быть заняты новыми сессиями пользователей. Таким образом обеспечивается конкурентность процесса авторизации пользователей на UTM.
## Бесплатные лицензии
Любой желающий может получить бесплатную лицензию (редакция SMB), в том числе для использования в коммерческих и частных сетях.
UTM, активированный лицензией SMB, позволяет авторизовать не более 20 пользователей (редакция Ideco SMB). Подробнее https://smb.ideco.ru

Получить лицензию SMB можно в личном кабинете: https://my.ideco.ru

**Антиспам Касперского:** приобретается и лицензируется отдельно от основной лицензии UTM и ее коммерческих компонентов. Активируется ключом, предоставленным в отделе продаж компании «Айдеко» после покупки антиспама.