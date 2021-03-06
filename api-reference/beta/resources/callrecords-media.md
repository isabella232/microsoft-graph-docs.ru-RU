---
title: Тип ресурса мультимедиа
description: Тип мультимедиа
localization_priority: Normal
author: williamlooney
ms.prod: cloud-communications
doc_type: resourcePageType
ms.openlocfilehash: 9245d9c030c15d17b286338aa7887333b26f2678
ms.sourcegitcommit: af4b2fc18449c33979cf6d75bd680f40602ba708
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/20/2020
ms.locfileid: "48601176"
---
# <a name="media-resource-type"></a>Тип ресурса мультимедиа

Пространство имен: microsoft.graph.callRecords

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Представляет мультимедиа (звук, видео, Видеообмен на экране и т. д.), используемые при вызове.

## <a name="properties"></a>Свойства

| Свойство     | Тип        | Описание |
|:-------------|:------------|:------------|
|label|String|Способ идентификации мультимедиа во время этапа согласования мультимедиа.|
|каллердевице|[Microsoft. Graph. Каллрекордс. Девицеинфо](callrecords-deviceinfo.md)|Сведения об устройстве, связанные с конечной точкой абонента этого носителя.|
|каллернетворк|[Microsoft. Graph. Каллрекордс. Нетворкинфо](callrecords-networkinfo.md)|Сведения о сети, связанные с конечной точкой абонента этого носителя.|
|каллидевице|[Microsoft. Graph. Каллрекордс. Девицеинфо](callrecords-deviceinfo.md)|Сведения об устройстве, связанные с конечной точкой вызываемого носителя.|
|каллинетворк|[Microsoft. Graph. Каллрекордс. Нетворкинфо](callrecords-networkinfo.md)|Сведения о сети, связанные с конечной точкой вызываемого носителя.|
|представлений|Коллекция [Microsoft. Graph. каллрекордс. медиастреам](callrecords-mediastream.md)|Сетевые потоки, связанные с этим носителем.|

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.callRecords.media",
  "baseType": null
}-->

```json
{
  "label": "String",
  "callerDevice": {"@odata.type": "microsoft.graph.callRecords.deviceInfo"},
  "callerNetwork": {"@odata.type": "microsoft.graph.callRecords.networkInfo"},
  "calleeDevice": {"@odata.type": "microsoft.graph.callRecords.deviceInfo"},
  "calleeNetwork": {"@odata.type": "microsoft.graph.callRecords.networkInfo"},
  "streams": [{"@odata.type": "microsoft.graph.callRecords.mediaStream"}]
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "media resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->

