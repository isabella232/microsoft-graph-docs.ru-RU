---
title: Тип ресурса Медиаконфиг
description: Конфигурация мультимедиа, используемая для подключения к вызову.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: e4f6e940cd319d10cd3f03e3c94d0473164beb29
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32562554"
---
# <a name="mediaconfig-resource-type"></a><span data-ttu-id="5aff0-103">Тип ресурса Медиаконфиг</span><span class="sxs-lookup"><span data-stu-id="5aff0-103">mediaConfig resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="5aff0-104">Конфигурация мультимедиа, используемая для подключения к вызову.</span><span class="sxs-lookup"><span data-stu-id="5aff0-104">The media configuration used to connect to a call.</span></span>

## <a name="properties"></a><span data-ttu-id="5aff0-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="5aff0-105">Properties</span></span>

| <span data-ttu-id="5aff0-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="5aff0-106">Property</span></span>       | <span data-ttu-id="5aff0-107">Тип</span><span class="sxs-lookup"><span data-stu-id="5aff0-107">Type</span></span>    | <span data-ttu-id="5aff0-108">Описание</span><span class="sxs-lookup"><span data-stu-id="5aff0-108">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="5aff0-109">Ремовефромдефаултаудиограуп</span><span class="sxs-lookup"><span data-stu-id="5aff0-109">removeFromDefaultAudioGroup</span></span> | <span data-ttu-id="5aff0-110">Boolean</span><span class="sxs-lookup"><span data-stu-id="5aff0-110">Boolean</span></span> |  |

## <a name="json-representation"></a><span data-ttu-id="5aff0-111">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="5aff0-111">JSON representation</span></span>

<span data-ttu-id="5aff0-112">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="5aff0-112">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "removeFromDefaultAudioGroup"
  ],
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
  "suppressions": [
    "Error: /api-reference/beta/resources/mediaconfig.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
