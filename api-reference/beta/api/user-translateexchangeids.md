---
title: 'Пользователь: Транслатиксчанжеидс'
description: Перевод идентификаторов ресурсов, связанных с Outlook, между форматами.
author: svpsiva
localization_priority: Normal
ms.prod: outlook
doc_type: apiPageType
ms.openlocfilehash: 7799f02dbb090be6d62d72f22a9ee0ef6c182d36
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48980012"
---
# <a name="user-translateexchangeids"></a>Пользователь: Транслатиксчанжеидс

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Перевод идентификаторов ресурсов, связанных с Outlook, между форматами.

## <a name="permissions"></a>Разрешения

Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).

| Тип разрешения | Разрешения (в порядке повышения привилегий) |
|:----------------|:--------------------------------------------|
| Делегированные (рабочая или учебная учетная запись) | User. ReadBasic. ALL, User. Read, User. ReadWrite, User. ReadBasic. ALL, User. Read. ALL, User. ReadWrite. ALL |
| Делегированные (личная учетная запись Майкрософт) | User. ReadBasic. ALL, User. Read, User. ReadWrite |
| Для приложений | User.Read.All, User.ReadWrite.All |

## <a name="http-request"></a>HTTP-запрос

<!-- { "blockType": "ignored" } -->

```http
POST /me/translateExchangeIds
POST /users/{id|userPrincipalName}/translateExchangeIds
```

## <a name="request-headers"></a>Заголовки запросов

| Имя | Значение |
|:-----|:------|
| Авторизация | Bearer {токен}. Обязательный. |

## <a name="request-body"></a>Текст запроса

| Параметр | Тип | Описание |
|:----------|:-----|:------------|
| инпутидс | Коллекция строк | Коллекция идентификаторов для преобразования. Все идентификаторы в коллекции должны иметь одинаковый тип идентификатора источника и должны быть для элементов в одном почтовом ящике. Максимальный размер этой коллекции составляет 1000 строк. |
| саурцеидтипе | ексчанжеидформат | Тип идентификатора идентификаторов в `InputIds` параметре. |
| таржетидтипе | ексчанжеидформат | Запрошенный тип идентификатора для преобразования. |

### <a name="exchangeidformat-values"></a>значения Ексчанжеидформат

| Значения | Описание |
|:-------|:------------|
| Код | Формат идентификатора двоичной записи, используемый клиентами MAPI. |
| евсид | Формат идентификатора, используемый клиентами веб-служб Exchange. |
| иммутаблинтрид | Двоичный формат неизменяемого идентификатора, совместимый с MAPI. |
| рестид | Формат идентификатора по умолчанию, используемый Microsoft Graph. |
| рестиммутаблинтрид | Неизменяемый формат идентификатора, используемый Microsoft Graph. |

Двоичные форматы ( `entryId` и `immutableEntryId` ) являются безопасными в URL-адресах в кодировке Base64. Безопасность URL реализована путем изменения кодировки base64 двоичных данных следующим образом:

- Замените `+` на `-`
- Замените `/` на `_`
- Удалите все замыкающие символы заполнения ( `=` ).
- Добавьте целое число в конец строки, указывающую количество заполненных символов в исходной ( `0` , `1` или `2` ).

## <a name="response"></a>Отклик

В случае успешного выполнения этот метод возвращает `200 OK` код отклика и коллекцию [конвертидресулт](../resources/convertidresult.md) в тексте отклика.

## <a name="example"></a>Пример

В приведенном ниже примере показано, как преобразовать несколько идентификаторов из стандартного формата REST API ( `restId` ) в неизменяемый формат REST ( `restImmutableEntryId` ).

### <a name="request"></a>Запрос

Ниже представлен пример запроса.

# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "user_translateexchangeids"
}-->

```http
POST https://graph.microsoft.com/beta/me/translateExchangeIds
Content-Type: application/json

{
  "inputIds" : [
    "{rest-formatted-id-1}",
    "{rest-formatted-id-2}"
  ],
  "sourceIdType": "restId",
  "targetIdType": "restImmutableEntryId"
}
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/user-translateexchangeids-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/user-translateexchangeids-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/user-translateexchangeids-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/user-translateexchangeids-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


### <a name="response"></a>Отклик

Ниже приведен пример ответа
<!-- {
  "blockType": "response",
  "@odata.type": "microsoft.graph.convertIdResult",
  "isCollection": true
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json

{
  "value": [
    {
      "sourceId": "{rest-formatted-id-1}",
      "targetId": "{rest-immutable-formatted-id-1}"
    },
    {
      "sourceId": "{rest-formatted-id-2}",
      "targetId": "{rest-immutable-formatted-id-2}"
    }
  ]
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Example",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->


