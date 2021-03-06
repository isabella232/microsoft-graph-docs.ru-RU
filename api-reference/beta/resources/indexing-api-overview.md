---
title: Индексирование данных с помощью API Поиска (Майкрософт)
description: Используйте Microsoft Graph для индексирования пользовательских элементов в службе поиска Microsoft.
localization_priority: Priority
author: snlraju-msft
ms.prod: search
doc_type: conceptualPageType
ms.openlocfilehash: 4940e2529a08f326f5e8615987e18488a5a2dbeb
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2020
ms.locfileid: "48403889"
---
# <a name="use-the-microsoft-search-api-to-index-data"></a>Индексирование данных с помощью API Поиска (Майкрософт)

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Вы можете использовать Microsoft Graph для добавления пользовательских элементов в результаты поиска в режиме [поиска Microsoft](/microsoftsearch/overview-microsoft-search).

Запросы на индексирование данных выполняются от имени приложения без вошедшего пользователя, указываемого [маркером доступа с разрешением приложения](/graph/auth-v2-service).

[!INCLUDE [search-api-preview](../../includes/search-api-preview-signup.md)]

## <a name="common-use-cases"></a>Основные варианты использования

Варианты использования интерфейсов API в этом разделе содержат создание [соединителей Microsoft Graph](/microsoftsearch/connectors-overview), включая следующие основные этапы:

1. [Создание подключения](../api/external-post-connections.md) к внешнему источнику данных.
2. [Создание и регистрация схемы](../api/externalconnection-post-schema.md), описывающей тип и способ индексирования внешних данных.
3. [Индексируйте данные](../api/externalconnection-put-items.md) как внешний элемент.

| Варианты использования                                        | Ресурсы REST                              | См. также |
|:-------------------------------------------------|:--------------------------------------------|:--|
| **Действия для настройки**                        |                                             |   |
| Создание, обновление или удаление подключения           | [externalConnection](externalconnection.md) | [Методы externalConnection](externalconnection.md#methods) |
| Регистрация схемы для внешних данных          | [schema](schema.md)                         | [Методы schema](schema.md#methods) |
| **Действия для индексирования**                             |                                             |   |
| Добавление, обновление или удаление пользовательского элемента индекса | [externalItem](externalitem.md)             | [Методы externalItem](externalItem.md#methods) |

## <a name="known-limitations"></a>Известные ограничения

Далее представлены текущие известные ограничения:

- Организациям доступно до 10 подключений.
- Поддерживаются только удостоверения Azure Active Directory.
- Вы можете создавать только четыре `externalItem` элемента ресурсов в секунду.
- Приложение может выполнять до четырех одновременных операций с подключением.
- Емкость подключений ограничена до 700 000 элементов, или примерно 70 ГБ данных.
- Максимальный размер объекта `externalItem` составляет 4 МБ.
- Сортировка результатов не поддерживается.
- Результаты ранжируются наилучшим возможным способом.

## <a name="whats-new"></a>Новые возможности
Узнайте о [новых функциях и обновлениях](/graph/whats-new-overview) для этого набора API.

## <a name="next-steps"></a>Дальнейшие действия

- См. статью [Обзор API Поиска (Майкрософт)](/graph/search-concept-overview).
- Разверните методы, свойства и отношения ресурсов [externalConnection](externalconnection.md), [схемы](schema.md) и [externalItem](externalitem.md).
- Ознакомьтесь с [примером соединителя поиска](https://github.com/microsoftgraph/msgraph-search-connector-sample) на сайте GitHub.


