---
title: Тип ресурса Привилежедролеассигнмент
description: 'Представляет назначение привилегированной роли для определенного пользователя. '
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: shauliu
ms.openlocfilehash: 924040176c2b979e6e25f70d5529c44f69b82959
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48052532"
---
# <a name="privilegedroleassignment-resource-type"></a>Тип ресурса Привилежедролеассигнмент

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет назначение привилегированной роли для определенного пользователя. 


## <a name="methods"></a>Методы

| Метод           | Возвращаемый тип    |Описание|
|:---------------|:--------|:----------|
|[Коллекция Привилежедролеассигнмент списка](../api/privilegedroleassignment-list.md) | Коллекция [privilegedRoleAssignment](privilegedroleassignment.md)|Получение коллекции объектов Привилежедролеассигнмент.|
|[Получение privilegedRoleAssignment](../api/privilegedroleassignment-get.md) | [privilegedRoleAssignment](privilegedroleassignment.md) |Чтение свойств и связей объекта Привилежедролеассигнмент.|
|[Создание задания](../api/privilegedroleassignment-post-privilegedroleassignments.md) |[privilegedRoleAssignment](privilegedroleassignment.md)| Создайте новое назначение путем публикации в коллекции назначений.|
|[Удаление](../api/privilegedroleassignment-delete.md) | Нет |Удаление объекта privilegedRoleAssignment. |
|[makePermanent](../api/privilegedroleassignment-makepermanent.md)|[privilegedRoleAssignment](privilegedroleassignment.md)|Выполнение назначения ролей как бессрочного.|
|[makeEligible](../api/privilegedroleassignment-makeeligible.md)|[privilegedRoleAssignment](privilegedroleassignment.md)|Выполнение назначения ролей как соответствующего требованиям.|
|[my](../api/privilegedroleassignment-my.md)|Коллекция [privilegedRoleAssignment](privilegedroleassignment.md)|Получение привилегированных назначений ролей текущего пользователя.|

## <a name="properties"></a>Свойства
| Свойство     | Тип   |Описание|
|:---------------|:--------|:----------|
|expirationDateTime|dateTimeOffset|Дата и время в формате UTC, когда истечет срок действия назначения роли Temporary privileged. Для назначения постоянной роли значение равно null.|
|id|string| Уникальный идентификатор для назначения привилегированной роли. Только для чтения. Он имеет формат "userId_roleId", где userId — это строка GUID для идентификатора пользователя Azure AD, а roleId — строка GUID для идентификатора роли администратора Azure.|
|Повышенный уровень|boolean|**значение true** , если назначение роли активировано. **значение false** , если назначение роли отключено.|
|ресултмессаже|string|Результирующее сообщение, заданное службой.|
|roleId|string|Идентификатор роли. В формате строки GUID.|
|userId|строка|Идентификатор пользователя. В формате строки GUID.|

## <a name="relationships"></a>Связи
| Связь | Тип   |Описание|
|:---------------|:--------|:----------|
|ролеинфо|[privilegedRole](privilegedrole.md)| Только для чтения. Допускается значение null. Сведения о связанной роли.|

## <a name="json-representation"></a>Представление JSON

Ниже представлено описание ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "baseType":"microsoft.graph.entity",
  "@odata.type": "microsoft.graph.privilegedRoleAssignment"
}-->

```json
{
  "expirationDateTime": "String (timestamp)",
  "id": "string (identifier)",
  "isElevated": true,
  "resultMessage": "string",
  "roleId": "string",
  "userId": "string"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "privilegedRoleAssignment resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


