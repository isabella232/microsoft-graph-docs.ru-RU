---
title: Тип ресурса Привилежедролеассигнментрекуест
description: Представляет запрос для операций назначения ролей в Привилегд управления удостоверениями.
localization_priority: Normal
doc_type: resourcePageType
ms.prod: microsoft-identity-platform
author: shauliu
ms.openlocfilehash: 5daeeee6f784c31f1e15843a8a1903ca41565118
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48070515"
---
# <a name="privilegedroleassignmentrequest-resource-type"></a>Тип ресурса Привилежедролеассигнментрекуест

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет запрос для операций назначения ролей в Привилегд управления удостоверениями.

`privilegedRoleAssignmentRequest` — Это объект с моделированием билетов, используемый для управления жизненным циклом назначений ролей. Он представляет намерение/решение для пользователей и администраторов, а также обеспечивает гибкость, позволяющую включать реализацию перечисленных счдулинг, шлюзов утверждения и т. д., как и в сравнении с прямым предоставлением `POST` и работой, а `LIST` также `MY` `Cancel` функциями `governanceRoleAssignment` .

## <a name="methods"></a>Методы

| Метод       | Возвращаемый тип | Описание |
|:-------------|:------------|:------------|
|[Список](../api/privilegedroleassignmentrequest-list.md) | Коллекция [привилежедролеассигнментрекуест](../resources/privilegedroleassignmentrequest.md)|Список запросов на назначение ролей.|
|[Создание](../api/privilegedroleassignmentrequest-post.md)|  [привилежедролеассигнментрекуест](../resources/privilegedroleassignmentrequest.md)|Создание запроса на управление жизненным циклом существующего или нового назначения роли.|
|[Отмена](../api/privilegedroleassignmentrequest-cancel.md)|  |Отмена ожидающего запроса на назначение роли.|
|[My](../api/privilegedroleassignmentrequest-my.md)|  |Получение запроса на назначение роли для текущего рекустор.|

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|id|String| Только для чтения. Идентификатор запроса на назначение роли.|
|ассигнментстате|String| Состояние назначения. Значение может быть `Eligible` для правого назначения `Active` , если оно напрямую назначено `Active` администраторами или активировано в соответствии с подходящими пользователями.|
|duration|String| Продолжительность назначения роли.|
|reason|String| Причина назначения роли.|
|рекуестеддатетиме|DateTimeOffset| Только для чтения. Время создания запроса. Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда применяется формат UTC). Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`.|
|roleId|String| Идентификатор роли.|
|schedule|[governanceSchedule](governanceschedule.md)| Объект расписания для запроса на назначение роли.|
|status|String| Только для чтения. состояние запроса на назначение роли. Возможные значения:,,,,,,,,, `NotStarted` `Completed` `RequestedApproval` `Scheduled` `Approved` `ApprovalDenied` `ApprovalAborted` `Cancelling` `Cancelled` `Revoked` , `RequestExpired` .|
|тиккетнумбер|String| Тиккетнумбер для назначения роли. |
|тиккетсистем|String| Тиккетсистем для назначения роли.|
|type|String| Представляет тип операции для назначения роли. Возможные значения `AdminAdd` : администраторы добавляют пользователей к ролям; `UserAdd` : пользователи добавляют назначения ролей.|
|userId|String| Идентификатор пользователя.|

## <a name="relationships"></a>Отношения
| Связь | Тип        | Описание |
|:-------------|:------------|:------------|
|ролеинфо|[privilegedRole](privilegedrole.md)| Объект Ролеинфо запроса назначения роли.|

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.privilegedRoleAssignmentRequest"
}-->

```json
{
  "assignmentState": "String",
  "duration": "String",
  "id": "String (identifier)",
  "reason": "String",
  "requestedDateTime": "String (timestamp)",
  "roleId": "String",
  "schedule": {"@odata.type": "microsoft.graph.governanceSchedule"},
  "status": "String",
  "ticketNumber": "String",
  "ticketSystem": "String",
  "type": "String",
  "userId": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "privilegedRoleAssignmentRequest resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


