---
title: Тип ресурсов locationConstraint
description: Условия, заданные клиентом в отношении расположения для проведения собрания.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
doc_type: resourcePageType
ms.openlocfilehash: f79f6243d996193aacee66c8955ce49c8b779482
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48073592"
---
# <a name="locationconstraint-resource-type"></a>Тип ресурсов locationConstraint

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Условия, заданные клиентом в отношении расположения для проведения собрания.

## <a name="json-representation"></a>Представление JSON

Ниже показано представление JSON ресурса.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.locationConstraint"
}-->

```json
{
  "isRequired": true,
  "locations": [{"@odata.type": "microsoft.graph.locationConstraintItem"}],
  "suggestLocation": true
}

```
## <a name="properties"></a>Свойства
| Свойство     | Тип   |Описание|
|:---------------|:--------|:----------|
|isRequired|Boolean|Клиент запрашивает у службы включение в отклик данных о расположении для проведения собрания. Если задано значение true и все ресурсы заняты, [findMeetingTimes](../api/user-findmeetingtimes.md) не вернет вариантов времени для проведения собрания. Если задано значение false и все ресурсы заняты, **findMeetingTimes** все равно будет искать варианты времени для проведения собрания, но без указания расположений. |
|locations|Коллекция [locationConstraintItem](locationconstraintitem.md)|Ограниченные сведения об одном или нескольких расположениях, которые клиент запрашивает для собрания.|
|сугжестлокатион|Boolean|Клиент запрашивает у службы один или несколько вариантов расположений для проведения собрания.|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "locationConstraint resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->


