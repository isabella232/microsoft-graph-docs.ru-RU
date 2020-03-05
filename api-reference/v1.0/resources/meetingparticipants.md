---
title: Тип ресурса МитингпартиЦипантс
description: Участники собрания.
author: ananmishr
localization_priority: Normal
ms.prod: cloud-communications
doc_type: resourcePageType
ms.openlocfilehash: dd00cbf5ce8395a819136ad9e655fa7670e5f3fa
ms.sourcegitcommit: 272996d2772b51105ec25f1cf7482ecda3b74ebe
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2020
ms.locfileid: "42447418"
---
# <a name="meetingparticipants-resource-type"></a><span data-ttu-id="3e211-103">Тип ресурса МитингпартиЦипантс</span><span class="sxs-lookup"><span data-stu-id="3e211-103">meetingParticipants resource type</span></span>

<span data-ttu-id="3e211-104">Пространство имен: Microsoft. Graph</span><span class="sxs-lookup"><span data-stu-id="3e211-104">Namespace: microsoft.graph</span></span>

<span data-ttu-id="3e211-105">Участники собрания.</span><span class="sxs-lookup"><span data-stu-id="3e211-105">Participants in a meeting.</span></span>

## <a name="properties"></a><span data-ttu-id="3e211-106">Свойства</span><span class="sxs-lookup"><span data-stu-id="3e211-106">Properties</span></span>

| <span data-ttu-id="3e211-107">Свойство</span><span class="sxs-lookup"><span data-stu-id="3e211-107">Property</span></span>       | <span data-ttu-id="3e211-108">Тип</span><span class="sxs-lookup"><span data-stu-id="3e211-108">Type</span></span>    | <span data-ttu-id="3e211-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3e211-109">Description</span></span>|
|:---------------|:--------|:----------|
| <span data-ttu-id="3e211-110">attendees</span><span class="sxs-lookup"><span data-stu-id="3e211-110">attendees</span></span> | <span data-ttu-id="3e211-111">Коллекция [митингпартиЦипантинфо](meetingparticipantinfo.md)</span><span class="sxs-lookup"><span data-stu-id="3e211-111">[meetingParticipantInfo](meetingparticipantinfo.md) collection</span></span> |  |
| <span data-ttu-id="3e211-112">organizer</span><span class="sxs-lookup"><span data-stu-id="3e211-112">organizer</span></span> | [<span data-ttu-id="3e211-113">митингпартиЦипантинфо</span><span class="sxs-lookup"><span data-stu-id="3e211-113">meetingParticipantInfo</span></span>](meetingparticipantinfo.md) |  |

## <a name="json-representation"></a><span data-ttu-id="3e211-114">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="3e211-114">JSON representation</span></span>

<span data-ttu-id="3e211-115">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="3e211-115">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "optionalProperties": [

  ],
  "@odata.type": "microsoft.graph.meetingParticipants"
}-->
```json
{
  "attendees": [{"@odata.type": "#microsoft.graph.meetingParticipantInfo"}],
  "organizer": {"@odata.type": "#microsoft.graph.meetingParticipantInfo"}
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "meetingParticipants resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
