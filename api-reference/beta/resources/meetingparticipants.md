---
title: Тип ресурса meetingParticipants
description: Ниже указано представление ресурса в формате JSON.
ms.openlocfilehash: 4f91c9198018e903eccff7e8fe07d6668d9fd2c9
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27082382"
---
# <a name="meetingparticipants-resource-type"></a><span data-ttu-id="3b2de-103">Тип ресурса meetingParticipants</span><span class="sxs-lookup"><span data-stu-id="3b2de-103">meetingParticipants resource type</span></span>

> <span data-ttu-id="3b2de-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="3b2de-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="3b2de-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="3b2de-105">Use of these APIs in production applications is not supported.</span></span>

## <a name="properties"></a><span data-ttu-id="3b2de-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="3b2de-106">Properties</span></span>

| <span data-ttu-id="3b2de-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="3b2de-107">Property</span></span>       | <span data-ttu-id="3b2de-108">Тип</span><span class="sxs-lookup"><span data-stu-id="3b2de-108">Type</span></span>    | <span data-ttu-id="3b2de-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3b2de-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="3b2de-110">attendees</span><span class="sxs-lookup"><span data-stu-id="3b2de-110">attendees</span></span> | <span data-ttu-id="3b2de-111">[meetingParticipantInfo](meetingparticipantinfo.md) коллекции</span><span class="sxs-lookup"><span data-stu-id="3b2de-111">[meetingParticipantInfo](meetingparticipantinfo.md) collection</span></span> |  |
| <span data-ttu-id="3b2de-112">organizer</span><span class="sxs-lookup"><span data-stu-id="3b2de-112">organizer</span></span> | [<span data-ttu-id="3b2de-113">meetingParticipantInfo</span><span class="sxs-lookup"><span data-stu-id="3b2de-113">meetingParticipantInfo</span></span>](meetingparticipantinfo.md) |  |

## <a name="json-representation"></a><span data-ttu-id="3b2de-114">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="3b2de-114">JSON representation</span></span>

<span data-ttu-id="3b2de-115">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="3b2de-115">The following is a JSON representation of the resource.</span></span>

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
<!-- {
  "type": "#page.annotation",
  "description": "meetingParticipants resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
