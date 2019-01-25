---
title: Тип ресурса plannerFavoritePlanReferenceCollection
description: " значение — это объект plannerFavoritePlanReference."
author: TarkanSevilmis
localization_priority: Normal
ms.prod: planner
ms.openlocfilehash: c473d4101a1247420e641b532ea04dfbc1a26d2c
ms.sourcegitcommit: 3d24047b3af46136734de2486b041e67a34f3d83
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2019
ms.locfileid: "29519488"
---
# <a name="plannerfavoriteplanreferencecollection-resource-type"></a><span data-ttu-id="08837-103">Тип ресурса plannerFavoritePlanReferenceCollection</span><span class="sxs-lookup"><span data-stu-id="08837-103">plannerFavoritePlanReferenceCollection resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="08837-104">Ресурс **plannerFavoritePlanReferenceCollection** представляет коллекцию ссылок на планы, которые помечены как Избранное пользователя.</span><span class="sxs-lookup"><span data-stu-id="08837-104">The **plannerFavoritePlanReferenceCollection** resource represents the collection of references to plans that are marked as a favorite by a user.</span></span> <span data-ttu-id="08837-105">Этот ресурс является открытым и является частью объекта [plannerUser](planneruser.md) .</span><span class="sxs-lookup"><span data-stu-id="08837-105">This resource is an open type and is part of the [plannerUser](planneruser.md) object.</span></span> <span data-ttu-id="08837-106">Имя свойства в паре значение свойства — это идентификатор соответствующего плана. значение — это объект [plannerFavoritePlanReference](plannerfavoriteplanreference.md) .</span><span class="sxs-lookup"><span data-stu-id="08837-106">The property name in the property-value pair is the ID of the corresponding plan; the value is the [plannerFavoritePlanReference](plannerfavoriteplanreference.md) object.</span></span>


## <a name="properties"></a><span data-ttu-id="08837-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="08837-107">Properties</span></span>
<span data-ttu-id="08837-108">Можно определить свойства этого типа open.</span><span class="sxs-lookup"><span data-stu-id="08837-108">You can define the properties of this open type.</span></span> <span data-ttu-id="08837-109">Имена свойств являются `id` значений [plannerPlan](plannerplan.md) ресурсов и их значения должны быть [plannerFavoritePlanReference](plannerfavoriteplanreference.md) объектов.</span><span class="sxs-lookup"><span data-stu-id="08837-109">The property names are `id` values of [plannerPlan](plannerplan.md) resources and their values must be [plannerFavoritePlanReference](plannerfavoriteplanreference.md) objects.</span></span> <span data-ttu-id="08837-110">Чтобы удалить элемент в списке "Избранное", задайте значение свойства, которое должно `null`.</span><span class="sxs-lookup"><span data-stu-id="08837-110">To remove an item in the favorites list, set the value of the property to `null`.</span></span>


## <a name="json-representation"></a><span data-ttu-id="08837-111">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="08837-111">JSON representation</span></span>

<span data-ttu-id="08837-112">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="08837-112">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerFavoritePlanReferenceCollection"
}-->

```json
{
  "jd8S5gOaFk2S8aWCIAJz42QAAxtD": {
    "@odata.type": "microsoft.graph.plannerFavoritePlanReference",
    "orderHint": "8586866870001551087",
    "planTitle": "Customer reviews"
  },
  "uZWtCtli30CGoWLIWSat1mQAC0ai": {
    "@odata.type": "microsoft.graph.plannerFavoritePlanReference",
    "orderHint": "8586848705198093378",
    "planTitle": "Order Management (December 2017)"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "plannerFavoritePlanReferenceCollection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/plannerfavoriteplanreferencecollection.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
