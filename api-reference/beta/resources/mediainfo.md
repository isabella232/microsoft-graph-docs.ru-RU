---
title: Тип ресурса mediaInfo
description: Запрашивает сведения о мультимедиа, используемые в действиях для.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 65cf71f5c116fe213d0e32d560ec24704bff1172
ms.sourcegitcommit: 3d24047b3af46136734de2486b041e67a34f3d83
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2019
ms.locfileid: "29523983"
---
# <a name="mediainfo-resource-type"></a><span data-ttu-id="dd1ea-103">Тип ресурса mediaInfo</span><span class="sxs-lookup"><span data-stu-id="dd1ea-103">mediaInfo resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="dd1ea-104">Запрашивает сведения о мультимедиа, используемые в действиях для.</span><span class="sxs-lookup"><span data-stu-id="dd1ea-104">The media information used in actions for prompts.</span></span>

## <a name="properties"></a><span data-ttu-id="dd1ea-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="dd1ea-105">Properties</span></span>
| <span data-ttu-id="dd1ea-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="dd1ea-106">Property</span></span>       | <span data-ttu-id="dd1ea-107">Тип</span><span class="sxs-lookup"><span data-stu-id="dd1ea-107">Type</span></span>    | <span data-ttu-id="dd1ea-108">Описание</span><span class="sxs-lookup"><span data-stu-id="dd1ea-108">Description</span></span>                      |
|:---------------|:--------|:---------------------------------|
| <span data-ttu-id="dd1ea-109">resourceId</span><span class="sxs-lookup"><span data-stu-id="dd1ea-109">resourceId</span></span>     | <span data-ttu-id="dd1ea-110">String</span><span class="sxs-lookup"><span data-stu-id="dd1ea-110">String</span></span>  | <span data-ttu-id="dd1ea-111">Уникальный идентификатор ресурса.</span><span class="sxs-lookup"><span data-stu-id="dd1ea-111">Unique identity of the resource.</span></span> |
| <span data-ttu-id="dd1ea-112">URI</span><span class="sxs-lookup"><span data-stu-id="dd1ea-112">uri</span></span>            | <span data-ttu-id="dd1ea-113">String</span><span class="sxs-lookup"><span data-stu-id="dd1ea-113">String</span></span>  | <span data-ttu-id="dd1ea-114">Путь к ресурсу.</span><span class="sxs-lookup"><span data-stu-id="dd1ea-114">Path to the resource.</span></span>            |

## <a name="json-representation"></a><span data-ttu-id="dd1ea-115">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="dd1ea-115">JSON representation</span></span>

<span data-ttu-id="dd1ea-116">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="dd1ea-116">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mediaInfo"
}-->
```json
{
  "resourceId": "String",
  "uri": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "mediaInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/mediainfo.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
