---
title: Обновление schemaExtension
description: Обновление свойств в определении указанного schemaExtension.
localization_priority: Normal
author: dkershaw10
ms.prod: extensions
doc_type: apiPageType
ms.openlocfilehash: ac657ee517a11201cab50c8aa161ad20c9352ff8
ms.sourcegitcommit: ea3b1a8b781a347015d9542826c5c0c24d50d35d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/19/2020
ms.locfileid: "49352447"
---
# <a name="update-schemaextension"></a>Обновление schemaExtension

Пространство имен: microsoft.graph

Обновление свойств в определении указанного [schemaExtension](../resources/schemaextension.md). 

Это означает, что пользовательские свойства или целевые типы ресурсов невозможно удалить из определения, но можно добавить новые настраиваемые свойства, а также изменить описание расширения.

Добавочные обновления расширения можно выполнить только в том случае, если расширение находится в состоянии "в **разработке** " или " **доступно** ". 

Обновление применяется ко всем ресурсам, включенным в свойство **TargetType** расширения. Эти ресурсы относятся к [типам вспомогательных ресурсов](/graph/extensibility-overview#supported-resources).

Для делегированных потоков пользователь, вошедшего в систему, может обновить расширение схемы, если для свойства **owner** расширения задано значение **AppID** приложения, которому принадлежит вошедшего пользователь. Это может быть приложение, которое изначально создало расширение, или другое приложение, принадлежащее пользователю, вошедшего в систему. 

Этот критерий для свойства **owner** позволяет вошедшего в систему пользователю вносить изменения в другие приложения, которыми они не владеет, например, Microsoft Graph Explorer. При использовании проводника Graph для обновления ресурса **schemaExtension** Включите свойство **owner** в текст запроса PATCH. Для получения дополнительных сведений см раздел [Extensions](/graph/known-issues#extensions) in [Известные проблемы в Microsoft Graph](/graph/known-issues).

## <a name="permissions"></a>Разрешения
Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).


|Тип разрешения      | Разрешения (в порядке повышения привилегий)              |
|:--------------------|:---------------------------------------------------------|
|Делегированные (рабочая или учебная учетная запись) | Application.ReadWrite.All, Directory.AccessAsUser.All    |
|Делегированные (личная учетная запись Майкрософт) | Не поддерживается.    |
|Для приложений | Не поддерживается. |

## <a name="http-request"></a>HTTP-запрос

<!-- { "blockType": "ignored" } -->
```http
PATCH /schemaExtensions/{id}
```

## <a name="optional-request-headers"></a>Необязательные заголовки запросов

| Имя      |Описание|
|:----------|:----------|
| Авторизация  | Bearer {токен}. Обязательный. |
| Content-Type   | application/json |

## <a name="request-body"></a>Текст запроса

В тексте запроса укажите значения для соответствующих полей, которые необходимо обновить. Предыдущие значения существующих свойств, не включенных в текст запроса, останутся прежними или будут повторно вычислены с учетом измененных значений других свойств. Для достижения оптимальной производительности не следует включать существующие значения, которые не изменились.

| Свойство   | Тип |Описание|
|:---------------|:--------|:----------|
|description|String|Описание расширения схемы.|
|properties|Коллекция [extensionSchemaProperty](../resources/extensionschemaproperty.md)|Коллекция типов и имен свойств, составляющих определение расширения схемы. Разрешены только добавочные изменения. |
|status|String|Состояние жизненного цикла расширения схемы. Начальное состояние при создании **разрабатывается**. Переход между состояниями возможен из **разработки** в **доступном** и **доступном** для **устаревших** состояниях.|
|targetTypes|Коллекция String|Набор типов Microsoft Graph (поддерживающих расширения), к которым можно применить это расширение схемы.  Разрешены только добавочные изменения.|

## <a name="response"></a>Отклик

В случае успешного выполнения этот метод возвращает код отклика `204 No Content`.

## <a name="example"></a>Пример

##### <a name="request"></a>Запрос

Ниже приведен пример запроса.

# <a name="http"></a>[HTTP](#tab/http)
<!-- {
  "blockType": "request",
  "name": "update_schemaextension"
}-->
```http
PATCH https://graph.microsoft.com/v1.0/schemaExtensions/{id}
Content-type: application/json
Content-length: 201

{
  "properties": [
    {
      "name":"new-name-value",
      "type":"new-type-value"
    },
    {
      "name":"additional-name-value",
      "type":"additional-type-value"
    }
  ]
}
```
# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/update-schemaextension-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/update-schemaextension-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/update-schemaextension-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/update-schemaextension-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---


##### <a name="response"></a>Отклик

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.schemaExtension"
} -->
```http
HTTP/1.1 204 No Content
```

## <a name="see-also"></a>См. также

- [Добавление пользовательских данных в ресурсы с помощью расширений](/graph/extensibility-overview)
- [Добавление пользовательских данных в группы с помощью расширений схемы](/graph/extensibility-schema-groups)

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "Update schemaextension",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}-->

