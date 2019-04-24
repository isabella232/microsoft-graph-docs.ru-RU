---
title: Тип ресурса МитингпартиЦипантинфо
description: Сведения о участниках собрания.
author: VinodRavichandran
localization_priority: Normal
ms.prod: microsoft-teams
ms.openlocfilehash: 1ba727344b1f653125a482b592e7d28c11d1d3d5
ms.sourcegitcommit: 0ce657622f42c510a104156a96bf1f1f040bc1cd
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/24/2019
ms.locfileid: "32457118"
---
# <a name="meetingparticipantinfo-resource-type"></a><span data-ttu-id="7b373-103">Тип ресурса МитингпартиЦипантинфо</span><span class="sxs-lookup"><span data-stu-id="7b373-103">meetingParticipantInfo resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="7b373-104">Сведения о участниках собрания.</span><span class="sxs-lookup"><span data-stu-id="7b373-104">Information about a participant in a meeting.</span></span>

## <a name="properties"></a><span data-ttu-id="7b373-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="7b373-105">Properties</span></span>

| <span data-ttu-id="7b373-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="7b373-106">Property</span></span>       | <span data-ttu-id="7b373-107">Тип</span><span class="sxs-lookup"><span data-stu-id="7b373-107">Type</span></span>                          | <span data-ttu-id="7b373-108">Описание</span><span class="sxs-lookup"><span data-stu-id="7b373-108">Description</span></span>                              |
|:---------------|:------------------------------|:-----------------------------------------|
| <span data-ttu-id="7b373-109">хищения</span><span class="sxs-lookup"><span data-stu-id="7b373-109">identity</span></span>       | [<span data-ttu-id="7b373-110">identitySet</span><span class="sxs-lookup"><span data-stu-id="7b373-110">identitySet</span></span>](identityset.md) | <span data-ttu-id="7b373-111">Сведения об удостоверении участника.</span><span class="sxs-lookup"><span data-stu-id="7b373-111">Identity information of the participant.</span></span> |
| <span data-ttu-id="7b373-112">Основное</span><span class="sxs-lookup"><span data-stu-id="7b373-112">upn</span></span>            | <span data-ttu-id="7b373-113">Строка</span><span class="sxs-lookup"><span data-stu-id="7b373-113">String</span></span>                        | <span data-ttu-id="7b373-114">Имя участника пользователя.</span><span class="sxs-lookup"><span data-stu-id="7b373-114">User principal name of the participant.</span></span>  |

## <a name="json-representation"></a><span data-ttu-id="7b373-115">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="7b373-115">JSON representation</span></span>

<span data-ttu-id="7b373-116">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="7b373-116">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingParticipantInfo"
}-->
```json
{
  "identity": {"@odata.type": "#microsoft.graph.identitySet"},
  "upn": "String"
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "meetingParticipantInfo resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/meetingparticipantinfo.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
