---
title: Получение ПрожектпартиЦипатион
description: Получение свойств и связей объекта ПрожектпартиЦипатион.
localization_priority: Normal
author: kevinbellinger
ms.prod: people
doc_type: apiPageType
ms.openlocfilehash: d3c37c0743bd9d1d9eccf0d35584dc537938ca07
ms.sourcegitcommit: 62507617292d5ad8598e83a8a253c986d9bac787
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2019
ms.locfileid: "37937632"
---
# <a name="get-projectparticipation"></a>Получение ПрожектпартиЦипатион

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Получение свойств и связей объекта [прожектпартиЦипатион](../resources/projectparticipation.md) в [профиле](../resources/profile.md)пользователя.

## <a name="permissions"></a>Разрешения

Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).

| Тип разрешения                        | Разрешения (в порядке повышения привилегий)                                      |
|:---------------------------------------|:---------------------------------------------------------------------------------|
| Делегированные (рабочая или учебная учетная запись)     | User. Read, User. ReadWrite, User. ReadBasic. ALL, User. Read. ALL, User. ReadWrite. ALL |
| Делегированные (личная учетная запись Майкрософт) | User. Read, User. ReadWrite, User. ReadBasic. ALL, User. Read. ALL, User. ReadWrite. ALL |
| Application                            | User. ReadBasic. ALL, User. Read. ALL, User. ReadWrite. ALL                            |

## <a name="http-request"></a>HTTP-запрос

<!-- { "blockType": "ignored" } -->

```http
GET /me/profile/projects/{id}
```

## <a name="optional-query-parameters"></a>Необязательные параметры запросов

Этот метод поддерживает следующие параметры запроса OData для настройки ответа. Общие сведения можно найти в разделе [Параметры запроса OData](/graph/query-parameters).

|Имя            |Значение    |Описание                                                                                                                                                                 |
|:---------------|:--------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|$filter         |string   |Разрешает отклик только на те объекты, которые содержат заданные условия.                                                                                             |
|$orderby        |строка   |По умолчанию объекты в отклике сортируются по значению **createdDateTime** в запросе. Вы можете изменить порядок ответа с помощью `$orderby` параметра.|
|$select         |string   |Список разделенных запятыми свойств, которые необходимо включить в отклик. Для оптимизации производительности выбирайте только необходимые свойства.                                        |
|$skip           |int      |Пропустите первые n результатов, которые удобно использовать для разбиения на страницы.                                                                                                                                |
|$top            |int      |Количество возвращаемых результатов.                                                                                                                                           |

## <a name="request-headers"></a>Заголовки запроса

| Имя           |Описание                  |
|:---------------|:----------------------------|
| Авторизация  | Bearer {токен}. Обязательный.   |

## <a name="request-body"></a>Текст запроса

Не указывайте текст запроса для этого метода.

## <a name="response"></a>Ответ

В случае успешного выполнения этот метод возвращает `200 OK` код отклика и запрошенный объект [прожектпартиЦипатион](../resources/projectparticipation.md) в тексте отклика.

## <a name="examples"></a>Примеры

### <a name="request"></a>Запрос

Ниже приведен пример запроса.
<!-- {
  "blockType": "request",
  "name": "get_projectparticipation"
}-->

```http
GET https://graph.microsoft.com/beta/me/profile/projects/{id}
```

### <a name="response"></a>Отклик

Ниже приведен пример отклика.

> **Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.projectParticipation"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "categories": [
    "categories-value"
  ],
  "client": {
    "displayName": "displayName-value",
    "pronunciation": "pronunciation-value",
    "department": "department-value",
    "officeLocation": "officeLocation-value",
    "address": {
      "type": "type-value",
      "postOfficeBox": "postOfficeBox-value",
      "street": "street-value",
      "city": "city-value",
      "state": "state-value",
      "countryOrRegion": "countryOrRegion-value",
      "postalCode": "postalCode-value"
    },
    "webUrl": "webUrl-value"
  },
  "displayName": "displayName-value",
  "detail": {
    "company": {
      "displayName": "displayName-value",
      "pronunciation": "pronunciation-value",
      "department": "department-value",
      "officeLocation": "officeLocation-value",
      "address": {
        "type": "type-value",
        "postOfficeBox": "postOfficeBox-value",
        "street": "street-value",
        "city": "city-value",
        "state": "state-value",
        "countryOrRegion": "countryOrRegion-value",
        "postalCode": "postalCode-value"
      },
      "webUrl": "webUrl-value"
    },
    "description": "description-value",
    "endMonthYear": "datetime-value",
    "jobTitle": "jobTitle-value",
    "role": "role-value",
    "startMonthYear": "datetime-value",
    "summary": "summary-value"
  },
  "colleagues": [
    {
      "displayName": "displayName-value",
      "relationship": "relationship-value",
      "userPrincipalName": "userPrincipalName-value"
    }
  ],
  "sponsors": [
    {
      "displayName": "displayName-value",
      "relationship": "relationship-value",
      "userPrincipalName": "userPrincipalName-value"
    }
  ]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Get projectParticipation",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->