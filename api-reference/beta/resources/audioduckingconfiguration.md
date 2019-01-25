---
title: Тип ресурса audioDuckingConfiguration
description: Параметры для Уклонение от других источников, (синхронизацию и выходить из нее других источников).
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: d61e4150250df25e020f45a65676d1c55c0e4c9d
ms.sourcegitcommit: 3d24047b3af46136734de2486b041e67a34f3d83
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2019
ms.locfileid: "29522464"
---
# <a name="audioduckingconfiguration-resource-type"></a><span data-ttu-id="f9e22-103">Тип ресурса audioDuckingConfiguration</span><span class="sxs-lookup"><span data-stu-id="f9e22-103">audioDuckingConfiguration resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="f9e22-104">Параметры для Уклонение от других источников, (синхронизацию и выходить из нее других источников).</span><span class="sxs-lookup"><span data-stu-id="f9e22-104">Parameters for ducking of other sources (phasing in and out of other sources.)</span></span>

## <a name="properties"></a><span data-ttu-id="f9e22-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="f9e22-105">Properties</span></span>

| <span data-ttu-id="f9e22-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="f9e22-106">Property</span></span>      | <span data-ttu-id="f9e22-107">Тип</span><span class="sxs-lookup"><span data-stu-id="f9e22-107">Type</span></span>     | <span data-ttu-id="f9e22-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f9e22-108">Description</span></span>                                                                     |
| :------------ | :------- | :-------------------------------------------------------------------------------|
| <span data-ttu-id="f9e22-109">lowerLevel</span><span class="sxs-lookup"><span data-stu-id="f9e22-109">lowerLevel</span></span>    | <span data-ttu-id="f9e22-110">Int64</span><span class="sxs-lookup"><span data-stu-id="f9e22-110">Int64</span></span>    | <span data-ttu-id="f9e22-111">Объем источников в процентах, когда источники которые ducked.</span><span class="sxs-lookup"><span data-stu-id="f9e22-111">The volume of sources in percent when the sources are being ducked.</span></span>             |
| <span data-ttu-id="f9e22-112">rampActive</span><span class="sxs-lookup"><span data-stu-id="f9e22-112">rampActive</span></span>    | <span data-ttu-id="f9e22-113">Int64</span><span class="sxs-lookup"><span data-stu-id="f9e22-113">Int64</span></span>    | <span data-ttu-id="f9e22-114">Количество времени (в миллисекундах), необходимое для ducked источников, чтобы «сделать».</span><span class="sxs-lookup"><span data-stu-id="f9e22-114">The amount of time (in milliseconds) it takes for ducked sources to "fade out".</span></span> |
| <span data-ttu-id="f9e22-115">rampInactive</span><span class="sxs-lookup"><span data-stu-id="f9e22-115">rampInactive</span></span>  | <span data-ttu-id="f9e22-116">Int64</span><span class="sxs-lookup"><span data-stu-id="f9e22-116">Int64</span></span>    | <span data-ttu-id="f9e22-117">Количество времени (в миллисекундах), необходимое для ducked источников «увеличение».</span><span class="sxs-lookup"><span data-stu-id="f9e22-117">The amount of time (in milliseconds) it takes for ducked sources to "fade in".</span></span>  |
| <span data-ttu-id="f9e22-118">upperLevel</span><span class="sxs-lookup"><span data-stu-id="f9e22-118">upperLevel</span></span>    | <span data-ttu-id="f9e22-119">Int64</span><span class="sxs-lookup"><span data-stu-id="f9e22-119">Int64</span></span>    | <span data-ttu-id="f9e22-120">Объем источников в процентах, когда ducked источников не выполняется.</span><span class="sxs-lookup"><span data-stu-id="f9e22-120">The volume of sources in percent when the sources are not being ducked.</span></span>         |

> <span data-ttu-id="f9e22-121">**Примечание:** Продолжительность расширение путь не может быть более 5000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="f9e22-121">**Note:** Ramp duration cannot be more than 5,000 milliseconds.</span></span>

## <a name="json-representation"></a><span data-ttu-id="f9e22-122">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="f9e22-122">JSON representation</span></span>

<span data-ttu-id="f9e22-123">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="f9e22-123">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.audioDuckingConfiguration"
}-->
```json
{
  "lowerLevel": 20,
  "rampActive": 1000,
  "rampInactive": 1000,
  "upperLevel": 100
}
```
<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "audioDuckingConfiguration resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/audioduckingconfiguration.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
