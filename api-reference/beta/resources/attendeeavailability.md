---
title: Тип ресурсов attendeeAvailability
description: Тип и занятость участника.
localization_priority: Normal
ms.openlocfilehash: a00fe38e678c6a51cd252b823a7d2651e531d20a
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/11/2019
ms.locfileid: "27820470"
---
# <a name="attendeeavailability-resource-type"></a><span data-ttu-id="a8a03-103">Тип ресурсов attendeeAvailability</span><span class="sxs-lookup"><span data-stu-id="a8a03-103">attendeeAvailability resource type</span></span>

> <span data-ttu-id="a8a03-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="a8a03-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="a8a03-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="a8a03-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="a8a03-106">Тип и занятость участника.</span><span class="sxs-lookup"><span data-stu-id="a8a03-106">The type and availability of an attendee.</span></span>

## <a name="json-representation"></a><span data-ttu-id="a8a03-107">Представление в формате JSON</span><span class="sxs-lookup"><span data-stu-id="a8a03-107">JSON representation</span></span>

<span data-ttu-id="a8a03-108">Ниже показано представление JSON ресурса.</span><span class="sxs-lookup"><span data-stu-id="a8a03-108">Here is a JSON representation of the resource</span></span>

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
## <a name="properties"></a><span data-ttu-id="a8a03-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="a8a03-109">Properties</span></span>
| <span data-ttu-id="a8a03-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="a8a03-110">Property</span></span>     | <span data-ttu-id="a8a03-111">Тип</span><span class="sxs-lookup"><span data-stu-id="a8a03-111">Type</span></span>   |<span data-ttu-id="a8a03-112">Описание</span><span class="sxs-lookup"><span data-stu-id="a8a03-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="a8a03-113">attendee</span><span class="sxs-lookup"><span data-stu-id="a8a03-113">attendee</span></span>|[<span data-ttu-id="a8a03-114">AttendeeBase</span><span class="sxs-lookup"><span data-stu-id="a8a03-114">AttendeeBase</span></span>](attendeebase.md)|<span data-ttu-id="a8a03-115">Тип участника (сведения о том, является ли участник пользователем или ресурсом, а также о том, обязательный ли он, если объект представляет пользователя).</span><span class="sxs-lookup"><span data-stu-id="a8a03-115">The type of attendee - whether it's a person or a resource, and whether required or optional if it's a person.</span></span>|
|<span data-ttu-id="a8a03-116">availability</span><span class="sxs-lookup"><span data-stu-id="a8a03-116">availability</span></span>|<span data-ttu-id="a8a03-117">Строка</span><span class="sxs-lookup"><span data-stu-id="a8a03-117">String</span></span>| <span data-ttu-id="a8a03-p102">Состояние занятости участника. Возможные значения: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span><span class="sxs-lookup"><span data-stu-id="a8a03-p102">The availability status of the attendee. Possible values are: `free`, `tentative`, `busy`, `oof`, `workingElsewhere`, `unknown`.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "attendeeAvailability resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
