---
title: Тип ресурса notebookLinks
description: Ссылки для открытия записной книжки OneNote.
ms.openlocfilehash: 33f9a877ea6cae64acf3f05234362bfb86530c2f
ms.sourcegitcommit: 334e84b4aed63162bcc31831cffd6d363dafee02
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/29/2018
ms.locfileid: "27075996"
---
# <a name="notebooklinks-resource-type"></a><span data-ttu-id="41a07-103">Тип ресурса notebookLinks</span><span class="sxs-lookup"><span data-stu-id="41a07-103">notebookLinks resource type</span></span>

> <span data-ttu-id="41a07-104">**Важно!** API бета-версии (/beta) в Microsoft Graph проходят тестирование и могут быть изменены.</span><span class="sxs-lookup"><span data-stu-id="41a07-104">**Important:** APIs under the /beta version in Microsoft Graph are in preview and are subject to change.</span></span> <span data-ttu-id="41a07-105">Использование этих API в производственных приложениях не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="41a07-105">Use of these APIs in production applications is not supported.</span></span>

<span data-ttu-id="41a07-106">Ссылки для открытия записной книжки OneNote.</span><span class="sxs-lookup"><span data-stu-id="41a07-106">Links for opening a OneNote notebook.</span></span>

## <a name="json-representation"></a><span data-ttu-id="41a07-107">Представление в формате JSON</span><span class="sxs-lookup"><span data-stu-id="41a07-107">JSON representation</span></span>

<span data-ttu-id="41a07-108">Ниже представлено описание ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="41a07-108">Here is a JSON representation of the resource.</span></span>

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
## <a name="properties"></a><span data-ttu-id="41a07-109">Свойства</span><span class="sxs-lookup"><span data-stu-id="41a07-109">Properties</span></span>
| <span data-ttu-id="41a07-110">Свойство</span><span class="sxs-lookup"><span data-stu-id="41a07-110">Property</span></span>     | <span data-ttu-id="41a07-111">Тип</span><span class="sxs-lookup"><span data-stu-id="41a07-111">Type</span></span>   |<span data-ttu-id="41a07-112">Описание</span><span class="sxs-lookup"><span data-stu-id="41a07-112">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="41a07-113">oneNoteClientUrl</span><span class="sxs-lookup"><span data-stu-id="41a07-113">oneNoteClientUrl</span></span>|[<span data-ttu-id="41a07-114">externalLink</span><span class="sxs-lookup"><span data-stu-id="41a07-114">externalLink</span></span>](externallink.md)|<span data-ttu-id="41a07-115">Открывает записную книжку в собственном клиенте OneNote, если он установлен.</span><span class="sxs-lookup"><span data-stu-id="41a07-115">Opens the notebook in the OneNote native client if it's installed.</span></span>|
|<span data-ttu-id="41a07-116">oneNoteWebUrl</span><span class="sxs-lookup"><span data-stu-id="41a07-116">oneNoteWebUrl</span></span>|[<span data-ttu-id="41a07-117">externalLink</span><span class="sxs-lookup"><span data-stu-id="41a07-117">externalLink</span></span>](externallink.md)|<span data-ttu-id="41a07-118">Открывает записную книжку в OneNote Online.</span><span class="sxs-lookup"><span data-stu-id="41a07-118">Opens the notebook in OneNote Online.</span></span>|

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!-- {
  "type": "#page.annotation",
  "description": "notebookLinks resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": ""
}-->