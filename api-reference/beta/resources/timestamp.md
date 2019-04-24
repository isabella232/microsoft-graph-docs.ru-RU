---
title: Тип ресурса timeStamp
description: Сведения о дате и времени для определенного момента времени.
localization_priority: Normal
ms.openlocfilehash: 79faa8f74fbaf64eb6756183ecc309c6522873e6
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32463574"
---
# <a name="timestamp-resource-type"></a><span data-ttu-id="e5711-103">Тип ресурса timeStamp</span><span class="sxs-lookup"><span data-stu-id="e5711-103">timeStamp resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="e5711-104">Сведения о дате и времени для определенного момента времени.</span><span class="sxs-lookup"><span data-stu-id="e5711-104">Date and time information for a point in time.</span></span>

## <a name="json-representation"></a><span data-ttu-id="e5711-105">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="e5711-105">JSON representation</span></span>

<span data-ttu-id="e5711-106">Ниже показано представление JSON ресурса.</span><span class="sxs-lookup"><span data-stu-id="e5711-106">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.timeStamp"
}-->

```json
{
  "date": "String (timestamp)",
  "time": "String (timestamp)",
  "timeZone": "string"
}

```
## <a name="properties"></a><span data-ttu-id="e5711-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="e5711-107">Properties</span></span>
| <span data-ttu-id="e5711-108">Свойство</span><span class="sxs-lookup"><span data-stu-id="e5711-108">Property</span></span>     | <span data-ttu-id="e5711-109">Тип</span><span class="sxs-lookup"><span data-stu-id="e5711-109">Type</span></span>   |<span data-ttu-id="e5711-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e5711-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="e5711-111">дата</span><span class="sxs-lookup"><span data-stu-id="e5711-111">date</span></span>|<span data-ttu-id="e5711-112">Date</span><span class="sxs-lookup"><span data-stu-id="e5711-112">Date</span></span>|<span data-ttu-id="e5711-113">Часть даты метки времени.</span><span class="sxs-lookup"><span data-stu-id="e5711-113">The date portion of the timestamp.</span></span>|
|<span data-ttu-id="e5711-114">time</span><span class="sxs-lookup"><span data-stu-id="e5711-114">time</span></span>|<span data-ttu-id="e5711-115">TimeOfDay</span><span class="sxs-lookup"><span data-stu-id="e5711-115">TimeOfDay</span></span>|<span data-ttu-id="e5711-116">Часть времени метки времени.</span><span class="sxs-lookup"><span data-stu-id="e5711-116">The time portion of the timestamp.</span></span>|
|<span data-ttu-id="e5711-117">timeZone</span><span class="sxs-lookup"><span data-stu-id="e5711-117">timeZone</span></span>|<span data-ttu-id="e5711-118">String</span><span class="sxs-lookup"><span data-stu-id="e5711-118">String</span></span>|<span data-ttu-id="e5711-119">Часть временной метки, представляющая часовой пояс (одна из 24 лонгитудинал областей мира).</span><span class="sxs-lookup"><span data-stu-id="e5711-119">The timezone portion of the timestamp, which is one of the 24 longitudinal areas in the world.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "timeStamp resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/timestamp.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
