---
title: Тип ресурса МитингпартиЦипантс
description: Участники собрания.
author: ananmishr
localization_priority: Normal
ms.prod: cloud-communications
doc_type: resourcePageType
ms.openlocfilehash: 3bcce64ab900dae7c7f13d7da0c3d34d164fd35d
ms.sourcegitcommit: 636671293b0be89088459c4fc8a5e661341b37cf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/31/2019
ms.locfileid: "40913522"
---
# <a name="meetingparticipants-resource-type"></a><span data-ttu-id="f2f09-103">Тип ресурса МитингпартиЦипантс</span><span class="sxs-lookup"><span data-stu-id="f2f09-103">meetingParticipants resource type</span></span>

<span data-ttu-id="f2f09-104">Участники собрания.</span><span class="sxs-lookup"><span data-stu-id="f2f09-104">Participants in a meeting.</span></span>

## <a name="properties"></a><span data-ttu-id="f2f09-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="f2f09-105">Properties</span></span>

| <span data-ttu-id="f2f09-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="f2f09-106">Property</span></span>       | <span data-ttu-id="f2f09-107">Тип</span><span class="sxs-lookup"><span data-stu-id="f2f09-107">Type</span></span>    | <span data-ttu-id="f2f09-108">Описание</span><span class="sxs-lookup"><span data-stu-id="f2f09-108">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="f2f09-109">attendees</span><span class="sxs-lookup"><span data-stu-id="f2f09-109">attendees</span></span> | <span data-ttu-id="f2f09-110">Коллекция [митингпартиЦипантинфо](meetingparticipantinfo.md)</span><span class="sxs-lookup"><span data-stu-id="f2f09-110">[meetingParticipantInfo](meetingparticipantinfo.md) collection</span></span> |  |
| <span data-ttu-id="f2f09-111">organizer</span><span class="sxs-lookup"><span data-stu-id="f2f09-111">organizer</span></span> | [<span data-ttu-id="f2f09-112">митингпартиЦипантинфо</span><span class="sxs-lookup"><span data-stu-id="f2f09-112">meetingParticipantInfo</span></span>](meetingparticipantinfo.md) |  |

## <a name="json-representation"></a><span data-ttu-id="f2f09-113">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="f2f09-113">JSON representation</span></span>

<span data-ttu-id="f2f09-114">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="f2f09-114">The following is a JSON representation of the resource.</span></span>

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
