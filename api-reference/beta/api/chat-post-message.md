---
title: Отправка chatMessage в чате
description: Отправка нового chatMessage в чате.
localization_priority: Normal
author: RamjotSingh
ms.prod: microsoft-teams
doc_type: apiPageType
ms.openlocfilehash: 0e11602181e50c2d6a190e45622c6bc7d4cd323f
ms.sourcegitcommit: a9720ab80625a4692f7d2450164717853535d0b0
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/11/2020
ms.locfileid: "48993950"
---
# <a name="send-chatmessage-in-a-chat"></a>Отправка chatMessage в чате

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Создание нового [chatMessage](../resources/chatmessage.md) в указанном [сеансе чата](../resources/chat.md). Этот API не может создать новый чат; чтобы получить идентификатор существующего чата, необходимо использовать метод Chat [List](chat-list.md) Chats, прежде чем создавать сообщение чата.

> **Note** : мы не рекомендуем использовать этот API для переноса данных. Пропускная способность, необходимая для обычной миграции, отсутствует.

> **Note** : нарушение [условий использования](/legal/microsoft-apis/terms-of-use) Microsoft Teams в качестве файла журнала. Отправлять только сообщения, которые пользователи смогут читать.

## <a name="permissions"></a>Разрешения

Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).

| Тип разрешения                        | Разрешения (в порядке повышения привилегий) |
|:---------------------------------------|:--------------------------------------------|
| Делегированные (рабочая или учебная учетная запись)     | ChatMessage. Send, Chat. ReadWrite |
| Делегированные (личная учетная запись Майкрософт) | Не поддерживается. |
| Для приложений                            | Не поддерживается. |

## <a name="http-request"></a>HTTP-запрос

<!-- { "blockType": "ignored" } -->

```http
POST /chats/{id}/messages
POST /users/{id}/chats/{id}/messages
```

## <a name="request-headers"></a>Заголовки запросов

| Имя          | Описание   |
|:--------------|:--------------|
| Авторизация | Bearer {код}. Обязательно. |

## <a name="request-body"></a>Текст запроса

В тексте запроса добавьте представление объекта [chatMessage](../resources/chatmessage.md) в формате JSON.

## <a name="response"></a>Отклик

В случае успешного выполнения этот метод возвращает `201 Created` код отклика и новый объект [chatMessage](../resources/chatmessage.md) в тексте отклика.

## <a name="examples"></a>Примеры

Более полный список примеров приведен [в статье Создание chatMessage в канале или чате](chatmessage-post.md).

### <a name="request"></a>Запрос

Ниже приведен пример запроса.

# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "create_chatmessage_from_chat"
}-->

```http
POST https://graph.microsoft.com/beta/teams/{id}/channels/{id}/messages
Content-type: application/json

{
  "body": {
     "content": "Hello world"
  }
}
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/create-chatmessage-from-chat-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/create-chatmessage-from-chat-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/create-chatmessage-from-chat-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/create-chatmessage-from-chat-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a>Отклик

Ниже приведен пример отклика.

> **Примечание.** Представленный здесь объект отклика может быть сокращен для удобочитаемости. При фактическом вызове будут возвращены все свойства.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.chatMessage"
} -->

```http
HTTP/1.1 201 Created
Content-type: application/json

{
  "id": "id-value",
  "replyToId": "replyToId-value",
  "from": {
    "application": null,
    "device": null,
    "user": {
      "id": "87ea812c-8816-40e9-b770-5c165fa31397",
      "displayName": "Test User"
    }
  },
  "messageType": "message",
  "body": {
     "content": "Hello world",
     "contentType": "text"
  }
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Create chatMessage",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->
