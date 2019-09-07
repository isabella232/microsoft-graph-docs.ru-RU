---
title: Тип ресурса МитингпартиЦипантс
description: Участники собрания.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
doc_type: resourcePageType
ms.openlocfilehash: 2d40479390703f50ac87b7c3196aa4d5bc55bc8a
ms.sourcegitcommit: c68a83d28fa4bfca6e0618467934813a9ae17b12
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/07/2019
ms.locfileid: "36792767"
---
# <a name="meetingparticipants-resource-type"></a><span data-ttu-id="599eb-103">Тип ресурса МитингпартиЦипантс</span><span class="sxs-lookup"><span data-stu-id="599eb-103">meetingParticipants resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="599eb-104">Участники собрания.</span><span class="sxs-lookup"><span data-stu-id="599eb-104">Participants in a meeting.</span></span>

## <a name="properties"></a><span data-ttu-id="599eb-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="599eb-105">Properties</span></span>

| <span data-ttu-id="599eb-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="599eb-106">Property</span></span>       | <span data-ttu-id="599eb-107">Тип</span><span class="sxs-lookup"><span data-stu-id="599eb-107">Type</span></span>    | <span data-ttu-id="599eb-108">Описание</span><span class="sxs-lookup"><span data-stu-id="599eb-108">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="599eb-109">attendees</span><span class="sxs-lookup"><span data-stu-id="599eb-109">attendees</span></span> | <span data-ttu-id="599eb-110">Коллекция [митингпартиЦипантинфо](meetingparticipantinfo.md)</span><span class="sxs-lookup"><span data-stu-id="599eb-110">[meetingParticipantInfo](meetingparticipantinfo.md) collection</span></span> |  |
| <span data-ttu-id="599eb-111">organizer</span><span class="sxs-lookup"><span data-stu-id="599eb-111">organizer</span></span> | [<span data-ttu-id="599eb-112">митингпартиЦипантинфо</span><span class="sxs-lookup"><span data-stu-id="599eb-112">meetingParticipantInfo</span></span>](meetingparticipantinfo.md) |  |
| <span data-ttu-id="599eb-113">производители</span><span class="sxs-lookup"><span data-stu-id="599eb-113">producers</span></span> | <span data-ttu-id="599eb-114">Коллекция [митингпартиЦипантинфо](meetingparticipantinfo.md)</span><span class="sxs-lookup"><span data-stu-id="599eb-114">[meetingParticipantInfo](meetingparticipantinfo.md) collection</span></span> | <span data-ttu-id="599eb-115">Только для широковещательного собрания.</span><span class="sxs-lookup"><span data-stu-id="599eb-115">For broadcast meeting only.</span></span> |
| <span data-ttu-id="599eb-116">Авторы</span><span class="sxs-lookup"><span data-stu-id="599eb-116">contributors</span></span> | <span data-ttu-id="599eb-117">Коллекция [митингпартиЦипантинфо](meetingparticipantinfo.md)</span><span class="sxs-lookup"><span data-stu-id="599eb-117">[meetingParticipantInfo](meetingparticipantinfo.md) collection</span></span> | <span data-ttu-id="599eb-118">Только для широковещательного собрания.</span><span class="sxs-lookup"><span data-stu-id="599eb-118">For broadcast meeting only.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="599eb-119">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="599eb-119">JSON representation</span></span>

<span data-ttu-id="599eb-120">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="599eb-120">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingParticipants"
}-->
```json
{
  "attendees": [{"@odata.type": "#microsoft.graph.meetingParticipantInfo"}],
  "organizer": {"@odata.type": "#microsoft.graph.meetingParticipantInfo"},
  "producers": [{"@odata.type": "#microsoft.graph.meetingParticipantInfo"}],
  "contributors": [{"@odata.type": "#microsoft.graph.meetingParticipantInfo"}],
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
