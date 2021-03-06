---
title: Обновление свойств educationUser
description: Обновление свойств объекта **educationuser**.
localization_priority: Normal
author: mmast-msft
ms.prod: education
doc_type: apiPageType
ms.openlocfilehash: 38a3f187a934f57b9ecb910047367ccf3bf20c28
ms.sourcegitcommit: 342516a52b69fcda31442b130eb6bd7e2c8a0066
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/10/2020
ms.locfileid: "48955148"
---
# <a name="update-educationuser-properties"></a>Обновление свойств educationUser

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Обновление свойств объекта **educationuser**.

## <a name="permissions"></a>Разрешения

Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).

| Тип разрешения                        | Разрешения (в порядке повышения привилегий) |
| :------------------------------------- | :------------------------------------------ |
| Делегированные (рабочая или учебная учетная запись)     | Не поддерживается.                              |
| Делегированные (личная учетная запись Майкрософт) | Не поддерживается.                              |
| Для приложений                            | EduRoster.ReadWrite.All                     |

## <a name="http-request"></a>HTTP-запрос

<!-- { "blockType": "ignored" } -->

```http
PATCH /education/me
PATCH /education/users/{id}
```

## <a name="request-headers"></a>Заголовки запросов

| Заголовок        | Значение                       |
| :------------ | :-------------------------- |
| Авторизация | Bearer {токен}. Обязательный.   |
| Content-Type  | application/json. Обязательный. |

## <a name="request-body"></a>Текст запроса

В тексте запроса укажите значения для соответствующих полей, которые необходимо обновить. Предыдущие значения существующих свойств, не включенных в текст запроса, останутся прежними или будут повторно вычислены с учетом измененных значений других свойств. Для достижения оптимальной производительности не включайте существующие значения, которые не изменились.

| Свойство         | Тип               | Описание                                                                                                                                     |
| :--------------- | :----------------- | :---------------------------------------------------------------------------------------------------------------------------------------------- |
| displayName      | String             | Отображаемое имя пользователя                                                                                                                            |
| givenName        | String             | Имя                                                                                                                                      |
| middleName       | String             | Отчество пользователя                                                                                                                             |
| surname          | String             | Фамилия пользователя                                                                                                                                 |
| mail             | String             | Электронный адрес                                                                                                                                   |
| mobilePhone;      | String             | Номер мобильного телефона пользователя                                                                                                                           |
| externalSource   | string             | Источник для создания пользователя. Возможные значения: `sis` , `manual` , или `lms` .                                                               |
| mailingAddress   | [physicalAddress]  | Почтовый адрес пользователя. Примечание: `type` и `postOfficeBox` не поддерживаются для `educationUser` ресурсов.                                         |
| residenceAddress | [physicalAddress]  | Адрес проживания пользователя. Примечание: `type` и `postOfficeBox` не поддерживаются для `educationUser` ресурсов.                                     |
| primaryRole      | string             | Роль по умолчанию для пользователя. Роль пользователя для отдельного курса может отличаться. Возможные значения: `student`, `teacher`, `enum_sentinel`. |
| student          | [educationStudent] | Если основная роль — student, этот блок будет содержать данные, касающиеся учащегося.                                                                  |
| teacher          | [educationTeacher](../resources/educationteacher.md) | Если основная роль — преподаватель, этот блок будет содержать данные, характерные для преподавателя.                                                                  |

## <a name="response"></a>Отклик

При успешном выполнении этот метод возвратит код отклика `200 OK` и обновленный объект [educationUser](../resources/educationuser.md) в теле отклика.

## <a name="example"></a>Пример

##### <a name="request"></a>Запрос

Ниже приведен пример запроса.

# <a name="http"></a>[HTTP](#tab/http)

<!-- {
  "blockType": "request",
  "name": "update_educationuser"
}-->

```http
PATCH https://graph.microsoft.com/beta/education/users/13020
Content-type: application/json
Content-length: 508

{
  "displayName": "Rogelio Cazares",
  "givenName": "Rogelio",
  "middleName": "Fernando",
  "surname": "Cazares",
}
```

# <a name="c"></a>[C#](#tab/csharp)
[!INCLUDE [sample-code](../includes/snippets/csharp/update-educationuser-csharp-snippets.md)]
[!INCLUDE [sample-code](../includes/snippets/csharp/update-educationuser-csharp-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="javascript"></a>[JavaScript](#tab/javascript)
[!INCLUDE [sample-code](../includes/snippets/javascript/update-educationuser-javascript-snippets.md)]
[!INCLUDE [sample-code](../includes/snippets/javascript/update-educationuser-javascript-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="objective-c"></a>[Objective-C](#tab/objc)
[!INCLUDE [sample-code](../includes/snippets/objc/update-educationuser-objc-snippets.md)]
[!INCLUDE [sample-code](../includes/snippets/objc/update-educationuser-objc-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

# <a name="java"></a>[Java](#tab/java)
[!INCLUDE [sample-code](../includes/snippets/java/update-educationuser-java-snippets.md)]
[!INCLUDE [sdk-documentation](../includes/snippets/snippets-sdk-documentation-link.md)]

---

##### <a name="response"></a>Отклик

Ниже приведен пример отклика. Примечание. Объект отклика, показанный здесь, может быть усечен для краткости. При фактическом вызове будут возвращены все свойства.

<!-- {
  "blockType": "response",
  "truncated": true,
  "@odata.type": "microsoft.graph.educationUser"
} -->

```http
HTTP/1.1 200 OK
Content-type: application/json
Content-length: 508

{
  "id": "13020",
  "displayName": "Rogelio Cazares",
  "givenName": "Rogelio",
  "middleName": "Fernando",
  "surname": "Cazares",
  "mail": "rogelioC@contoso.com",
  "mobilePhone": "+1 (253) 555-0101",
  "createdBy": {
        "user": {
          "displayName": "Susana Rocha",
          "id": "14012",
        }
  },
  "externalSource": "sis",
  "mailingAddress": {
        "city": "Los Angeles",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Main St."
      },
  "primaryRole": "string",
  "residenceAddress": {
        "city": "Los Angeles",
        "countryOrRegion": "United States",
        "postalCode": "98055",
        "state": "CA",
        "street": "12345 Main St."
      },
  "student": {
      "primaryRole": "student",
      "externalId": "13005",
      "birthDate": "2001-01-01T00:00:00Z"
    }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "Update educationuser",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
  ]
}
-->

[PhysicalAddress]: ../resources/physicaladdress.md
[educationstudent]: ../resources/educationstudent.md


