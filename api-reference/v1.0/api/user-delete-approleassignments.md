---
title: Удаление Аппролеассигнмент, назначенных пользователю
description: Удаление Аппролеассигнмент, предоставленных пользователю.
localization_priority: Normal
doc_type: apiPageType
ms.prod: microsoft-identity-platform
author: krbain
ms.openlocfilehash: 939dbfa3863f89be1148c3f3954a3cdc7cd0b74f
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "47992204"
---
# <a name="delete-an-approleassignment-granted-to-a-user"></a>Удаление Аппролеассигнмент, назначенных пользователю

Пространство имен: microsoft.graph

Удаление [аппролеассигнмент](../resources/approleassignment.md) , предоставленных пользователю.

## <a name="permissions"></a>Разрешения

Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).

|Тип разрешения      | Разрешения (в порядке повышения привилегий)              |
|:--------------------|:---------------------------------------------------------|
|Делегированные (рабочая или учебная учетная запись) | Аппролеассигнмент. ReadWrite. ALL, Directory. AccessAsUser. ALL    |
|Делегированные (личная учетная запись Майкрософт) | Не поддерживается.    |
|Для приложений | AppRoleAssignment.ReadWrite.All |

## <a name="http-request"></a>HTTP-запрос

<!-- { "blockType": "ignored" } -->

```http
DELETE /users/{id}/appRoleAssignments/{id}
```

> [!NOTE]
> Рекомендуется удалять назначения ролей приложений с помощью `appRoleAssignedTo` отношения между субъектами службы _ресурсов_ , а не с `appRoleAssignments` назначенным пользователем, группой или субъектом службы.

## <a name="request-headers"></a>Заголовки запросов

| Имя       | Тип | Описание|
|:---------------|:--------|:----------|
| Authorization  | string  | Bearer {токен}. Обязательный. |

## <a name="request-body"></a>Тело запроса

Не указывайте текст запроса для этого метода.

## <a name="response"></a>Отклик

При успешном выполнении этот метод возвращает код отклика `204 No Content`. Метод не возвращает данные в теле отклика.

## <a name="examples"></a>Примеры

### <a name="request"></a>Запрос

Ниже приведен пример запроса на удаление назначения роли приложения.


# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "user_delete_approleassignment"
}-->

```http
DELETE https://graph.microsoft.com/v1.0/users/{id}/appRoleAssignments/{id}
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/user-delete-approleassignment-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/user-delete-approleassignment-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/user-delete-approleassignment-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/user-delete-approleassignment-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a>Отклик

Ниже приведен пример отклика.

<!-- {
  "blockType": "response",
  "truncated": true
} -->

```http
HTTP/1.1 204 No Content
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Delete appRoleAssignment",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->

