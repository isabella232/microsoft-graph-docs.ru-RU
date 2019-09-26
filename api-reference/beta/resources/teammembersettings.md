---
title: Тип ресурса Теаммемберсеттингс
description: Параметры для настройки того, могут ли участники выполнять определенные действия, например создавать каналы и добавлять ботов в команде.
localization_priority: Normal
author: clearab
ms.prod: microsoft-teams
doc_type: resourcePageType
ms.openlocfilehash: 8967eb083ad2bd413277c42b688c2d0c48d8244b
ms.sourcegitcommit: 86903a4730bbd825eabb7f0a1b2429723cc8b1e6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/26/2019
ms.locfileid: "37196261"
---
# <a name="teammembersettings-resource-type"></a><span data-ttu-id="2d416-103">Тип ресурса Теаммемберсеттингс</span><span class="sxs-lookup"><span data-stu-id="2d416-103">teamMemberSettings resource type</span></span>

[!INCLUDE [beta-disclaimer](../../includes/beta-disclaimer.md)]

<span data-ttu-id="2d416-104">Параметры для настройки того, могут ли участники выполнять определенные действия, например создавать каналы и добавлять боты в [команду](team.md).</span><span class="sxs-lookup"><span data-stu-id="2d416-104">Settings to configure whether members can perform certain actions, for example, create channels and add bots, in the [team](team.md).</span></span>

## <a name="properties"></a><span data-ttu-id="2d416-105">Свойства</span><span class="sxs-lookup"><span data-stu-id="2d416-105">Properties</span></span>
| <span data-ttu-id="2d416-106">Свойство</span><span class="sxs-lookup"><span data-stu-id="2d416-106">Property</span></span>     | <span data-ttu-id="2d416-107">Тип</span><span class="sxs-lookup"><span data-stu-id="2d416-107">Type</span></span>   |<span data-ttu-id="2d416-108">Описание</span><span class="sxs-lookup"><span data-stu-id="2d416-108">Description</span></span>|
|:---------------|:--------|:----------|
|<span data-ttu-id="2d416-109">алловкреатеупдатечаннелс</span><span class="sxs-lookup"><span data-stu-id="2d416-109">allowCreateUpdateChannels</span></span>|<span data-ttu-id="2d416-110">Boolean.</span><span class="sxs-lookup"><span data-stu-id="2d416-110">Boolean</span></span>|<span data-ttu-id="2d416-111">Если задано значение true, участники могут добавлять и обновлять любые каналы.</span><span class="sxs-lookup"><span data-stu-id="2d416-111">If set to true, members can add and update any channels.</span></span>|
|<span data-ttu-id="2d416-112">алловкреатеприватечаннелс</span><span class="sxs-lookup"><span data-stu-id="2d416-112">allowCreatePrivateChannels</span></span>|<span data-ttu-id="2d416-113">Boolean.</span><span class="sxs-lookup"><span data-stu-id="2d416-113">Boolean</span></span>|<span data-ttu-id="2d416-114">Если задано значение true, участники могут добавлять и обновлять частные каналы.</span><span class="sxs-lookup"><span data-stu-id="2d416-114">If set to true, members can add and update private channels.</span></span>|
|<span data-ttu-id="2d416-115">алловделетечаннелс</span><span class="sxs-lookup"><span data-stu-id="2d416-115">allowDeleteChannels</span></span>|<span data-ttu-id="2d416-116">Boolean.</span><span class="sxs-lookup"><span data-stu-id="2d416-116">Boolean</span></span>|<span data-ttu-id="2d416-117">Если задано значение true, участники могут удалять каналы.</span><span class="sxs-lookup"><span data-stu-id="2d416-117">If set to true, members can delete channels.</span></span>|
|<span data-ttu-id="2d416-118">алловаддремовеаппс</span><span class="sxs-lookup"><span data-stu-id="2d416-118">allowAddRemoveApps</span></span>|<span data-ttu-id="2d416-119">Boolean.</span><span class="sxs-lookup"><span data-stu-id="2d416-119">Boolean</span></span>|<span data-ttu-id="2d416-120">Если задано значение true, участники могут добавлять и удалять приложения.</span><span class="sxs-lookup"><span data-stu-id="2d416-120">If set to true, members can add and remove apps.</span></span>|
|<span data-ttu-id="2d416-121">алловкреатеупдатеремоветабс</span><span class="sxs-lookup"><span data-stu-id="2d416-121">allowCreateUpdateRemoveTabs</span></span>|<span data-ttu-id="2d416-122">Boolean.</span><span class="sxs-lookup"><span data-stu-id="2d416-122">Boolean</span></span>|<span data-ttu-id="2d416-123">Если задано значение true, члены могут добавлять, обновлять и удалять вкладки.</span><span class="sxs-lookup"><span data-stu-id="2d416-123">If set to true, members can add, update, and remove tabs.</span></span> |
|<span data-ttu-id="2d416-124">алловкреатеупдатеремовеконнекторс</span><span class="sxs-lookup"><span data-stu-id="2d416-124">allowCreateUpdateRemoveConnectors</span></span>|<span data-ttu-id="2d416-125">Boolean.</span><span class="sxs-lookup"><span data-stu-id="2d416-125">Boolean</span></span>|<span data-ttu-id="2d416-126">Если задано значение true, участники могут добавлять, обновлять и удалять соединители.</span><span class="sxs-lookup"><span data-stu-id="2d416-126">If set to true, members can add, update, and remove connectors.</span></span>|

## <a name="json-representation"></a><span data-ttu-id="2d416-127">Представление JSON</span><span class="sxs-lookup"><span data-stu-id="2d416-127">JSON representation</span></span>

<span data-ttu-id="2d416-128">Ниже указано представление ресурса в формате JSON.</span><span class="sxs-lookup"><span data-stu-id="2d416-128">The following is a JSON representation of the resource.</span></span>

<!-- {
  "blockType": "resource",
  "@odata.type": "microsoft.graph.teamMemberSettings"
}-->

```json
{
  "allowCreateUpdateChannels": true,
  "allowCreatePrivateChannels": true,
  "allowDeleteChannels": true,
  "allowAddRemoveApps": true,
  "allowCreateUpdateRemoveTabs": true,
  "allowCreateUpdateRemoveConnectors": true
}
```

<!-- uuid: 8fcb5dbc-d5aa-4681-8e31-b001d5168d79
2015-10-25 14:57:30 UTC -->
<!--
{
  "type": "#page.annotation",
  "description": "team's memberSettings resource",
  "keywords": "",
  "section": "documentation",
  "tocPath": "",
  "suppressions": []
}
-->
