---
title: Тип ресурса participantMixerLevel
description: Конфигурация микшер уровни для заданного звука участников
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 14804e02766e375568fac03cb97d2eaf76142353
ms.sourcegitcommit: d95f6d39a0479da6e531f3734c4029dc596b9a3f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2019
ms.locfileid: "29643834"
---
# <a name="participantmixerlevel-resource-type"></a><span data-ttu-id="22018-103">Тип ресурса participantMixerLevel</span><span class="sxs-lookup"><span data-stu-id="22018-103">participantMixerLevel resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="22018-104">Конфигурация микшер уровни для заданного звука участников</span><span class="sxs-lookup"><span data-stu-id="22018-104">Configuration of mixer levels for given audio participant</span></span>

## <a name="properties"></a><span data-ttu-id="22018-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="22018-105">Properties</span></span>

| <span data-ttu-id="22018-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="22018-106">Property</span></span>               | <span data-ttu-id="22018-107">Тип</span><span class="sxs-lookup"><span data-stu-id="22018-107">Type</span></span>                                                      | <span data-ttu-id="22018-108">Описание</span><span class="sxs-lookup"><span data-stu-id="22018-108">Description</span></span>                                                                                         |
| :--------------------- | :-------------------------------------------------------- | :---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="22018-109">Уклонение от</span><span class="sxs-lookup"><span data-stu-id="22018-109">ducking</span></span>                | [<span data-ttu-id="22018-110">audioDuckingConfiguration</span><span class="sxs-lookup"><span data-stu-id="22018-110">audioDuckingConfiguration</span></span>](audioduckingconfiguration.md) | <span data-ttu-id="22018-111">Конфигурация (синхронизацию и) из других источников для этой partipant пользовательский набор Уклонение от.</span><span class="sxs-lookup"><span data-stu-id="22018-111">Configuration of ducking (phasing in and out) of other sources for this partipant custom mix.</span></span>       |
| <span data-ttu-id="22018-112">exclusiveMode</span><span class="sxs-lookup"><span data-stu-id="22018-112">exclusiveMode</span></span>          | <span data-ttu-id="22018-113">boolean</span><span class="sxs-lookup"><span data-stu-id="22018-113">boolean</span></span>                                                   | <span data-ttu-id="22018-114">Является ли источники без явного источника уровня необходимо удалить из набора.</span><span class="sxs-lookup"><span data-stu-id="22018-114">Whether sources without explicit source level should be removed from the mix.</span></span>                       |
| <span data-ttu-id="22018-115">Участник</span><span class="sxs-lookup"><span data-stu-id="22018-115">participant</span></span>            | <span data-ttu-id="22018-116">String</span><span class="sxs-lookup"><span data-stu-id="22018-116">String</span></span>                                                    | <span data-ttu-id="22018-117">Участник, для которого настраивается микшера.</span><span class="sxs-lookup"><span data-stu-id="22018-117">The participant for whom the mixer is being configured.</span></span>                                             |
| <span data-ttu-id="22018-118">sourceLevels</span><span class="sxs-lookup"><span data-stu-id="22018-118">sourceLevels</span></span>           | <span data-ttu-id="22018-119">[audioSourceLevel](audiosourcelevel.md) коллекции</span><span class="sxs-lookup"><span data-stu-id="22018-119">[audioSourceLevel](audiosourcelevel.md) collection</span></span>        | <span data-ttu-id="22018-120">Конфигурации уровня для других источников.</span><span class="sxs-lookup"><span data-stu-id="22018-120">Level configuration for other sources.</span></span>                                                              |

## <a name="json-representation"></a><span data-ttu-id="22018-121">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="22018-121">JSON representation</span></span>

<span data-ttu-id="22018-122">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="22018-122">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.participantMixerLevel"
}-->
```json
{
  "ducking": { "@odata.type": "#microsoft.graph.audioDuckingConfiguration" },
  "exclusiveMode": true,
  "participant": "String",
  "sourceLevels": [ { "@odata.type": "#microsoft.graph.audioSourceLevel" } ]
}
```

## <a name="example---mixer-level"></a><span data-ttu-id="22018-123">Пример — уровень микшер</span><span class="sxs-lookup"><span data-stu-id="22018-123">Example - Mixer level</span></span>

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.participantMixerLevel"
}-->
```json
{
  "ducking": {
    "@odata.type": "#microsoft.graph.audioDuckingParameters",
    "rampActive": 1000,
    "rampInactive": 1000,
    "lowerLevel": 20,
    "upperLevel": 100
  },
  "exclusiveMode": true,
  "participant": "123456W77E24E4D85F80597083CB830",
  "sourceLevels": [
    {
      "@odata.type": "#microsoft.graph.audioSourceLevel",
      "duckOthers": false,
      "level": 100,
      "participant": "8A34A46B3D174ADC8DCEDC4E7D572698"
    }
  ]
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "participantMixerLevel resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/participantmixerlevel.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
