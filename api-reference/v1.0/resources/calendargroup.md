---
title: Тип ресурса calendarGroup
description: Группа пользовательских календарей.
author: harini84
localization_priority: Normal
ms.prod: outlook
doc_type: resourcePageType
ms.openlocfilehash: 7a78daf6f0e1dd1cd4a271e89b19d541fbe32d0d
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48043929"
---
# <a name="calendargroup-resource-type"></a>Тип ресурса calendarGroup

Пространство имен: microsoft.graph

Группа пользовательских календарей.

## <a name="methods"></a>Методы

| Метод                                                      | Возвращаемый тип                        | Описание                                                   |
| :---------------------------------------------------------- | :--------------------------------- | :------------------------------------------------------------ |
| [Список групп календарей](../api/user-list-calendargroups.md)  | Коллекция объектов [Calendar](calendar.md) | Получение групп календарей пользователя.                               |
| [Создание группы календарей](../api/user-post-calendargroups.md) | [Calendar](calendar.md)            | Создание группы календарей.                                  |
| [Получение группы календарей](../api/calendargroup-get.md)           | [calendarGroup](calendargroup.md)  | Чтение свойств и связей, принадлежащих объекту группы календарей. |
| [Обновление](../api/calendargroup-update.md)                    | [calendarGroup](calendargroup.md)  | Обновление объекта calendarGroup.                                  |
| [удаление](../api/calendargroup-delete.md);                    | Нет                               | Удаление объекта calendarGroup.                                  |
| [Список календарей](../api/calendargroup-list-calendars.md)    | Коллекция [Calendar](calendar.md) | Список календарей в группе календарей.                           |
| [Создание объекта Calendar](../api/calendargroup-post-calendars.md)   | [Calendar](calendar.md)            | Создание календаря в группе календарей.                    |

## <a name="properties"></a>Свойства

| Свойство  | Тип   | Описание                                                                                                                                                                                               |
| :-------- | :----- | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| name      | String | Имя группы.                                                                                                                                                                                           |
| changeKey | String | Указывает версию группы календарей. При каждом изменении группы календарей также меняется значение ChangeKey. Благодаря этому Exchange может применять изменения к правильной версии объекта. Только для чтения. |
| classId   | Guid   | Идентификатор класса. Только для чтения.                                                                                                                                                                          |
| id        | Строка | Уникальный идентификатор группы. Только для чтения.                                                                                                                                                                 |

## <a name="relationships"></a>Связи

| Связь | Тип                               | Описание                                                                    |
| :----------- | :--------------------------------- | :----------------------------------------------------------------------------- |
| calendars    | Коллекция [Calendar](calendar.md) | Календари в группе календарей. Свойство навигации. Только для чтения. Допускается значение null. |

## <a name="json-representation"></a>Представление JSON

Ниже представлено описание ресурса в формате JSON.

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "calendars"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.calendarGroup",
  "@odata.annotations": [
    {
      "property": "calendars",
      "capabilities": {
        "changeTracking": false,
        "expandable": false,
        "navigability": "single",
        "searchable": false
      }
    }
  ]
}-->

```json
{
  "changeKey": "string",
  "classId": "guid",
  "id": "string (identifier)",
  "name": "string"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->

<!-- {
  "type": "#page.annotation",
  "description": "calendarGroup resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

