---
title: Список ТрустфрамеворкполиЦиес
description: Эта операция перечисляет все объекты Трустфрамеворкполици в клиенте Azure AD B2C.
localization_priority: Normal
author: Nickgmicrosoft
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: ae99ff718b16e97797132261329ac4a0b29ae81e
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48971851"
---
# <a name="list-trustframeworkpolicies"></a>Список ТрустфрамеворкполиЦиес

Пространство имен: microsoft.graph

> **Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены. Использование этих API в производственных приложениях не поддерживается.

Получение списка [трустфрамеворкполиЦиес](../resources/trustframeworkpolicy.md) в клиенте или каталоге.

## <a name="permissions"></a>Разрешения

Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).

|Тип разрешения      | Разрешения (в порядке повышения привилегий)              |
|:--------------------|:---------------------------------------------------------|
|Делегированные (рабочая или учебная учетная запись)|Policy. Read. ALL, Policy. ReadWrite. Трустфрамеворк|
|Делегированные (личная учетная запись Майкрософт)| Не поддерживается.|
|Для приложения|Policy. Read. ALL, Policy. ReadWrite. Трустфрамеворк|

Рабочая или учебная учетная запись должна быть глобальным администратором клиента.

## <a name="http-request"></a>HTTP-запрос

<!-- { "blockType": "ignored" } -->
```http
GET /trustFramework/policies/
```
## <a name="optional-query-parameters"></a>Необязательные параметры запросов

Этот метод поддерживает `$select` `$expand` [параметры запросов OData](/graph/query-parameters) и для настройки отклика.

## <a name="request-headers"></a>Заголовки запросов

|Имя|Описание|
|:---------------|:----------|
|Авторизация|Bearer {токен}. Обязательный.|

## <a name="request-body"></a>Текст запроса

Не указывайте текст запроса для этого метода.

## <a name="response"></a>Отклик

В случае успешного выполнения этот метод возвращает `200 OK` код отклика и коллекцию объектов [трустфрамеворкполици](../resources/trustframeworkpolicy.md) в представлении JSON в тексте отклика.

## <a name="example"></a>Пример

В следующем примере показано получение всех **трустфрамеворкполиЦиес**.

##### <a name="request"></a>Запрос


# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "get_trustFrameworks"
}-->
```msgraph-interactive
GET https://graph.microsoft.com/beta/trustFramework/policies
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/get-trustframeworks-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/get-trustframeworks-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/get-trustframeworks-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/get-trustframeworks-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a>Отклик

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.trustFrameworkPolicy",
  "isCollection": true
} -->
```http
HTTP/1.1 200 OK
Content-type: application/json

{
    "value": [
        {
            "id": "B2C_1A_CustomPolicy2"
        },
        {
            "id": "B2C_1A_CustomPolicy3"
        },
        {
            "id": "B2C_1A_SocialAndLocalAccounts_Base"
        }
    ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "List trustFrameworkPolicy",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->


