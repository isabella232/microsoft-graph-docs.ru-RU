---
title: Список удаленных элементов, принадлежащих пользователю
description: 'Получает список недавно удаленных элементов, принадлежащих указанному пользователю.  '
author: keylimesoda
localization_priority: Normal
ms.prod: microsoft-identity-platform
doc_type: apiPageType
ms.openlocfilehash: f639bb8b0c7fcf04aff072cc3295255a310fbfda
ms.sourcegitcommit: 7ceec757fd82ef3fd80aa3089ef46d3807aa3aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/09/2020
ms.locfileid: "48404541"
---
# <a name="list-deleted-items-owned-by-a-user"></a>Список удаленных элементов, принадлежащих пользователю

Пространство имен: microsoft.graph

Получает список недавно удаленных элементов, принадлежащих указанному пользователю.  

В настоящее время функции списка удаленных элементов поддерживаются только для ресурсов [приложения](../resources/application.md) и [группы](../resources/group.md) , принадлежащих пользователю.

Это действие службы, которое означает, что она не поддерживает разбивку на страницы.  API возвращает до 1 000 удаленных объектов, принадлежащих пользователю, отсортированных по ИДЕНТИФИКАТОРу.

## <a name="permissions"></a>Разрешения

Для вызова этого API требуется одно из указанных ниже разрешений. Дополнительные сведения, включая сведения о том, как выбрать разрешения, см. в статье [Разрешения](/graph/permissions-reference).

| Тип разрешения | Разрешения (в порядке повышения привилегий) |
| --- | --- |
| Делегированные (рабочая или учебная учетная запись) | Group.Read.All, Group.ReadWrite.All |
| Делегированные (личная учетная запись Майкрософт) |  Не поддерживается. |
| Для приложений | Group.Read.All, Group.ReadWrite.All  |

## <a name="http-request"></a>HTTP-запрос

``` http
POST /directory/deletedItems/getUserOwnedObjects
```

## <a name="request-headers"></a>Заголовки запросов

| Имя          | Описание               |
| ------------- | ------------------------- |
| Авторизация | Bearer {токен}. Обязательный. |

## <a name="request-body"></a>Текст запроса

```json
{
  "userId":"{id}",
  "type":"Group"
}
```

В тексте запроса требуются следующие параметры:

| Параметр    | Тип |Описание|
|:---------------|:--------|:----------|
|userId|String|Идентификатор владельца.|
|type|String|Тип собственных объектов, которые требуется вернуть; в `Group` настоящее время является единственным поддерживаемым значением.|


## <a name="response"></a>Отклик

Успешные запросы возвращают `200 OK` коды ответа; объект Response содержит свойства [Directory (удаленные элементы)](../resources/directory.md) .

## <a name="example"></a>Пример

##### <a name="request"></a>Запрос

Ниже приведен пример запроса.

``` http
POST https://graph.microsoft.com/v1.0/directory/deletedItems/getUserOwnedObjects
Content-type: application/json
```

``` json
{
  "userId":"55ac777c-109e-4022-b58c-470c8fcb6892",
  "type":"group"
}
```

###### <a name="response"></a>Отклик

Ниже приведен пример отклика. Note: этот объект ответа может быть усечен для краткости. Все поддерживаемые свойства возвращаются из фактических вызовов.

``` http
HTTP/1.1 200
Content-type: application/json
Content-length: 1249

{
"value": [
          {
              "@odata.type": "#microsoft.graph.group",
              "id": "bfa7033a-7367-4644-85f5-95aaf385cbd7",
              "deletedDateTime": 2018-04-01T12:39:16Z,
              "classification": null,
              "createdDateTime": "2017-03-22T12:39:16Z",
              "description": null,
              "displayName": "Test",
              "groupTypes": [
                  "Unified"
              ],
              "mail": "Test@contoso.com",
              "mailEnabled": true,
              "mailNickname": "Test",
              "membershipRule": null,
              "membershipRuleProcessingState": null,
              "preferredDataLocation": null,
              "preferredLanguage": null,
              "proxyAddresses": [
                  "SMTP:Test@contoso.com"
              ],
              "renewedDateTime": "2017-09-22T22:30:39Z",
              "securityEnabled": false,
              "theme": null,
              "visibility": "Public"
          } 
        ]
 }
```