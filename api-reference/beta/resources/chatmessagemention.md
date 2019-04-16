---
title: Тип ресурса Чатмессажементион
description: 'Представляет упоминание в объекте chatMessage. Упоминание может быть у пользователя, группы, ленты или канала. '
localization_priority: Normal
author: nkramer
ms.openlocfilehash: 5d7304325e48c87bfd75b57bf49585f66a77b262
ms.sourcegitcommit: a39db1154a07aa0dd7e96fb6f9d7e891a812207e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/16/2019
ms.locfileid: "31889998"
---
# <a name="chatmessagemention-resource-type"></a><span data-ttu-id="9dc5f-104">Тип ресурса Чатмессажементион</span><span class="sxs-lookup"><span data-stu-id="9dc5f-104">chatMessageMention resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="9dc5f-105">Представляет упоминание в объекте [chatMessage](chatmessage.md) .</span><span class="sxs-lookup"><span data-stu-id="9dc5f-105">Represents a mention in a [chatMessage](chatmessage.md) entity.</span></span> <span data-ttu-id="9dc5f-106">Упоминание может быть у пользователя, группы, ленты или канала.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-106">The mention can be to a user, team, bot, or channel.</span></span> 

## <a name="properties"></a><span data-ttu-id="9dc5f-107">Свойства</span><span class="sxs-lookup"><span data-stu-id="9dc5f-107">Properties</span></span>
| <span data-ttu-id="9dc5f-108">Свойство</span><span class="sxs-lookup"><span data-stu-id="9dc5f-108">Property</span></span>     | <span data-ttu-id="9dc5f-109">Тип</span><span class="sxs-lookup"><span data-stu-id="9dc5f-109">Type</span></span>   |<span data-ttu-id="9dc5f-110">Описание</span><span class="sxs-lookup"><span data-stu-id="9dc5f-110">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="9dc5f-111">id</span><span class="sxs-lookup"><span data-stu-id="9dc5f-111">id</span></span>|<span data-ttu-id="9dc5f-112">int</span><span class="sxs-lookup"><span data-stu-id="9dc5f-112">int</span></span>|<span data-ttu-id="9dc5f-113">Индекс упоминаемого объекта.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-113">Index of the entity being mentioned.</span></span> <span data-ttu-id="9dc5f-114">Соответствует <at id="index"> тегу основного текста сообщения.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-114">Matches with the <at id="index"> tag of the message body.</span></span>|
|<span data-ttu-id="9dc5f-115">Ментионтекст</span><span class="sxs-lookup"><span data-stu-id="9dc5f-115">mentionText</span></span>|<span data-ttu-id="9dc5f-116">string</span><span class="sxs-lookup"><span data-stu-id="9dc5f-116">string</span></span>|<span data-ttu-id="9dc5f-117">Строка, используемая для представления упоминания.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-117">String used to represent the mention.</span></span> <span data-ttu-id="9dc5f-118">Например, отображаемое имя пользователя, имя группы.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-118">For example, User display name, Team name.</span></span>|
|<span data-ttu-id="9dc5f-119">котором</span><span class="sxs-lookup"><span data-stu-id="9dc5f-119">mentioned</span></span>|[<span data-ttu-id="9dc5f-120">identitySet</span><span class="sxs-lookup"><span data-stu-id="9dc5f-120">identitySet</span></span>](identityset.md)|<span data-ttu-id="9dc5f-121">Упоминаемая сущность (пользователь, приложение, группа или канал).</span><span class="sxs-lookup"><span data-stu-id="9dc5f-121">The entity (user, application, team, or channel) that was mentioned.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="9dc5f-122">Представление в формате JSON</span><span class="sxs-lookup"><span data-stu-id="9dc5f-122">JSON representation</span></span>

<span data-ttu-id="9dc5f-123">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="9dc5f-123">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "baseType": "microsoft.graph.entity",
  "@odata.type": "microsoft.graph.chatMessageMention"
}-->

```json
{
  "id": "number",
  "mentionText": "string",
  "mentioned": "microsoft.graph.identitySet"
 }

```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "chat mention resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": [
    "Error: /api-reference/beta/resources/chatmessagemention.md:\r\n      Exception processing links.\r\n    System.ArgumentException: Link Definition was null. Link text: !INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)\r\n      at ApiDoctor.Validation.DocFile.get_LinkDestinations()\r\n      at ApiDoctor.Validation.DocSet.ValidateLinks(Boolean includeWarnings, String[] relativePathForFiles, IssueLogger issues, Boolean requireFilenameCaseMatch, Boolean printOrphanedFiles)"
  ]
}
-->
