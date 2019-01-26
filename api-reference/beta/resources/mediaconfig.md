---
title: Тип ресурса mediaConfig
description: Конфигурация мультимедиа, используемый для подключения к звонку.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 0b2d8b8063307660b0d4cce459e1906f0b0a99c5
ms.sourcegitcommit: 66066b71d353fd7c2481d43b1dba2c33390eee61
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/26/2019
ms.locfileid: "29573965"
---
# <a name="mediaconfig-resource-type"></a><span data-ttu-id="67670-103">Тип ресурса mediaConfig</span><span class="sxs-lookup"><span data-stu-id="67670-103">mediaConfig resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="67670-104">Конфигурация мультимедиа, используемый для подключения к звонку.</span><span class="sxs-lookup"><span data-stu-id="67670-104">The media configuration used to connect to a call.</span></span>

## <a name="properties"></a><span data-ttu-id="67670-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="67670-105">Properties</span></span>

| <span data-ttu-id="67670-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="67670-106">Property</span></span>       | <span data-ttu-id="67670-107">Тип</span><span class="sxs-lookup"><span data-stu-id="67670-107">Type</span></span>    | <span data-ttu-id="67670-108">Описание</span><span class="sxs-lookup"><span data-stu-id="67670-108">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="67670-109">removeFromDefaultAudioGroup</span><span class="sxs-lookup"><span data-stu-id="67670-109">removeFromDefaultAudioGroup</span></span> | <span data-ttu-id="67670-110">Boolean</span><span class="sxs-lookup"><span data-stu-id="67670-110">Boolean</span></span> |  |

## <a name="json-representation"></a><span data-ttu-id="67670-111">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="67670-111">JSON representation</span></span>

<span data-ttu-id="67670-112">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="67670-112">The following is a JSON representation of the resource.</span></span>

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
  "suppressions": [
    "Error: /api-reference/beta/resources/mediaconfig.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
