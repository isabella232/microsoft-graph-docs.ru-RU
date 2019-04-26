---
title: Тип ресурса МитингпартиЦипантс
description: Участники собрания.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: f6446ec0b896854e2566d4de82acfdb53bee893d
ms.sourcegitcommit: 014eb3944306948edbb6560dbe689816a168c4f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/26/2019
ms.locfileid: "33342410"
---
# <a name="meetingparticipants-resource-type"></a><span data-ttu-id="ffe84-103">Тип ресурса МитингпартиЦипантс</span><span class="sxs-lookup"><span data-stu-id="ffe84-103">meetingParticipants resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="ffe84-104">Участники собрания.</span><span class="sxs-lookup"><span data-stu-id="ffe84-104">Participants in a meeting.</span></span>

## <a name="properties"></a><span data-ttu-id="ffe84-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="ffe84-105">Properties</span></span>

| <span data-ttu-id="ffe84-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="ffe84-106">Property</span></span>       | <span data-ttu-id="ffe84-107">Тип</span><span class="sxs-lookup"><span data-stu-id="ffe84-107">Type</span></span>    | <span data-ttu-id="ffe84-108">Описание</span><span class="sxs-lookup"><span data-stu-id="ffe84-108">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="ffe84-109">attendees</span><span class="sxs-lookup"><span data-stu-id="ffe84-109">attendees</span></span> | <span data-ttu-id="ffe84-110">Коллекция [митингпартиЦипантинфо](meetingparticipantinfo.md)</span><span class="sxs-lookup"><span data-stu-id="ffe84-110">[meetingParticipantInfo](meetingparticipantinfo.md) collection</span></span> |  |
| <span data-ttu-id="ffe84-111">organizer</span><span class="sxs-lookup"><span data-stu-id="ffe84-111">organizer</span></span> | [<span data-ttu-id="ffe84-112">МитингпартиЦипантинфо</span><span class="sxs-lookup"><span data-stu-id="ffe84-112">meetingParticipantInfo</span></span>](meetingparticipantinfo.md) |  |

## <a name="json-representation"></a><span data-ttu-id="ffe84-113">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="ffe84-113">JSON representation</span></span>

<span data-ttu-id="ffe84-114">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="ffe84-114">The following is a JSON representation of the resource.</span></span>

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
  "suppressions": []
}
-->
