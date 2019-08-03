---
title: Тип ресурса Рубриккритерион
description: Критерий Rubric
localization_priority: Normal
author: dipakboyed
ms.prod: education
doc_type: resourcePageType
ms.openlocfilehash: 250132ab5304ab9df94707349df951e5b1e995a6
ms.sourcegitcommit: 129e58f83fc566f9d9f36e26b0c0b8cdf81d27d9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/03/2019
ms.locfileid: "36173344"
---
# <a name="rubriccriterion-resource-type"></a><span data-ttu-id="912bb-103">Тип ресурса Рубриккритерион</span><span class="sxs-lookup"><span data-stu-id="912bb-103">rubricCriterion resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="912bb-104">Критерий Rubric.</span><span class="sxs-lookup"><span data-stu-id="912bb-104">A criterion of a rubric.</span></span> <span data-ttu-id="912bb-105">Описание связи между Rubric *качеством*, *уровнями*и критериями можно узнать в разделе \*\* [едукатионрубрик](educationrubric.md) .</span><span class="sxs-lookup"><span data-stu-id="912bb-105">See [educationRubric](educationrubric.md) for a description of the relationship between rubric *qualities*, *levels*, and *criteria*.</span></span>

## <a name="properties"></a><span data-ttu-id="912bb-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="912bb-106">Properties</span></span>

| <span data-ttu-id="912bb-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="912bb-107">Property</span></span>     | <span data-ttu-id="912bb-108">Тип</span><span class="sxs-lookup"><span data-stu-id="912bb-108">Type</span></span>        | <span data-ttu-id="912bb-109">Описание</span><span class="sxs-lookup"><span data-stu-id="912bb-109">Description</span></span> |
|:-------------|:------------|:------------|
|<span data-ttu-id="912bb-110">description</span><span class="sxs-lookup"><span data-stu-id="912bb-110">description</span></span>|[<span data-ttu-id="912bb-111">itemBody</span><span class="sxs-lookup"><span data-stu-id="912bb-111">itemBody</span></span>](itembody.md)|<span data-ttu-id="912bb-112">Описание этого критерия.</span><span class="sxs-lookup"><span data-stu-id="912bb-112">The description of this criterion.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="912bb-113">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="912bb-113">JSON representation</span></span>

<span data-ttu-id="912bb-114">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="912bb-114">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.rubricCriterion",
  "baseType": null
}-->

```json
{
  "description": {"@odata.type": "microsoft.graph.itemBody"}
}
```

<!-- uuid: 16cd6b66-4b1a-43a1-adaf-3a886856ed98
2019-02-04 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "rubricCriterion resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->