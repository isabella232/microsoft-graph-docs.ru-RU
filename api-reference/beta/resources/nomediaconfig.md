---
title: Тип ресурса noMediaConfig
description: Конфигурация мультимедиа, указывающие нет носителя.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 8d564493889cc367ecdb697ce4031c40a4cbbbef
ms.sourcegitcommit: d95f6d39a0479da6e531f3734c4029dc596b9a3f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2019
ms.locfileid: "29641318"
---
# <a name="nomediaconfig-resource-type"></a><span data-ttu-id="cb416-103">Тип ресурса noMediaConfig</span><span class="sxs-lookup"><span data-stu-id="cb416-103">noMediaConfig resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="cb416-104">Конфигурация мультимедиа, указывающие нет носителя.</span><span class="sxs-lookup"><span data-stu-id="cb416-104">Media configuration for indicating no media.</span></span>

## <a name="properties"></a><span data-ttu-id="cb416-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="cb416-105">Properties</span></span>

| <span data-ttu-id="cb416-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="cb416-106">Property</span></span>       | <span data-ttu-id="cb416-107">Тип</span><span class="sxs-lookup"><span data-stu-id="cb416-107">Type</span></span>    | <span data-ttu-id="cb416-108">Описание</span><span class="sxs-lookup"><span data-stu-id="cb416-108">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="cb416-109">removeFromDefaultAudioGroup</span><span class="sxs-lookup"><span data-stu-id="cb416-109">removeFromDefaultAudioGroup</span></span> | <span data-ttu-id="cb416-110">Boolean</span><span class="sxs-lookup"><span data-stu-id="cb416-110">Boolean</span></span> |  |

## <a name="json-representation"></a><span data-ttu-id="cb416-111">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="cb416-111">JSON representation</span></span>

<span data-ttu-id="cb416-112">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="cb416-112">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.noMediaConfig"
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
  "description": "noMediaConfig resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/nomediaconfig.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
