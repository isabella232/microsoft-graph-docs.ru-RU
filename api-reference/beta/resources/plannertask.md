---
title: Тип ресурса plannerTask
description: Ресурс **plannerTask** представляет задачу планировщика в Microsoft 365. Задача планировщика входит в план и может быть назначена сегменту в плане. Каждый объект Task содержит объект Details, который может содержать дополнительные сведения о задаче. Просмотрите обзор для получения дополнительных сведений о связях между группами, планами и задачами.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
doc_type: resourcePageType
ms.openlocfilehash: b630976abce3ecebb92eed84ec593f9a1e70f2cd
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48064009"
---
# <a name="plannertask-resource-type"></a>Тип ресурса plannerTask

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Ресурс **plannerTask** представляет задачу планировщика в Microsoft 365. Задача планировщика входит в [план](plannerplan.md) и может быть назначена [сегменту](plannerbucket.md) в плане. Каждый объект Task содержит объект [Details](plannertaskdetails.md) , который может содержать дополнительные сведения о задаче. Просмотрите [Обзор](planner-overview.md) для получения дополнительных сведений о связях между группами, планами и задачами.


## <a name="methods"></a>Методы

| Метод           | Возвращаемый тип    |Описание|
|:---------------|:--------|:----------|
|[Получение объекта plannerTask](../api/plannertask-get.md) | [plannerTask](plannertask.md) |Чтение свойств и отношений объекта **plannerTask**.|
|[Обновление](../api/plannertask-update.md) | [plannerTask](plannertask.md) |Обновление объекта **plannerTask**. |
|[Удаление](../api/plannertask-delete.md) | Нет |Удаление объекта **plannerTask**. |

## <a name="properties"></a>Свойства
| Свойство     | Тип   |Описание|
|:---------------|:--------|:----------|
|activeChecklistItemCount|Int32|Количество элементов контрольного списка со значением `false`, указывающим, что задача не выполнена.|
|appliedCategories|[plannerAppliedCategories](plannerappliedcategories.md)|Категории, к которым применена задача. Возможные значения см. [здесь](plannerappliedcategories.md).|
|assigneePriority|String|Указание, используемое для упорядочивания элементов этого типа в списке. Формат определяется, как описано [здесь](planner-order-hint-format.md).|
|assignments|[plannerAssignments](plannerassignments.md)|Список исполнителей, которым назначена задача.|
|bucketId|Строка|Идентификатор сегмента, к которому относится задача. Сегмент должен находиться в том же плане, что и задача. Содержит 28 знаков, учитывается регистр. [Проверка формата](tasks-identifiers-disclaimer.md) проводится для службы. |
|checklistItemCount|Int32|Количество элементов контрольного списка, представленных в задаче.|
|completedBy|[identitySet](identityset.md)|Идентификатор пользователя, который выполнил задачу.|
|completedDateTime|DateTimeOffset|Только для чтения. Дата и время присвоения свойству задачи `'percentComplete'` значения `'100'`. Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда используется формат UTC). Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`|
|conversationThreadId|Строка|Идентификатор разговора о задаче. Это идентификатор объекта разговора, созданного в группе.|
|createdBy|[identitySet](identityset.md)|Идентификатор пользователя, создавшего задачу.|
|createdDateTime|DateTimeOffset|Только для чтения. Дата и время создания задачи. Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда используется формат UTC). Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`.|
|dueDateTime|DateTimeOffset|Срок выполнения задачи. Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда используется формат UTC). Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`.|
|hasDescription|Boolean|Только для чтения. Значение — `true`, если объект details задачи имеет описание. В противном случае — `false`.|
|id|String|Только для чтения. Идентификатор задачи. Содержит 28 знаков, учитывается регистр. [Проверка формата](tasks-identifiers-disclaimer.md) проводится для службы.|
|orderHint|String|Указание, используемое для упорядочивания элементов этого типа в списке. Формат определяется, как описано [здесь](planner-order-hint-format.md).|
|percentComplete|Int32|Процент выполнения задачи. Если установлено значение `100`, задача считается выполненной. |
|priority|Int32|Приоритет задачи. Допустимый диапазон значений: между `0` и `10` (включительно), при котором увеличивается значение низкого приоритета ( `0` имеет самый высокий приоритет и `10` имеет самый низкий приоритет).  В настоящее время планировщик интерпретирует значения `0` , а также как " `1` срочные", а также "средний", " `2` `3` средний" и " `4` `5` `6` `7` средний", а также "средний" `8` `9` `10` .  В настоящее время планировщик устанавливает значение `1` "срочно", " `3` важно", `5` "среднее" и `9` "недорогой".|
|planId|Строка|Идентификатор плана, к которому относится задача.|
|previewType|String|Устанавливает тип предварительного просмотра задачи. Возможные значения: `automatic`, `noPreview`, `checklist`, `description`, `reference`.|
|referenceCount|Int32|Количество внешних ссылок на задачу.|
|startDateTime|DateTimeOffset|Дата и время начала задачи. Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда используется формат UTC). Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: `'2014-01-01T00:00:00Z'`.|
|title|Строка|Название задачи.|

## <a name="relationships"></a>Связи
| Связь | Тип   |Описание|
|:---------------|:--------|:----------|
|assignedToTaskBoardFormat|[plannerAssignedToTaskBoardTaskFormat](plannerassignedtotaskboardtaskformat.md);| Только для чтения. Допускает значение null. Используется для правильного отображения задачи на доске задач при сортировке по свойству assignedTo.|
|bucketTaskBoardFormat|[plannerBucketTaskBoardTaskFormat](plannerbuckettaskboardtaskformat.md);| Только для чтения. Допускает значение null. Используется для правильного отображения задачи на доске задач при сортировке по сегменту.|
|подробности|[plannerTaskDetails](plannertaskdetails.md);| Только для чтения. Допускает значение null. Дополнительные сведения о задаче.|
|progressTaskBoardFormat|[plannerProgressTaskBoardTaskFormat](plannerprogresstaskboardtaskformat.md).| Только для чтения. Допускает значение null. Используется для правильного отображения задачи на доске задач при сортировке по ходу выполнения.|

## <a name="json-representation"></a>Представление в формате JSON
Ниже представлено описание ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "keyProperty": "id",
  "baseType":"microsoft.graph.entity",  
  "@odata.type": "microsoft.graph.plannerTask"
}-->

```json
{
  "activeChecklistItemCount": 1024,
  "appliedCategories": {"@odata.type": "microsoft.graph.plannerAppliedCategories"},
  "assigneePriority": "String",
  "assignments": {"@odata.type": "microsoft.graph.plannerAssignments"},
  "bucketId": "String",
  "checklistItemCount": 1024,
  "completedBy": {"@odata.type": "microsoft.graph.identitySet"},
  "completedDateTime": "String (timestamp)",
  "conversationThreadId": "String",
  "createdBy": {"@odata.type": "microsoft.graph.identitySet"},
  "createdDateTime": "String (timestamp)",
  "dueDateTime": "String (timestamp)",
  "hasDescription": true,
  "id": "String (identifier)",
  "orderHint": "String",
  "percentComplete": 1024,
  "priority": 1024,
  "planId": "String",
  "previewType": "String",
  "referenceCount": 1024,
  "startDateTime": "String (timestamp)",
  "title": "String"
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "plannerTask resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


