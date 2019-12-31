---
title: Тип ресурса Митингинфо
description: Сведения о собрании, указанные для создания или присоединения к собранию.
author: ananmishr
localization_priority: Normal
ms.prod: cloud-communications
doc_type: resourcePageType
ms.openlocfilehash: b6ed682e063ce1f9b2d780a547a8de1856c6dbd0
ms.sourcegitcommit: 636671293b0be89088459c4fc8a5e661341b37cf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/31/2019
ms.locfileid: "40913396"
---
# <a name="meetinginfo-resource-type"></a>Тип ресурса Митингинфо

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

Это абстрактный класс, который содержит сведения о собрании.
 
Чтобы присоединиться к существующему собранию, необходимо либо указать [организермитингинфо](organizermeetinginfo.md) в сочетании с [чатинфо](./chatinfo.md), либо только с [токенмитингинфо](tokenmeetinginfo.md).


## <a name="derived-types"></a>Производные типы

| Тип                                                 | Описание                                                         |
|:-----------------------------------------------------|:--------------------------------------------------------------------|
| [организермитингинфо](./organizermeetinginfo.md)    | Сведения об организаторе собрания                          |
| [токенмитингинфо](tokenmeetinginfo.md)              | Зашифрованный маркер, содержащий сведения о собрании  |

## <a name="json-representation"></a>Представление JSON

Ниже указано представление ресурса в формате JSON.

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingInfo"
}-->
```json
{
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "meetingInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
