---
title: Тип ресурса Воркбукворкшитпротектионоптионс
description: Представляет параметры защиты листа.
author: lumine2008
localization_priority: Normal
ms.prod: excel
doc_type: resourcePageType
ms.openlocfilehash: bac52b26863af7247ab0fa3b08b87c56f401fc43
ms.sourcegitcommit: 272996d2772b51105ec25f1cf7482ecda3b74ebe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "42519094"
---
# <a name="workbookworksheetprotectionoptions-resource-type"></a>Тип ресурса Воркбукворкшитпротектионоптионс

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

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
<!--
{
  "type": "#page.annotation",
  "description": "workbookWorksheetProtectionOptions resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
