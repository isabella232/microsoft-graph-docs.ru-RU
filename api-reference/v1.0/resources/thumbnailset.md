---
author: JeremyKelley
ms.author: JeremyKelley
ms.date: 09/10/2017
title: ThumbnailSet
localization_priority: Normal
description: Ресурс ThumbnailSet представляет собой коллекцию ресурсов thumbnail с ключами.
ms.prod: ''
doc_type: resourcePageType
ms.openlocfilehash: 5aa7ca5646ea0555c0f6547e7171312537343345
ms.sourcegitcommit: acdf972e2f25fef2c6855f6f28a63c0762228ffa
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/18/2020
ms.locfileid: "48090860"
---
# <a name="thumbnailset-resource-type"></a>Тип ресурса ThumbnailSet

Пространство имен: microsoft.graph

Ресурс **ThumbnailSet** представляет собой коллекцию ресурсов [thumbnail](thumbnail.md) с ключами. Он представляет набор эскизов, связанных с ресурсом DriveItem.

## <a name="json-representation"></a>Представление JSON

Ниже представлено описание ресурса в формате JSON.

<!--{
  "blockType": "resource",
  "optionalProperties": [
    "source",
    "small",
    "medium",
    "large"
  ],
  "keyProperty": "id",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.thumbnailSet",
  "openType": true
}-->

```json
{
  "id": "string (identifier)",
  "large": { "@odata.type": "microsoft.graph.thumbnail" },
  "medium": { "@odata.type": "microsoft.graph.thumbnail" },
  "small": { "@odata.type": "microsoft.graph.thumbnail" },
  "source": { "@odata.type": "microsoft.graph.thumbnail" }
}
```

## <a name="properties"></a>Свойства

| Свойство | Тип                      | Описание                                                                       |
|:---------|:--------------------------|:----------------------------------------------------------------------------------|
| id       | Строка                    | Идентификатор в элементе. Только для чтения.                                                |
| large    | [Thumbnail](thumbnail.md) | Эскиз размером 1920x1920.                                                     |
| medium   | [Thumbnail](thumbnail.md) | Эскиз размером 176x176.                                                       |
| small    | [Thumbnail](thumbnail.md) | Обрезанный эскиз размером 48x48.                                                        |
| source   | [Thumbnail](thumbnail.md) | Пользовательский эскиз исходного изображения, используемого для создания других эскизов. |

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "ThumbnailSet enables access to thumbnails of different sizes",
  "section": "documentation",
  "tocPath": "Resources/ThumbnailSet"
} -->

