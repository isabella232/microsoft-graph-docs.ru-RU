---
title: Тип ресурса МитингпартиЦипантс
description: Участники собрания.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 57a07e29beae6915c7e40f7fb8a6e941351fd38f
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32463826"
---
# <a name="meetingparticipants-resource-type"></a><span data-ttu-id="acbe2-103">Тип ресурса МитингпартиЦипантс</span><span class="sxs-lookup"><span data-stu-id="acbe2-103">meetingParticipants resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="acbe2-104">Участники собрания.</span><span class="sxs-lookup"><span data-stu-id="acbe2-104">Participants in a meeting.</span></span>

## <a name="properties"></a><span data-ttu-id="acbe2-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="acbe2-105">Properties</span></span>

| <span data-ttu-id="acbe2-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="acbe2-106">Property</span></span>       | <span data-ttu-id="acbe2-107">Тип</span><span class="sxs-lookup"><span data-stu-id="acbe2-107">Type</span></span>    | <span data-ttu-id="acbe2-108">Описание</span><span class="sxs-lookup"><span data-stu-id="acbe2-108">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="acbe2-109">attendees</span><span class="sxs-lookup"><span data-stu-id="acbe2-109">attendees</span></span> | <span data-ttu-id="acbe2-110">Коллекция [митингпартиЦипантинфо](meetingparticipantinfo.md)</span><span class="sxs-lookup"><span data-stu-id="acbe2-110">[meetingParticipantInfo](meetingparticipantinfo.md) collection</span></span> |  |
| <span data-ttu-id="acbe2-111">organizer</span><span class="sxs-lookup"><span data-stu-id="acbe2-111">organizer</span></span> | [<span data-ttu-id="acbe2-112">МитингпартиЦипантинфо</span><span class="sxs-lookup"><span data-stu-id="acbe2-112">meetingParticipantInfo</span></span>](meetingparticipantinfo.md) |  |

## <a name="json-representation"></a><span data-ttu-id="acbe2-113">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="acbe2-113">JSON representation</span></span>

<span data-ttu-id="acbe2-114">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="acbe2-114">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingParticipants"
}-->
```json
{
  "attendees": [{"@odata.type": "#microsoft.graph.meetingParticipantInfo"}],
  "organizer": {"@odata.type": "#microsoft.graph.meetingParticipantInfo"}
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "meetingParticipants resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/meetingparticipants.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
