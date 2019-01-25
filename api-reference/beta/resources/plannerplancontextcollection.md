---
title: Тип ресурса plannerPlanContextCollection
description: Ресурс **plannerPlanContextCollection** представляет коллекцию внешних контекстах, с которыми связан плана. Этот ресурс является открытым и является частью объекта plannerPlan. Значение в паре значение свойства — это объект plannerPlanContext.
localization_priority: Normal
author: TarkanSevilmis
ms.prod: planner
ms.openlocfilehash: 6ec515a164c5b0fca6334930b55a4b5d4e73b7d9
ms.sourcegitcommit: 3d24047b3af46136734de2486b041e67a34f3d83
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2019
ms.locfileid: "29516499"
---
# <a name="plannerplancontextcollection-resource-type"></a><span data-ttu-id="ecd55-105">Тип ресурса plannerPlanContextCollection</span><span class="sxs-lookup"><span data-stu-id="ecd55-105">plannerPlanContextCollection resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]


<span data-ttu-id="ecd55-106">Ресурс **plannerPlanContextCollection** представляет коллекцию внешних контекстах, с которыми связан плана.</span><span class="sxs-lookup"><span data-stu-id="ecd55-106">The **plannerPlanContextCollection** resource represents the collection of external contexts to which a plan is linked.</span></span> <span data-ttu-id="ecd55-107">Этот ресурс является открытым и является частью объекта [plannerPlan](plannerplan.md) .</span><span class="sxs-lookup"><span data-stu-id="ecd55-107">This resource is an open type and is part of the [plannerPlan](plannerplan.md) object.</span></span> <span data-ttu-id="ecd55-108">Значение в паре значение свойства — это объект [plannerPlanContext](plannerplancontext.md) .</span><span class="sxs-lookup"><span data-stu-id="ecd55-108">The value in the property-value pair is the [plannerPlanContext](plannerplancontext.md) object.</span></span>


## <a name="properties"></a><span data-ttu-id="ecd55-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="ecd55-109">Properties</span></span>
<span data-ttu-id="ecd55-110">Можно определить свойства этого типа open.</span><span class="sxs-lookup"><span data-stu-id="ecd55-110">You can define the properties of this open type.</span></span> <span data-ttu-id="ecd55-111">Значения свойства должны быть особый идентификатор, представляющий внешнего контекста как имя свойства.</span><span class="sxs-lookup"><span data-stu-id="ecd55-111">The property values should be distinctive identifier that represents the external context as the property name.</span></span> <span data-ttu-id="ecd55-112">Значения свойства должны быть [plannerPlanContext](plannerplancontext.md) объектов.</span><span class="sxs-lookup"><span data-stu-id="ecd55-112">The property values must be [plannerPlanContext](plannerplancontext.md) objects.</span></span> <span data-ttu-id="ecd55-113">На основании требований к OData, имена свойств в открытые типы не может содержать следующие символы: `.`, `:`, `%`, `@`.</span><span class="sxs-lookup"><span data-stu-id="ecd55-113">Based on OData requirements, property names in open types cannot contain the following characters: `.`, `:`, `%`, `@`.</span></span> <span data-ttu-id="ecd55-114">Эти символы должны быть закодированы с помощью Кодировка URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="ecd55-114">These characters need to be encoded using URL encoding.</span></span> <span data-ttu-id="ecd55-115">Чтобы удалить элемент в списке "Избранное", задайте значение свойства, которое должно `null`.</span><span class="sxs-lookup"><span data-stu-id="ecd55-115">To remove an item in the favorites list, set the value of the property to `null`.</span></span>

## <a name="json-representation"></a><span data-ttu-id="ecd55-116">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="ecd55-116">JSON representation</span></span>

<span data-ttu-id="ecd55-117">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="ecd55-117">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.plannerPlanContextCollection"
}-->

```json
{
  "48#19%3Ad128c63941b24733951ea7defd81e550%40thread%2Eskype19%3Ad128c63941b24733951ea7defd81e550%40thread%2Eskype": {
    "@odata.type": "#microsoft.graph.plannerPlanContext",
    "associationType": "Board",
    "createdDateTime": "2015-10-14T00:57:28.4698344Z",
    "displayNameSegments": [
        "Finance Team",
        "Budget Plans"
    ],
    "ownerAppId": "5e3ce6c0-2b1f-4285-8d4b-75ee78787346"
  }
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "plannerPlanContextCollection resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/plannerplancontextcollection.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
