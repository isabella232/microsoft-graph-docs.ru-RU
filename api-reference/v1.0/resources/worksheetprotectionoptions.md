---
title: Тип ресурса WorksheetProtectionOptions
description: Представляет параметры защиты листа.
author: lumine2008
localization_priority: Normal
ms.prod: excel
doc_type: resourcePageType
ms.openlocfilehash: 8bc4745f31d5b2a6cffe89a4fb912739212a6c3e
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48015010"
---
# <a name="worksheetprotectionoptions-resource-type"></a>Тип ресурса WorksheetProtectionOptions

Пространство имен: microsoft.graph

Представляет параметры защиты листа.

## <a name="properties"></a>Свойства
| Свойство     | Тип   |Описание|
|:---------------|:--------|:----------|
|allowAutoFilter|boolean|Представляет параметр защиты листа, разрешающий использовать функцию автофильтра.|
|allowDeleteColumns|boolean|Представляет параметр защиты листа, разрешающий удалять столбцы.|
|allowDeleteRows|boolean|Представляет параметр защиты листа, разрешающий удалять строки.|
|allowFormatCells|boolean|Представляет параметр защиты листа, разрешающий форматировать ячейки.|
|allowFormatColumns|boolean|Представляет параметр защиты листа, разрешающий форматировать столбцы.|
|allowFormatRows|boolean|Представляет параметр защиты листа, разрешающий форматировать строки.|
|allowInsertColumns|boolean|Представляет параметр защиты листа, разрешающий вставлять столбцы.|
|allowInsertHyperlinks|boolean|Представляет параметр защиты листа, разрешающий вставлять гиперссылки.|
|allowInsertRows|boolean|Представляет параметр защиты листа, разрешающий вставлять строки.|
|allowPivotTables|boolean|Представляет параметр защиты листа, разрешающий использовать функцию сводных таблиц.|
|allowSort|boolean|Представляет параметр защиты листа, разрешающий использовать функцию сортировки.|

## <a name="json-representation"></a>Представление JSON

Ниже представлено описание ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.workbookWorksheetProtectionOptions"
}-->

```json
{
  "allowAutoFilter": true,
  "allowDeleteColumns": true,
  "allowDeleteRows": true,
  "allowFormatCells": true,
  "allowFormatColumns": true,
  "allowFormatRows": true,
  "allowInsertColumns": true,
  "allowInsertHyperlinks": true,
  "allowInsertRows": true,
  "allowPivotTables": true,
  "allowSort": true
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "WorksheetProtectionOptions resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

