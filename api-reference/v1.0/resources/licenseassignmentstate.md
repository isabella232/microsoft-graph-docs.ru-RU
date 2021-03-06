---
title: Тип ресурса Лиценсеассигнментстате
description: Свойство **лиценсеассигнментстатес** объекта User — коллекция объектов **лиценсеассигнментстате** . Он предоставляет пользователю сведения о назначении лицензий пользователю.
author: dkershaw10
localization_priority: Normal
ms.prod: groups
doc_type: resourcePageType
ms.openlocfilehash: b26ab4be63cbb40929dbea3f40522ee4c6b7ff70
ms.sourcegitcommit: 577bfd3bb8a2e2679ef1c5942a4a496c2aa3a277
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/17/2020
ms.locfileid: "48582186"
---
# <a name="licenseassignmentstate-resource-type"></a>Тип ресурса Лиценсеассигнментстате

Пространство имен: microsoft.graph


Свойство **лиценсеассигнментстатес** объекта [User](user.md) — коллекция объектов **лиценсеассигнментстате** . Он предоставляет пользователю сведения о назначении лицензий пользователю. Сведения включают следующие сведения:  

- Какие планы отключены для пользователя
- Указывает, была ли лицензия назначена пользователю напрямую или унаследована от группы.
- Текущее состояние назначения
- Сведения об ошибке, если состояние назначения — ошибка 


## <a name="properties"></a>Свойства
| Свойство     | Тип   |Описание|
|:---------------|:--------|:----------|
|ассигнедбиграуп|Строка|Идентификатор группы, которая назначает эту лицензию. Если назначение относится к прямой назначенной лицензии, это поле будет иметь значение null. Только для чтения.|
|дисабледпланс|Collection(String)|Планы обслуживания, которые отключены в этом назначении. Только для чтения.|
|error|String|Ошибка при назначении лицензии. Если лицензия назначена успешно, это поле будет иметь значение null. Только для чтения. Возможные значения: `CountViolation` , `MutuallyExclusiveViolation` , `DependencyViolation` , `ProhibitedInUsageLocationViolation` , `UniquenessViolation` и `Others` . Дополнительные сведения о том, как определять и устранять ошибки назначения лицензий, можно найти [здесь](/azure/active-directory/users-groups-roles/licensing-groups-resolve-problems).|
|skuId|String|Уникальный идентификатор SKU. Только для чтения.|
|state|String|Указывает текущее состояние этого назначения. Только для чтения. Возможные значения: Active, Активевисеррор, Disabled и Error.|

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

```json
{
  "assignedByGroup": "String",
  "disabledPlans": "Collection(String)",
  "error": " String ",  
  "skuId": "String ",
  "state": "String"
}

```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79 2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "licenseAssignmentState resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: microsoft.graph.user/licenseAssignmentStates:
      Referenced type microsoft.graph.licenseAssignmentState is not defined in the doc set! Potential suggestion: UNKNOWN"
  ]
}-->