---
title: Тип ресурса Медиаконфиг
description: Конфигурация мультимедиа, используемая для подключения к вызову.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
doc_type: resourcePageType
ms.openlocfilehash: 4d00470d517c4d701a028a1911efe02a6f441639
ms.sourcegitcommit: 2c62457e57467b8d50f21b255b553106a9a5d8d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/31/2019
ms.locfileid: "36009778"
---
# <a name="mediaconfig-resource-type"></a><span data-ttu-id="98632-103">Тип ресурса Медиаконфиг</span><span class="sxs-lookup"><span data-stu-id="98632-103">mediaConfig resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="98632-104">Конфигурация мультимедиа, используемая для подключения к вызову.</span><span class="sxs-lookup"><span data-stu-id="98632-104">The media configuration used to connect to a call.</span></span>

## <a name="properties"></a><span data-ttu-id="98632-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="98632-105">Properties</span></span>

| <span data-ttu-id="98632-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="98632-106">Property</span></span>       | <span data-ttu-id="98632-107">Тип</span><span class="sxs-lookup"><span data-stu-id="98632-107">Type</span></span>    | <span data-ttu-id="98632-108">Описание</span><span class="sxs-lookup"><span data-stu-id="98632-108">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="98632-109">Ремовефромдефаултаудиограуп</span><span class="sxs-lookup"><span data-stu-id="98632-109">removeFromDefaultAudioGroup</span></span> | <span data-ttu-id="98632-110">Boolean</span><span class="sxs-lookup"><span data-stu-id="98632-110">Boolean</span></span> |  |

## <a name="json-representation"></a><span data-ttu-id="98632-111">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="98632-111">JSON representation</span></span>

<span data-ttu-id="98632-112">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="98632-112">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "removeFromDefaultAudioGroup"
   ],
  "abstract": true,
  "@odata.type": "microsoft.graph.mediaConfig"
}-->
```json
{
  "removeFromDefaultAudioGroup": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "mediaConfig resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
