---
title: Тип ресурсов attendeeAvailability
description: Доступность участника.
localization_priority: Normal
author: angelgolfer-ms
ms.prod: outlook
doc_type: resourcePageType
ms.openlocfilehash: ffdff0945522d04361510cfcc5917381fecfaa03
ms.sourcegitcommit: 2c62457e57467b8d50f21b255b553106a9a5d8d6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/31/2019
ms.locfileid: "36030060"
---
# <a name="attendeeavailability-resource-type"></a><span data-ttu-id="428f3-103">Тип ресурсов attendeeAvailability</span><span class="sxs-lookup"><span data-stu-id="428f3-103">attendeeAvailability resource type</span></span>

<span data-ttu-id="428f3-104">Доступность участника.</span><span class="sxs-lookup"><span data-stu-id="428f3-104">The availability of an attendee.</span></span>

## <a name="json-representation"></a><span data-ttu-id="428f3-105">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="428f3-105">JSON representation</span></span>

<span data-ttu-id="428f3-106">Ниже показано представление JSON ресурса.</span><span class="sxs-lookup"><span data-stu-id="428f3-106">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.attendeeAvailability"
}-->

```json
{
  "attendee": {"@odata.type": "microsoft.graph.attendeeBase"},
  "availability": "String"
}

```
## <a name="properties"></a><span data-ttu-id="428f3-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="428f3-107">Properties</span></span>
| <span data-ttu-id="428f3-108">Свойство</span><span class="sxs-lookup"><span data-stu-id="428f3-108">Property</span></span>     | <span data-ttu-id="428f3-109">Тип</span><span class="sxs-lookup"><span data-stu-id="428f3-109">Type</span></span>   |<span data-ttu-id="428f3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="428f3-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="428f3-111">attendee</span><span class="sxs-lookup"><span data-stu-id="428f3-111">attendee</span></span>|[<span data-ttu-id="428f3-112">attendeeBase</span><span class="sxs-lookup"><span data-stu-id="428f3-112">attendeeBase</span></span>](attendeebase.md)|<span data-ttu-id="428f3-113">Адрес электронной почты и тип участника — является ли это пользователь или ресурс, а также является ли он обязательным, если это человек.</span><span class="sxs-lookup"><span data-stu-id="428f3-113">The email address and type of attendee - whether it's a person or a resource, and whether required or optional if it's a person.</span></span>|
|<span data-ttu-id="428f3-114">availability</span><span class="sxs-lookup"><span data-stu-id="428f3-114">availability</span></span>|<span data-ttu-id="428f3-115">freeBusyStatus</span><span class="sxs-lookup"><span data-stu-id="428f3-115">freeBusyStatus</span></span>| <span data-ttu-id="428f3-116">Состояние занятости участника.</span><span class="sxs-lookup"><span data-stu-id="428f3-116">The availability status of the attendee.</span></span> <span data-ttu-id="428f3-117">Допустимые значения: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="428f3-117">The possible values are: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attendeeAvailability resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
