---
title: Получение Пермиссионгрантполици
description: Получение одного объекта Пермиссионгрантполици.
localization_priority: Normal
doc_type: apiPageType
ms.prod: microsoft-identity-platform
author: psignoret
ms.openlocfilehash: a5de4b449d9cdeec4a2293a7944ed44d796816c2
ms.sourcegitcommit: 6201b3a5646f640f25a68ab033eca9eb60ccd05e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/21/2020
ms.locfileid: "49377255"
---
# <a name="get-permissiongrantpolicy"></a>Получение Пермиссионгрантполици

Пространство имен: microsoft.graph

Получение одного объекта [пермиссионгрантполици](../resources/permissiongrantpolicy.md) .

## <a name="permissions"></a>Разрешения

Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).

| Тип разрешения                        | Разрешения (в порядке повышения привилегий) |
|:---------------------------------------|:--------------------------------------------|
| Делегированные (рабочая или учебная учетная запись)     | Policy. Read. Пермиссионгрант, Policy. ReadWrite. Пермиссионгрант |
| Делегированные (личная учетная запись Майкрософт) | Не поддерживается. |
| Приложение                            | Policy. Read. Пермиссионгрант, Policy. ReadWrite. Пермиссионгрант |

## <a name="http-request"></a>HTTP-запрос

<!-- { "blockType": "ignored" } -->

```http
GET /policies/permissionGrantPolicies/{id}
```

## <a name="optional-query-parameters"></a>Необязательные параметры запросов

Этот метод поддерживает [параметры запросов OData](/graph/query-parameters) для настройки отклика.

## <a name="request-headers"></a>Заголовки запросов

| Имя           | Описание                |
|:---------------|:---------------------------|
| Авторизация  | Bearer {токен}. Обязательный.  |

## <a name="request-body"></a>Текст запроса

Не указывайте текст запроса для этого метода.

## <a name="response"></a>Отклик

В случае успешного выполнения этот метод возвращает `200 OK` код отклика и запрошенный объект [пермиссионгрантполици](../resources/permissiongrantpolicy.md) в тексте отклика.

## <a name="examples"></a>Примеры

### <a name="request"></a>Запрос

Ниже приведен пример запроса.
В этом примере запрошенная политика — это встроенная политика предоставления разрешений `microsoft-user-default-low` , которая включает в себя недорогие делегированные разрешения для приложений из проверенных издателей или приложений, зарегистрированных в этом клиенте.


<!-- {
  "blockType": "request",
  "name": "get_permissiongrantpolicy"
}-->

```http
GET https://graph.microsoft.com/v1.0/policies/permissionGrantPolicies/microsoft-user-default-low
```

### <a name="response"></a>Отклик

Ниже приведен пример отклика. Политика имеет два `includes` набора условий, один из которых соответствует Делегированному разрешению, классифицированному `low` для клиентских приложений, зарегистрированных в этом клиенте, и другой, который соответствует делегированным разрешениям, классифицированным `low` для приложений из проверенных издателей (независимо от того, в каком клиенте зарегистрировано приложение).

> **Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.permissionGrantPolicy",
  "isCollection": false
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "id": "microsoft-user-default-low",
    "displayName": "Default User Low Risk Policy",
    "description": "All low risk permissions are consentable by member type users by default.",
    "includes": [
        {
            "id": "cb0c20dd-919d-40c5-ba6d-7ffb233b4b0b",
            "permissionClassification": "low",
            "permissionType": "delegated",
            "resourceApplication": "any",
            "permissions": [ "all" ],
            "clientApplicationIds": [ "all" ],
            "clientApplicationTenantIds": [ "11e37ee2-48fe-42e0-aab9-07d0bb165353" ],
            "clientApplicationPublisherIds": [ "all" ],
            "clientApplicationsFromVerifiedPublisherOnly": false
        },
        {
            "id": "8ce99f96-730c-4ebd-8397-07ee65942b97",
            "permissionClassification": "low",
            "permissionType": "delegated",
            "resourceApplication": "any",
            "permissions": [ "all" ],
            "clientApplicationIds": [ "all" ],
            "clientApplicationTenantIds": [ "all" ],
            "clientApplicationPublisherIds": [ "all" ],
            "clientApplicationsFromVerifiedPublisherOnly": true
        }
    ],
    "excludes": []
}
```
