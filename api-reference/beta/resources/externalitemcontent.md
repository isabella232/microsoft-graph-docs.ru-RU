---
title: Тип ресурса Екстерналитемконтент
description: Содержимое элемента, индексируемого с помощью подключения Microsoft Search.
localization_priority: Normal
author: snlraju-msft
ms.prod: search
doc_type: resourcePageType
ms.openlocfilehash: a9121648f35dd09d8fb87d4738bb2bf6e9b3960b
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "47998812"
---
# <a name="externalitemcontent-resource-type"></a>Тип ресурса Екстерналитемконтент

Пространство имен: microsoft.graph

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Содержимое объекта [екстерналитем](externalitem.md) , индексируемого с помощью [подключения](externalconnection.md)Microsoft Search.

[!INCLUDE [search-api-preview](../../includes/search-api-preview-signup.md)]

## <a name="properties"></a>Свойства

| Свойство | Тип   | Описание                                                                                 |
|:---------|:-------|:--------------------------------------------------------------------------------------------|
| значение    | String | Содержимое для Екстерналитем. Обязательное.                                                 |
| type     | String | Тип контента в свойстве Value. Возможные значения: `text` и `html`. Обязательно. |

## <a name="relationships"></a>Связи

Нет

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.externalItemContent",
  "baseType": ""
}-->

```json
{
  "value": "String",
  "type": "String"
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "externalItemContent resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}-->


