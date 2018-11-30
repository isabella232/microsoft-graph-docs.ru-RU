---
title: Тип ресурса mediaPrompt
description: Тип mediaPrompt.
ms.openlocfilehash: 1a782d391110d35b07b551e44ebd3b931dbcadba
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27080912"
---
# <a name="mediaprompt-resource-type"></a><span data-ttu-id="46ce5-103">Тип ресурса mediaPrompt</span><span class="sxs-lookup"><span data-stu-id="46ce5-103">mediaPrompt resource type</span></span>

> <span data-ttu-id="46ce5-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="46ce5-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="46ce5-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="46ce5-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="46ce5-106">Тип mediaPrompt.</span><span class="sxs-lookup"><span data-stu-id="46ce5-106">The mediaPrompt type.</span></span>

## <a name="properties"></a><span data-ttu-id="46ce5-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="46ce5-107">Properties</span></span>

| <span data-ttu-id="46ce5-108">Свойство</span><span class="sxs-lookup"><span data-stu-id="46ce5-108">Property</span></span>    | <span data-ttu-id="46ce5-109">Тип</span><span class="sxs-lookup"><span data-stu-id="46ce5-109">Type</span></span>                      | <span data-ttu-id="46ce5-110">Description</span><span class="sxs-lookup"><span data-stu-id="46ce5-110">Description</span></span>                                                                     |
| :---------- | :------------------------ | :------------------------------------------------------------------------------ |
| <span data-ttu-id="46ce5-111">цикл</span><span class="sxs-lookup"><span data-stu-id="46ce5-111">loop</span></span>        | <span data-ttu-id="46ce5-112">Int32</span><span class="sxs-lookup"><span data-stu-id="46ce5-112">Int32</span></span>                     | <span data-ttu-id="46ce5-113">Счетчик цикла.</span><span class="sxs-lookup"><span data-stu-id="46ce5-113">The loop count.</span></span> <span data-ttu-id="46ce5-114">значение 0 указывает цикл бесконечно.</span><span class="sxs-lookup"><span data-stu-id="46ce5-114">0 value indicates to loop infinitely.</span></span> <span data-ttu-id="46ce5-115">Значение по умолчанию — `1`.</span><span class="sxs-lookup"><span data-stu-id="46ce5-115">The default value is `1`.</span></span> |
| <span data-ttu-id="46ce5-116">mediaInfo</span><span class="sxs-lookup"><span data-stu-id="46ce5-116">mediaInfo</span></span>   | [<span data-ttu-id="46ce5-117">mediaInfo</span><span class="sxs-lookup"><span data-stu-id="46ce5-117">mediaInfo</span></span>](mediainfo.md) | <span data-ttu-id="46ce5-118">Сведения о мультимедиа</span><span class="sxs-lookup"><span data-stu-id="46ce5-118">The media information</span></span>                                                           |

## <a name="json-representation"></a><span data-ttu-id="46ce5-119">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="46ce5-119">JSON representation</span></span>

<span data-ttu-id="46ce5-120">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="46ce5-120">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.mediaPrompt"
}-->

```json
{
  "loop": 1024,
  "mediaInfo": { "@odata.type": "#microsoft.graph.mediaInfo" }
}
```

## <a name="example"></a><span data-ttu-id="46ce5-121">Пример</span><span class="sxs-lookup"><span data-stu-id="46ce5-121">Example</span></span>

<!-- {
  "blockType": "example",
  "@odata.type": "microsoft.graph.mediaPrompt"
}-->
```json
{
  "mediaInfo": {
    "uri": "https://cdn.contoso.com/beep.wav",
    "resourceId": "1D6DE2D4-CD51-4309-8DAA-70768651088E"
  },
  "loop": 5
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "mediaPrompt resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
