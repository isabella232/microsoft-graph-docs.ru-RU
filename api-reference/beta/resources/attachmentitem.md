---
title: Тип ресурса Аттачментитем
description: Представляет атрибуты элемента, который необходимо присоединить.
localization_priority: Normal
author: svpsiva
ms.prod: outlook
doc_type: resourcePageType
ms.openlocfilehash: 14213afcaf555b21816a3b3ccf2481c1555c4b90
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48040180"
---
# <a name="attachmentitem-resource-type"></a>Тип ресурса Аттачментитем

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет атрибуты элемента, который необходимо присоединить.

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|attachmentType|String| Тип вложения. Возможные значения: `file`, `item`, `reference`. Обязательное.|
|contentType|String|Характер данных во вложении. Необязательный.|
|isInline|Boolean|Значение `true`, если вложение является встроенным. В противном случае — значение `false`. Необязательный.|
|name|String|Отображаемое имя вложения. Это может быть строка с описанием и не обязательно должно быть фактическим именем файла. Обязательный.|
|size|Int64|Размер вложения в байтах. Обязательный элемент.|

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "contentType",
    "isInline"
  ],
  "@odata.type": "microsoft.graph.attachmentItem",
  "baseType": null
}-->

```json
{
  "attachmentType": "String",
  "contentType": "String",
  "isInline": true,
  "name": "String",
  "size": 1024
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attachmentItem resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

