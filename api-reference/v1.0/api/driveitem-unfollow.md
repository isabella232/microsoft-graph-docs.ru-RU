---
author: learafa
ms.author: learafa
description: Отменяйте подписку на элемент, на который подписан пользователь.
title: Отписаться от элемента Drive
localization_priority: Normal
ms.prod: sharepoint
doc_type: apiPageType
ms.openlocfilehash: 057ba8e3d75b9e78af19008060426ad695ca5543
ms.sourcegitcommit: 82da4012294b046416c9ae93d2294d80dab217f6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "48904211"
---
# <a name="unfollow-drive-item"></a>Отписаться от элемента Drive

Пространство имен: microsoft.graph

Отменяйте подписку на [driveItem](../resources/driveitem.md).

>**Примечание:** Чтобы подписаться на элемент, обратитесь к разделу [Отслеживание элемента](driveitem-follow.md).

## <a name="permissions"></a>Разрешения

Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).

|Тип разрешения      | Разрешения (в порядке повышения привилегий)              |
|:--------------------|:---------------------------------------------------------|
|Делегированные (рабочая или учебная учетная запись) | Files.Read, Files.ReadWrite, Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All    |
|Делегированные (личная учетная запись Майкрософт) | Не поддерживается.    |
|Для приложений | Files.Read.All, Files.ReadWrite.All, Sites.Read.All, Sites.ReadWrite.All |

## <a name="http-request"></a>HTTP-запрос

<!-- { "blockType": "ignored" } -->

```http
DELETE /me/drive/following/{item-id}
DELETE /users/{user-id}/drive/following/{item-id}
POST /me/drive/items/{item-id}/unfollow
POST /users/{user-id}/drive/items/{item-id}/unfollow
```

## <a name="request-body"></a>Тело запроса

Тело запроса не требуется.

## <a name="response"></a>Отклик

При успешном выполнении вызова API возвращается отклик `204 No Content`. Метод не возвращает данные в теле отклика.

## <a name="example"></a>Пример
### <a name="request"></a>Запрос
Ниже приведен пример запроса.
В этом примере отменяется отслеживание элемента, указанного в параметре `{item-id}` .


# <a name="http"></a>[HTTP](#tab/http)
<!-- { "blockType": "request", "name": "unfollow-item", "scopes": "files.read" } -->

```http
POST /me/drive/items/{item-id}/unfollow
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/unfollow-item-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/unfollow-item-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/unfollow-item-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/unfollow-item-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

### <a name="response"></a>Отклик
<!-- { 
    "blockType": "response", 
    "truncated": true 
} -->
```http
HTTP/1.1 204 No Content
```
<!--
{
  "type": "#page.annotation",
  "description": "Unfollow an item that the user is following.",
  "keywords": "unfollow item",
  "section": "documentation",
  "tocPath": "Items/Unfollow",
  "suppressions": [
  ]
}
-->

