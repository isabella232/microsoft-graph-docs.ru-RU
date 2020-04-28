---
title: Тип ресурса Шифтактивити
description: Представляет действие в смене.
author: nkramer
localization_priority: Normal
ms.prod: microsoft-teams
doc_type: resourcePageType_
ms.openlocfilehash: 6adc82eca2c7ce53713997c18001aef19c76e3dc
ms.sourcegitcommit: 272996d2772b51105ec25f1cf7482ecda3b74ebe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "42520634"
---
# <a name="shiftactivity-resource-type"></a>Тип ресурса Шифтактивити

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет действие в [смене](shift.md).

## <a name="properties"></a>Свойства
| Свойство                         | Тип                    | Описание                                                                                                                                                                        |
|------------------------------|-------------------------|---------------------------------------------------------------------------------------------|
| Предопл               | `bool`                  | Указывает, следует `microsoft.graph.user` ли платить за действие в течение этого периода `shift`. Обязательный.    |
| startDateTime               | `DateTimeOffset`                  | Дата и время начала для ресурса `shiftActivity`. Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда применяется формат UTC). Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: "2014-01-01T00:00:00Z". Обязательный элемент. |
| endDateTime               | `DateTimeOffset`                  | Дата и время окончания для ресурса `shiftActivity`. Тип Timestamp представляет сведения о времени и дате с использованием формата ISO 8601 (всегда применяется формат UTC). Например, значение полуночи 1 января 2014 г. в формате UTC выглядит так: "2014-01-01T00:00:00Z". Обязательный элемент.    |
| code               | `string`                  | Определенный пользователем код для `shiftActivity`. Обязательный.    |
| displayName               | `string`                  | Имя ресурса `shiftActivity`. Обязательный элемент.    |

## <a name="json-representation"></a>Представление JSON

Ниже представлено описание ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "keyProperty": "id",
  "@odata.type": "microsoft.graph.shiftActivity"
}-->
```json
{
  "isPaid": true,
  "startDateTime": "2019-03-11T15:00:00Z",
  "endDateTime": "2019-03-11T15:15:00Z",
  "code": "",
  "displayName": "Lunch"
}
```


<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "shiftActivity resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
