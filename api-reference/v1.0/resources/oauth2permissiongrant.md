---
title: Тип ресурса oAuth2PermissionGrant
description: Представляет делегированные разрешения (области OAuth 2,0), которые были предоставлены приложению, часто в результате процесса согласия пользователя или администратора.
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: psignoret
ms.openlocfilehash: 557bd9973a3a04ffedb2104a480823de21c95499
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48041199"
---
# <a name="oauth2permissiongrant-resource-type"></a>Тип ресурса oAuth2PermissionGrant

Пространство имен: microsoft.graph

Представляет делегированные разрешения, которые были предоставлены участнику службы приложения.

Предоставленные делегированные разрешения могут быть созданы в результате того, что пользователь отправил запрос на доступ к API или создал его напрямую.

Делегированные разрешения иногда называются "областями" OAuth 2,0 "или" Scopes ".

## <a name="methods"></a>Методы

| Метод | Возвращаемый тип | Описание |
|:---------------|:--------|:----------|
| [Список oAuth2PermissionGrants](../api/oauth2permissiongrant-list.md) | Коллекция [oAuth2PermissionGrant](oauth2permissiongrant.md) | Получение списка предоставленных делегированных разрешений. |
| [Получение oAuth2PermissionGrant](../api/oauth2permissiongrant-get.md) | [oAuth2PermissionGrant](oauth2permissiongrant.md)  | Считывание разрешения с одним делегированным делегированием.|
| [Создание oAuth2PermissionGrant](../api/oauth2permissiongrant-post.md) | [oAuth2PermissionGrant](oauth2permissiongrant.md) | Создайте делегированное предоставление разрешений. |
| [Обновление oAuth2PermissionGrant](../api/oauth2permissiongrant-update.md) | Нет | Обновление объекта oAuth2PermissionGrant. |
| [Удаление oAuth2PermissionGrant](../api/oauth2permissiongrant-delete.md) | Нет  | Удаление делегированного предоставления разрешений. |
|[Получение дельты](../api/oauth2permissiongrant-delta.md)|[oAuth2PermissionGrant](oauth2permissiongrant.md)|Получение только что созданных, обновленных или удаленных объектов **oauth2permissiongrant** без выполнения полного считывания всей коллекции ресурсов.|

## <a name="properties"></a>Свойства

| Свойство | Тип | Описание |
|:---------------|:--------|:----------|
| id | String | Уникальный идентификатор для **oAuth2PermissionGrant**. Только для чтения.|
| clientId | String | **Идентификатор** [субъекта-службы](serviceprincipal.md) клиента для приложения, которому разрешено работать от имени вошедшего пользователя при доступе к API. Обязательно. Поддерживается `$filter` ( `eq` только). |
| консенттипе | String | Указывает, предоставляется ли авторизация клиентскому приложению для олицетворения всех пользователей или только определенного пользователя. *АллпринЦипалс* указывает авторизацию для олицетворения всех пользователей. *Субъект* указывает на авторизацию для олицетворения определенного пользователя. Согласие от имени всех пользователей может быть предоставлено администратором. Пользователи, не являющиеся администраторами, могут быть авторизованы для разрешения от чужого имени в некоторых случаях для некоторых делегированных разрешений. Обязательно. Поддерживается `$filter` ( `eq` только). |
| principalId | String | **Идентификатор** [пользователя](user.md) , от имени которого клиент имеет право доступа к ресурсу, когда **консенттипе** является *субъектом*. Если **консенттипе** — *аллпринЦипалс* , это значение равно null. Является обязательным, если **консенттипе** является *субъектом*. |
| resourceId | String | **Идентификатор** [субъекта службы](serviceprincipal.md) ресурсов, которому разрешен доступ. Этот параметр определяет API, который клиент может пытаться вызвать от имени пользователя, выполнившего вход в систему. |
| scope | String | Разделенный пробелами список значений утверждений для делегированных разрешений, которые следует включить в маркеры доступа для приложения ресурсов (API). Например, `openid User.Read GroupMember.Read.All`. Каждое значение утверждения должно быть согласовано с полем **значение** одного из делегированных разрешений, определенных API, указанным в свойстве **публишедпермиссионскопес** [субъекта-службы](serviceprincipal.md)ресурсов. |

## <a name="relationships"></a>Связи

Отсутствуют.

Этот ресурс поддерживает отслеживание добавлений, удалений и обновлений с помощью [разностного запроса](/graph/delta-query-overview) с функцией [delta](../api/oauth2permissiongrant-delta.md).

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.oAuth2PermissionGrant"
}-->

```json
{
  "clientId": "string",
  "consentType": "string",
  "id": "string (identifier)",
  "principalId": "string",
  "resourceId": "string",
  "scope": "string"
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "oAuth2PermissionGrant resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->

