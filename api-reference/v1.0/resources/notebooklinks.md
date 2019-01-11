---
title: Тип ресурса notebookLinks
description: Ссылки для открытия записной книжки OneNote.
author: Jewan-microsoft
localization_priority: Normal
ms.openlocfilehash: 2666d7da98eeb6115a179ddbbadcd8b5e7f941d7
ms.sourcegitcommit: d2b3ca32602ffa76cc7925d7f4d1e2258e611ea5
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/11/2019
ms.locfileid: "27826887"
---
# <a name="notebooklinks-resource-type"></a><span data-ttu-id="8f56e-103">Тип ресурса notebookLinks</span><span class="sxs-lookup"><span data-stu-id="8f56e-103">notebookLinks resource type</span></span>

<span data-ttu-id="8f56e-104">Ссылки для открытия записной книжки OneNote.</span><span class="sxs-lookup"><span data-stu-id="8f56e-104">Links for opening a OneNote notebook.</span></span>

## <a name="json-representation"></a><span data-ttu-id="8f56e-105">Представление в формате JSON</span><span class="sxs-lookup"><span data-stu-id="8f56e-105">JSON representation</span></span>

<span data-ttu-id="8f56e-106">Ниже представлено описание ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="8f56e-106">Here is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.notebookLinks"
}-->

```json
{
  "oneNoteClientUrl": {"@odata.type": "microsoft.graph.externalLink"},
  "oneNoteWebUrl": {"@odata.type": "microsoft.graph.externalLink"}
}

```
## <a name="properties"></a><span data-ttu-id="8f56e-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="8f56e-107">Properties</span></span>
| <span data-ttu-id="8f56e-108">Свойство</span><span class="sxs-lookup"><span data-stu-id="8f56e-108">Property</span></span>     | <span data-ttu-id="8f56e-109">Тип</span><span class="sxs-lookup"><span data-stu-id="8f56e-109">Type</span></span>   |<span data-ttu-id="8f56e-110">Описание</span><span class="sxs-lookup"><span data-stu-id="8f56e-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="8f56e-111">oneNoteClientUrl</span><span class="sxs-lookup"><span data-stu-id="8f56e-111">oneNoteClientUrl</span></span>|[<span data-ttu-id="8f56e-112">externalLink</span><span class="sxs-lookup"><span data-stu-id="8f56e-112">externalLink</span></span>](externallink.md)|<span data-ttu-id="8f56e-113">Открывает записную книжку в собственном клиенте OneNote, если он установлен.</span><span class="sxs-lookup"><span data-stu-id="8f56e-113">Opens the notebook in the OneNote native client if it's installed.</span></span>|
|<span data-ttu-id="8f56e-114">oneNoteWebUrl</span><span class="sxs-lookup"><span data-stu-id="8f56e-114">oneNoteWebUrl</span></span>|[<span data-ttu-id="8f56e-115">externalLink</span><span class="sxs-lookup"><span data-stu-id="8f56e-115">externalLink</span></span>](externallink.md)|<span data-ttu-id="8f56e-116">Открывает записную книжку в OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="8f56e-116">Opens the notebook in OneNote Online.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "notebookLinks resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->
