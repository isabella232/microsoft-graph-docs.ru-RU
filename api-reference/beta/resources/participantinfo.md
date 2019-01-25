---
title: Тип ресурса participantInfo
description: Содержит дополнительные свойства сведения об удостоверениях, участников
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 3d040fd5be86068c30e7a63dae50888c4f3ec756
ms.sourcegitcommit: 3d24047b3af46136734de2486b041e67a34f3d83
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/24/2019
ms.locfileid: "29528349"
---
# <a name="participantinfo-resource-type"></a><span data-ttu-id="474fb-103">Тип ресурса participantInfo</span><span class="sxs-lookup"><span data-stu-id="474fb-103">participantInfo resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="474fb-104">Содержит дополнительные свойства сведения об удостоверениях, участников</span><span class="sxs-lookup"><span data-stu-id="474fb-104">Contains additional properties about the participant identity</span></span>

## <a name="properties"></a><span data-ttu-id="474fb-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="474fb-105">Properties</span></span>

| <span data-ttu-id="474fb-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="474fb-106">Property</span></span>       | <span data-ttu-id="474fb-107">Тип</span><span class="sxs-lookup"><span data-stu-id="474fb-107">Type</span></span>                          | <span data-ttu-id="474fb-108">Описание</span><span class="sxs-lookup"><span data-stu-id="474fb-108">Description</span></span>  |
|:---------------|:------------------------------|:-------------|
| <span data-ttu-id="474fb-109">identity</span><span class="sxs-lookup"><span data-stu-id="474fb-109">identity</span></span>       | [<span data-ttu-id="474fb-110">identitySet</span><span class="sxs-lookup"><span data-stu-id="474fb-110">identitySet</span></span>](identityset.md) | <span data-ttu-id="474fb-111">[IdentitySet](identityset.md) , связанный с данным участником.</span><span class="sxs-lookup"><span data-stu-id="474fb-111">The [identitySet](identityset.md) associated with this participant.</span></span> |
| <span data-ttu-id="474fb-112">languageId</span><span class="sxs-lookup"><span data-stu-id="474fb-112">languageId</span></span>     | <span data-ttu-id="474fb-113">String</span><span class="sxs-lookup"><span data-stu-id="474fb-113">String</span></span>                        | <span data-ttu-id="474fb-114">Строка языка и региональных параметров языка.</span><span class="sxs-lookup"><span data-stu-id="474fb-114">The language culture string.</span></span> |
| <span data-ttu-id="474fb-115">область</span><span class="sxs-lookup"><span data-stu-id="474fb-115">region</span></span>         | <span data-ttu-id="474fb-116">String</span><span class="sxs-lookup"><span data-stu-id="474fb-116">String</span></span>                        | <span data-ttu-id="474fb-117">Область участника.</span><span class="sxs-lookup"><span data-stu-id="474fb-117">Region of the participant.</span></span> |

## <a name="json-representation"></a><span data-ttu-id="474fb-118">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="474fb-118">JSON representation</span></span>

<span data-ttu-id="474fb-119">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="474fb-119">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [
    "languageId", "region"
  ],
  "@odata.type": "microsoft.graph.participantInfo"
}-->
```json
{
  "identity": { "@odata.type": "#microsoft.graph.identitySet" },
  "languageId": "String",
  "region": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "participantInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/participantinfo.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
