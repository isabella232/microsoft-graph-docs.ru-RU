---
title: Тип ресурса recipient
description: 'Представляет сведения о пользователе, который отправляет или получает событие, сообщение или запись в группе. '
localization_priority: Normal
ms.openlocfilehash: 9718d7e6ce09a42e742303aaed484fa6335f3cbc
ms.sourcegitcommit: d95f6d39a0479da6e531f3734c4029dc596b9a3f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/30/2019
ms.locfileid: "29642585"
---
# <a name="recipient-resource-type"></a><span data-ttu-id="1b004-103">Тип ресурса recipient</span><span class="sxs-lookup"><span data-stu-id="1b004-103">recipient resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="1b004-104">Представляет сведения о пользователе, который отправляет или получает событие, сообщение или запись в группе.</span><span class="sxs-lookup"><span data-stu-id="1b004-104">Represents information about a user in the sending or receiving end of an event, message or group post.</span></span> 

## <a name="properties"></a><span data-ttu-id="1b004-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="1b004-105">Properties</span></span>
| <span data-ttu-id="1b004-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="1b004-106">Property</span></span>     | <span data-ttu-id="1b004-107">Тип</span><span class="sxs-lookup"><span data-stu-id="1b004-107">Type</span></span>   |<span data-ttu-id="1b004-108">Описание</span><span class="sxs-lookup"><span data-stu-id="1b004-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="1b004-109">emailAddress</span><span class="sxs-lookup"><span data-stu-id="1b004-109">emailAddress</span></span>|[<span data-ttu-id="1b004-110">EmailAddress</span><span class="sxs-lookup"><span data-stu-id="1b004-110">EmailAddress</span></span>](emailaddress.md)|<span data-ttu-id="1b004-111">Электронный адрес получателя.</span><span class="sxs-lookup"><span data-stu-id="1b004-111">The recipient's email address.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="1b004-112">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="1b004-112">JSON representation</span></span>

<span data-ttu-id="1b004-113">Ниже представлено описание ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="1b004-113">Here is a JSON representation of the resource</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.recipient"
}-->

```json
{
  "emailAddress": {"@odata.type": "microsoft.graph.emailAddress"}
}

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "recipient resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/recipient.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
