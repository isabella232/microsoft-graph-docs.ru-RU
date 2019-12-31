---
title: Тип ресурса Рекордингинфо
description: Сведения о записи для участника.
author: ananmishr
localization_priority: Normal
ms.prod: cloud-communications
doc_type: resourcePageType
ms.openlocfilehash: e924ea98bb0f9ac8e0b610a4672cbed83d83d0bc
ms.sourcegitcommit: 636671293b0be89088459c4fc8a5e661341b37cf
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/31/2019
ms.locfileid: "40913445"
---
# <a name="recordinginfo-resource-type"></a><span data-ttu-id="68f91-103">Тип ресурса Рекордингинфо</span><span class="sxs-lookup"><span data-stu-id="68f91-103">recordingInfo resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="68f91-104">Сведения о записи для участника.</span><span class="sxs-lookup"><span data-stu-id="68f91-104">Recording information for a participant.</span></span>

## <a name="properties"></a><span data-ttu-id="68f91-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="68f91-105">Properties</span></span>

| <span data-ttu-id="68f91-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="68f91-106">Property</span></span>        | <span data-ttu-id="68f91-107">Тип</span><span class="sxs-lookup"><span data-stu-id="68f91-107">Type</span></span>    | <span data-ttu-id="68f91-108">Описание</span><span class="sxs-lookup"><span data-stu-id="68f91-108">Description</span></span>|
|:----------------|:--------|:----------|
| <span data-ttu-id="68f91-109">initiatedBy</span><span class="sxs-lookup"><span data-stu-id="68f91-109">initiatedBy</span></span>     | [<span data-ttu-id="68f91-110">participantInfo</span><span class="sxs-lookup"><span data-stu-id="68f91-110">participantInfo</span></span>](participantinfo.md) | <span data-ttu-id="68f91-111">Участник, который инициировал запись.</span><span class="sxs-lookup"><span data-stu-id="68f91-111">The participant who initiated the recording.</span></span> |
| <span data-ttu-id="68f91-112">рекордингстатус</span><span class="sxs-lookup"><span data-stu-id="68f91-112">recordingStatus</span></span> | <span data-ttu-id="68f91-113">String</span><span class="sxs-lookup"><span data-stu-id="68f91-113">String</span></span> | <span data-ttu-id="68f91-114">`unknown`Возможные значения: `notRecording`,, `recording`, или. `failed`</span><span class="sxs-lookup"><span data-stu-id="68f91-114">Possible values are: `unknown`, `notRecording`, `recording`, or `failed`.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="68f91-115">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="68f91-115">JSON representation</span></span>

<span data-ttu-id="68f91-116">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="68f91-116">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recordingInfo"
}-->
```json
{
  "initiatedBy": {"@odata.type": "#microsoft.graph.participantInfo"},
  "recordingStatus": "unknown | notRecording | recording | failed"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "recordingInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
